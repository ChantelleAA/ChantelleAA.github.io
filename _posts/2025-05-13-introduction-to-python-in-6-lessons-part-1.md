---
layout: post
title: "Introduction to Python in 6 Lessons"
date: 2025-05-13
categories: [python, tutorial]
excerpt: ""
---

# Python Lesson 1: Your First Project – A Temperature Converter

Welcome! In this lesson we’ll write a simple Python program to convert temperatures (Fahrenheit to Celsius) while learning core concepts. Python is an **interpreted, high-level, general-purpose** programming language. This means you can write and run Python code line-by-line without a long compile step (interpreted), the code reads almost like English (high-level), and it’s used for everything from web apps to data science (general-purpose). Python’s syntax is designed for readability and simplicity, making it beginner-friendly. For example, the official Python site notes that *“Python can be easy to pick up whether you’re a first time programmer or … experienced”*. In other words, don’t worry if coding is new to you – Python was made to help people start programming gently.

Python can run on your computer or in an online notebook. We’ll use **Google Colab** (a free hosted Jupyter notebook) so you don’t even need to install anything. Colab is a cloud service that “requires no setup” and gives you a friendly environment to write and run Python code. It even provides free computing power. As you’ll see below, you can mix code cells (where you write Python) with text cells (for explanations) – and the interface shows line-by-line execution results in a console view.

## Tools You’ll Use

* **Python 3**: The latest version of Python. We’ll use features like the `input()` and `print()` functions.
* **Google Colab Notebook**: An online editor you open in your web browser. No download needed; just sign in with your Google account.
* **Web Links for Reference**: We’ll include links if you want to explore topics in depth, such as Python documentation or tutorials on data types and input/output.

## Why Build a Temperature Converter?

Building a temperature converter is a fun *first project*. It has a clear goal (convert °F to °C) and uses simple math. In real life, you might use this if you’re a scientist recording weather data or a cook following a recipe from another country. By writing this converter, you’ll learn how to:

* Get **input** from the user (e.g. asking “What’s the temperature in °F?”).
* Store values in **variables**.
* Perform a **calculation** (the conversion formula).
* Display the **output** back to the user (showing the result in °C).

This project gives immediate results: you type a number, the program prints the converted temperature. It’s interactive and motivating for a beginner.

## Understanding Variables

A **variable** in Python is like a labeled box that holds data. Imagine writing your name on a box and putting a number inside – you can later change the contents or label. In code, a variable has a name and stores a value (number, text, etc.). For example, we might use `temp_f` to hold the Fahrenheit temperature. In Python, you simply assign it like `temp_f = 72`. The act of assigning creates the box (variable) and labels it. Unlike some other languages, you don’t have to declare the type; Python figures out that `72` is a number.

👉 **Quick check:** What might happen if we later write `temp_f = "72"` (with quotes around 72)? (Answer: Python would treat it as text, and subtraction on it would cause an error.)

Think of variables as named containers. You can put a different value in `temp_f` later, and the old one is replaced. This is perfect for our converter because each time we run the program it can store a new input. (We’ll see an example soon.)

&#x20;*Figure: A computer screen showing a programming environment (code reflected in glasses). Python code looks like text, and we’ll type code similarly to run our temperature converter.* In the above image, notice the open text editor with code. Python lets you write instructions (like boxes of data).

## Getting Input and Output

To make our program interactive, we’ll use `input()` to **ask the user** for a number and `print()` to **show the result**. In Python, the `input()` function displays a prompt and returns what the user types as a **string** (text). For example:

```python
user_input = input("Enter temperature in °F: ")
```

This line will pause the program and show the message. If the user types `100` and presses Enter, `user_input` will be `"100"` (a string!). You’ll often convert this to a number (with `int()` or `float()`) before doing math.

The `print()` function then shows values on the screen. It can print text and numbers together. For instance:

```python
print("Converted to °C:", temp_c)
```

will display something like: `Converted to °C: 37.78`. In short, **input and output** let your program talk to the user. As one tutorial notes, *“the input() function enables interaction with users by gathering input during program execution,”* and `print()` displays the output.

