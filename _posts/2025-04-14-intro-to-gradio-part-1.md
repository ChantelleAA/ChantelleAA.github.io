---
layout: post
title: "Gradio Part 1: Introduction to Gradio (How to easily deploy functions or ML models in Python)"
date: 2025-04-14
categories: [intro, tutorials]
excerpt: "Gradio is a Python library that allows you to quickly create customizable web interfaces for your machine learning models, data analyses, or any Python function."
comments: true
---

# Gradio: The best way to share your Python Code, ML Model or Function with others

Have you ever written a really cool function or built a machine learning model that you wish others could test out easily without having to share your entire codebase or set up a complex deployment system?

Enter **Gradio**, an amazing Python library that lets you turn your Python functions into fully interactive web applications **in just a few lines of code**. Whether you're building a model demo, a utility tool, or just something fun, Gradio helps you create and share your work effortlessly.

What makes it truly special is this: Not only can you launch your app locally on your machine, but Gradio also gives you a **public link**, so **anyone from anywhere** can try your app, even if they don’t have Python installed. It’s like sharing your code, but without the headache of packaging or deploying it manually.

Let’s look at how simple and powerful it is by building and deploying a tiny app together.


## Scenario: You Built a Fun Text Function

Imagine you’ve written a small function that turns English sentences into **Pig Latin**, a playful coded version of English often used as a language game.

```python
def to_pig_latin(text):
    words = text.split()
    translated = []
    for word in words:
        if word[0] in 'aeiouAEIOU':
            translated.append(word + 'way')
        else:
            translated.append(word[1:] + word[0] + 'ay')
    return ' '.join(translated)
```

This function splits the input sentence into words and applies simple Pig Latin rules. Now let’s build an interactive interface for it using Gradio.



## Step-by-Step: Deploying with Gradio

```python
import gradio as gr

demo = gr.Interface(
    fn=to_pig_latin,
    inputs=gr.Textbox(lines=2, placeholder="Enter English text here..."),
    outputs=gr.Textbox(label="Pig Latin Translation"),
    title="Pig Latin Translator",
    description="Try out this fun Pig Latin translator! Type in any English sentence and watch it transform."
)

demo.launch()
```

Let’s break this down so you fully understand what’s going on:

### 1. `import gradio as gr`
This imports the Gradio library. The `gr` alias is just a shorthand so you can write `gr.Interface()` instead of `gradio.Interface()` every time.

### 2. `gr.Interface(...)`
This is the core component in Gradio. It wraps your function into a ready-to-use interface.

**Parameters:**
- `fn=to_pig_latin`: This tells Gradio which function you want to wrap. In our case, it's `to_pig_latin`, the Pig Latin converter.
- `inputs=gr.Textbox(...)`: This defines what kind of input your app will take from the user. Here, we're using a multiline textbox for the user to type their English sentence.
  - `lines=2`: Sets the textbox to show 2 lines by default.
  - `placeholder`: A hint inside the textbox before anything is typed.
- `outputs=gr.Textbox(...)`: This specifies what the function returns. We're using another textbox to show the translated result.
  - `label`: Adds a label above the output box so users know what they're looking at.
- `title`: The big, bold heading shown at the top of the app.
- `description`: A short helpful sentence shown under the title, explaining what your app does.

### 3. `demo.launch()`
This launches the app. By default, Gradio runs it on your local server and also provides a **public shareable link** (using [ngrok](https://ngrok.com)) so others can access your app remotely, even on their phone.


## Why I love Gradio?

- **Zero setup for UI**: You don't need to write HTML or use frameworks like React or Flask.
- **Share instantly**: Within seconds, you can get a public URL that you can share with colleagues, friends, or clients.
- **Perfect for demos**: Whether it’s a deep learning model or a simple function, Gradio helps you create polished, interactive demos.
- **Works with models and pipelines**: It supports anything from basic functions to complex models like those from Hugging Face Transformers.


