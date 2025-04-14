---
layout: post
title: "Introduction to Gradio (How to easily deploy functions or ML models in Python)"
date: 2025-04-12
categories: [intro, tutorials]
excerpt: "Gradio is a Python library that allows you to quickly create customizable web interfaces for your machine learning models, data analyses, or any Python function."
---

# Gradio: Making Python Code Sharing Effortless

Gradio is an amazing library created by Hugging Face to make sharing of code developed in Python very easy and efficient. The amazing thing is that asides being able to host it locally, you can actually also host it publicly so a computer which doesn't hold your code can execute it.

Imagine you wrote an amazing code that implements some function that you have created or some model whose weights are on your computer. You would like for your friends or your colleagues to test out your function or your model to see how it works or to even try to test or break the model.

Trying to deploy your function or model for a very small usecase could be overkill having to write HTML code, or some front end development. GitHub Pages is restricted to one deployment at a time, but enter Gradio, a simple straightforward way to do it.

I don't have enough words to quantify the excitement I feel about how exactly amazing the library is without showing you an example! For this part, we would look at a simple function and how to deploy it with Gradio.

## Example

Let's say you came up with a text analysis function that counts the frequency of words in a passage and returns the most common words. Here's how you can deploy it with Gradio:

```python
import gradio as gr
from collections import Counter
import re

def analyze_text(text):
    # Clean text and convert to lowercase
    text = re.sub(r'[^\w\s]', '', text.lower())
    
    # Split into words and count frequencies
    words = text.split()
    word_counts = Counter(words)
    
    # Get the 5 most common words
    most_common = word_counts.most_common(5)
    
    # Format results
    result = "Most frequent words:\n"
    for word, count in most_common:
        result += f"'{word}': {count} occurrences\n"
    
    return result

# Create Gradio interface
demo = gr.Interface(
    fn=analyze_text,
    inputs=gr.Textbox(lines=10, placeholder="Paste your text here..."),
    outputs="text",
    title="Text Word Frequency Analyzer",
    description="Enter text to analyze word frequency and see the most common words."
)

# Launch the app
demo.launch(share=True)  # share=True creates a public link
```

## How It Works

1. We define our Python function `analyze_text()` that processes text input
2. We create a Gradio interface with:
   - The function to run (`fn`)
   - Input component (a text box)
   - Output component (text display)
   - Title and description for the interface
3. We launch the interface with `share=True` to generate a public link

When you run this code, Gradio will:
- Start a local web server (typically at http://localhost:7860)
- Generate a temporary public URL (valid for 72 hours)
- Open a browser window with your interface

## Advanced Features

Gradio can do much more:

- Handle multiple inputs and outputs
- Process images, audio, and video
- Create tabs, layouts, and complex UI elements
- Authenticate users with credentials
- Track usage with analytics
- Deploy permanently with Hugging Face Spaces

## Sharing Options

With just one parameter, you can:
- `share=True`: Create a temporary public URL
- `auth=("username", "password")`: Add authentication
- `integrate with Hugging Face Spaces`: For permanent deployment

This makes Gradio perfect for:
- ML model demos
- Research paper accompanying code
- Teaching and education
- Prototype testing
- Team collaboration


