---
layout: post
title: "Gradio Part 2: Build and Share a Fun ML App to Reveal Someone's Personality by How They Write"
date: 2025-04-16
categories: [ml, tutorials]
excerpt: "Create and share a machine learning personality prediction app with Gradio."
comments: true
---


In [Part 1](./2025-04-14-intro-to-gradio-part-1.md), we turned a simple function into a web app using Gradio. In this part, we go deeper: we’ll train a real **text classification model on a psychological dataset**, wrap it with Gradio, and let users type about themselves to see which **MBTI personality type** they might be.

And this time, we’re not just guessing **Introvert vs Extrovert**. We’re going for all **16 MBTI types**—like INTP, ENFJ, ISFP, etc.

By the end of this guide, you’ll know how to:

- Download and preprocess real-world personality data
- Train a transformer model to classify personality types from writing
- Build a beautiful interactive interface using Gradio
- Show predictions with **confidence scores**
- Share your app publicly in seconds

Click here to follow on Colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ChantelleAA/ChantelleAA.github.io/blob/gh-pages/_posts/notebooks/gradio2/mbti_gradio_app.ipynb)

## Step 1: Download the Dataset

We'll use the MBTI Personality Dataset from Kaggle. To help others access it directly without needing a Kaggle account, here’s how to download it from an alternate public source.

Let's start with loading and exploring the dataset.

```python
import pandas as pd

# Download and load the dataset
file_id = "1I4g7CvmYDHSn48SE7EXdLkiYqX-4gBse"
url = f"https://drive.google.com/uc?export=download&id={file_id}"

df = pd.read_csv(url)


# Combine text from all posts
df['posts'] = df['posts'].apply(lambda x: x.replace('|||', ' '))

# Check the 16 MBTI types
print("Unique types:", df['type'].unique())
```


---

## Step 2: What Is the MBTI?

MBTI stands for Myers-Briggs Type Indicator. It classifies people into 16 personality types based on 4 letters:

- **I/E** – Introversion vs Extroversion  
- **N/S** – Intuition vs Sensing  
- **T/F** – Thinking vs Feeling  
- **P/J** – Perceiving vs Judging

For example, someone who is analytical and reserved might be **INTP**, while someone empathetic and sociable might be **ENFJ**.


---

## Step 3: Prepare the Data

Let’s look at how we can prepare this data for model training.

```python
from sklearn.model_selection import train_test_split

# Filter to include only rows with non-empty posts
df = df[df['posts'].notna()]

# Split into train and test
X_train, X_test, y_train, y_test = train_test_split(df['posts'], df['type'], test_size=0.2, random_state=42)
```

---

## Step 4: Using Transformers for Deeper Analysis

We’ll use the **DistilBERT** model from Hugging Face for this. It’s a smaller, faster version of BERT that performs well on text classification tasks.

### Install dependencies

```bash
pip install transformers datasets scikit-learn gradio
```

---

### Load and Fine-Tune DistilBERT

We'll use Hugging Face’s `transformers` and `datasets` libraries to tokenize and fine-tune the model.

```python
from transformers import DistilBertTokenizerFast, DistilBertForSequenceClassification, Trainer, TrainingArguments
from datasets import Dataset
import numpy as np

# Encode MBTI types into integers
unique_labels = sorted(df['type'].unique())
label2id = {label: i for i, label in enumerate(unique_labels)}
id2label = {i: label for label, i in label2id.items()}

# Add label IDs to data
train_data = pd.DataFrame({'text': X_train, 'label': [label2id[y] for y in y_train]})
test_data = pd.DataFrame({'text': X_test, 'label': [label2id[y] for y in y_test]})

# Convert to Hugging Face Dataset
train_dataset = Dataset.from_pandas(train_data)
test_dataset = Dataset.from_pandas(test_data)

# Tokenizer
tokenizer = DistilBertTokenizerFast.from_pretrained('distilbert-base-uncased')

def tokenize(batch):
    return tokenizer(batch['text'], padding=True, truncation=True)

train_dataset = train_dataset.map(tokenize, batched=True)
test_dataset = test_dataset.map(tokenize, batched=True)

# Model
model = DistilBertForSequenceClassification.from_pretrained('distilbert-base-uncased', num_labels=16, id2label=id2label, label2id=label2id)
```

---

### Train the Model

```python
training_args = TrainingArguments(
    output_dir='./results',
    learning_rate=2e-5,
    per_device_train_batch_size=8,
    num_train_epochs=2,
    evaluation_strategy='epoch',
    logging_dir='./logs',
    logging_steps=10,
)

trainer = Trainer(
    model=model,
    args=training_args,
    train_dataset=train_dataset,
    eval_dataset=test_dataset
)

trainer.train()
```

This will take a few minutes depending on your machine. If you’re running in Google Colab, it’s faster with GPU.

---

## Step 5: Add a Gradio Interface

Now let's make the model interactive.

```python
import gradio as gr
import torch

def predict_mbti(text):
    inputs = tokenizer(text, return_tensors="pt", truncation=True, padding=True)
    outputs = model(**inputs)
    probs = torch.nn.functional.softmax(outputs.logits, dim=1)
    conf, pred_id = torch.max(probs, dim=1)
    pred_label = model.config.id2label[pred_id.item()]
    
    top5 = torch.topk(probs, k=5)
    result = "\n".join([f"{model.config.id2label[i]}: {probs[0][i]:.2f}" for i in top5.indices[0]])

    return f"**Predicted MBTI Type: {pred_label}**\n\nConfidence: {conf.item():.2f}\n\nTop predictions:\n{result}"
```

---

### Interface Code

```python
interface = gr.Interface(
    fn=predict_mbti,
    inputs=gr.Textbox(lines=6, placeholder="Write a paragraph about yourself..."),
    outputs=gr.Markdown(),
    title="MBTI Personality Predictor (All 16 Types)",
    description="This app uses a Hugging Face transformer model to analyze your writing and predict your MBTI type. It's trained on real Kaggle data and shows confidence levels for each prediction."
)

interface.launch()
```