Here’s an example of how it works in a session:

```plaintext
Enter temperature in °F: 100
The temperature in °C is: 37.78
```

(That output means the user typed `100` and the program printed the result.)

![image1](https://sdmntpritalynorth.oaiusercontent.com/files/00000000-821c-6246-a15c-c33887398d27/raw?se=2025-05-15T08%3A44%3A15Z&sp=r&sv=2024-08-04&sr=b&scid=00000000-0000-0000-0000-000000000000&skoid=b928fb90-500a-412f-a661-1ece57a7c318&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-05-15T05%3A46%3A12Z&ske=2025-05-16T05%3A46%3A12Z&sks=b&skv=2024-08-04&sig=h4MR/s1vl1EkV9zfhd9Q4r8EGHlZapnVESe81LfBJXs%3D)
*Figure: A young programmer writing Python code on a computer. You’ll type code and see results on your screen as shown*
This image shows someone coding at a desk. You’ll do the same in Colab or any Python editor.

## Planning with a Flowchart

Before coding, it often helps to sketch a **flowchart** of what the program will do. This is a simple diagram of steps:

![image2](https://sdmntpritalynorth.oaiusercontent.com/files/00000000-a2e4-6246-95f6-b3dbeef6f9c5/raw?se=2025-05-15T08%3A47%3A01Z&sp=r&sv=2024-08-04&sr=b&scid=00000000-0000-0000-0000-000000000000&skoid=b928fb90-500a-412f-a661-1ece57a7c318&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-05-15T04%3A59%3A06Z&ske=2025-05-16T04%3A59%3A06Z&sks=b&skv=2024-08-04&sig=G5mxx6nku/QHMghftXHWM51W/n5RYCZLm2xf3bRxxfk%3D)*Figure: Drawing a flowchart on a whiteboard, illustrating program logic as input ➔ process ➔ output.*

1. **Input**: Read the Fahrenheit temperature from the user.
2. **Process**: Convert it to Celsius using the formula:

   $$
   \text{Celsius} = (\text{Fahrenheit} - 32) \times \tfrac{5}{9}.
   $$
3. **Output**: Display the Celsius temperature.

This flowchart (above) shows boxes for each step. The left box is **Input**, the middle is **Process**, and the right is **Output**. Arrows show the flow: you start with the input value, apply the conversion, then show the result. Drawing this isn’t required, but it helps to think through the steps before writing code.

## Writing the Code

Now let’s turn the plan into Python code. Open a new Colab notebook and add a code cell. We’ll write lines one by one, with comments and explanation:

```python
# 1. Get user input for Fahrenheit temperature:
temp_f = float(input("Enter temperature in °F: "))

# 2. Convert to Celsius:
temp_c = (temp_f - 32) * 5/9

# 3. Output the result:
print("Temperature in °C is:", temp_c)
```

* The first line uses `input()` to ask **Enter temperature in °F:**. We wrap `input(...)` inside `float()` to convert the entered text into a number (since input returns a string). Now `temp_f` is a numeric value we can do math with.
* The second line applies the formula. We subtract 32, multiply by 5, then divide by 9. This follows the standard conversion.
* The third line prints the result in a friendly message.

Run this cell. When prompted, type a number (like `100`) and press Enter. You should see the program output something like:

```plaintext
Temperature in °C is: 37.77777777777778
```

That long decimal is okay, but we can format it later if needed. You’ve just written and executed your first Python program! 🎉

👉 **Quick check:** Try running the program with different inputs. What result do you expect if you enter `32`? (Hint: 32°F should be 0°C.)

## Common Errors (and How to Fix Them)

Every beginner makes mistakes – it’s totally normal! Let’s look at a few errors you might see, and how to fix them.

* **Type Error (String vs Number):** If you forget `float()`, your code would be:

  ```python
  temp_f = input("Enter temperature in °F: ")
  temp_c = (temp_f - 32) * 5/9
  ```

  This causes an error because `temp_f` is a string and you can’t subtract 32 (an integer) from it. The program might crash with a message like:

  ```plaintext
  TypeError: unsupported operand type(s) for -: 'str' and 'int'
  ```

  To fix this, **convert** the input to a number (as shown above).

* **Syntax Error:** Missing a parenthesis or colon can cause a `SyntaxError`. For example:

  ```python
  print "Hello"
  ```

  (in Python 3, this needs parentheses: `print("Hello")`). Always check spelling and that parentheses match. The error message will point out something like “SyntaxError: invalid syntax” and underline the problem part.

* **Name Error:** If you try to use a variable that doesn’t exist or is misspelled, Python says something like:

  ```plaintext
  NameError: name 'tempc' is not defined
  ```

  (Note: `tempc` vs `temp_c` are different names.) The fix is to double-check variable names for typos.

* **Indentation Error:** Python uses spaces/tabs for structure. For this simple script we didn’t use extra blocks, but if you indent wrong (especially inside loops or `if` statements), you’ll get an IndentationError. The fix: align code correctly (each block should be indented the same amount).

&#x20;*Figure: A programmer frowning at code on his laptop, demonstrating common frustration from errors. Don’t worry – errors happen to everyone, and they help you learn!*

Whenever you see an error, read the message carefully. It usually tells you **what** went wrong and **where** (it will show a line number). Use that clue to fix your code. If you’re stuck, ask a friend or look up the error – Google is very good at explaining error messages!

## External Resources

* **What is Python?** The official “About” page and FAQ explain Python’s features: [python.org/about](https://www.python.org/about/) (it even promises “friendly & easy to learn”).
* **Python Data Types:** Learn about numbers, text (strings), and converting input: [W3Schools – Python Data Types](https://www.w3schools.com/python/python_datatypes.asp).
* **Input/Output in Python:** For deeper reading on `input()` and `print()`, see [GeeksforGeeks – Python Input/Output](https://www.geeksforgeeks.org/input-and-output-in-python/) or [W3Schools – Python Input](https://www.w3schools.com/python/python_user_input.asp) (notes that `input()` always returns a string).
* **Python Tutorial:** If you want a broader overview, the [official Python tutorial](https://docs.python.org/3/tutorial/) is a great reference once you’re more comfortable.

Each of these links dives deeper into the topics we’ve touched on. Don’t worry if you don’t read them all now – they’re here for when you want to explore further.

## Recap

* **Python** is an interpreted, high-level language (easy to write and read). It’s beginner-friendly and widely used.
* We used **variables** (`temp_f`, `temp_c`) to store values. Think of them as labeled boxes for data.
* We gathered **input** with `input()` (remember it returns a string by default), and showed **output** with `print()`.
* Our **temperature converter** program took a Fahrenheit value, applied the conversion formula, and printed the Celsius result.
* We sketched a **flowchart** to plan our steps: Input ➔ Process (convert) ➔ Output. Drawing it helped organize our thoughts.
* We saw some **common errors**: string vs number mistakes, syntax typos, etc. These errors are normal – read the message and fix the code!

Great job on finishing your first Python lesson. You now have a working program and have learned key ideas about programming. 🎉

## Mini-Challenge

Try to extend your temperature converter:

* Modify the program so it **asks for Celsius and converts to Fahrenheit**. (Hint: formula is `F = C * 9/5 + 32`.)
* Add extra output, e.g. after converting to °C, also print the value in **Kelvin** (K = C + 273.15).
* Format the output to round to 2 decimal places: use Python’s [`round()`](https://www.w3schools.com/python/ref_func_round.asp) function or f-strings (f"For example: `{round(temp_c, 2)}`").

These mini-tasks reinforce what you’ve learned. Experiment and see what happens – that’s a big part of learning to code!

## What’s Next?

* **Lesson 2 Preview:** We’ll dive deeper into data types and **more practice with variables**. You’ll learn about integers vs. floats (whole numbers vs. decimals), and how to do simple math and string operations in Python.
* **Roadmap:** Up next, we’ll cover conditional logic (making decisions with `if`), loops, and writing our own functions. Each lesson builds on the last, using projects to keep things exciting.

Keep up the great work! Remember, every programmer started with first steps like these. You’re on your way to creating even cooler projects. 🙌
