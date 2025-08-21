---
layout: post
title: "Introduction to Python in 6 Lessons - Part 2"
date: 2025-05-13
categories: [python, tutorial, mini-project]
excerpt: "In this second lesson of our Python beginner series, we’ll build a simple calculator that performs basic arithmetic: addition, subtraction, multiplication, and division. This hands-on project introduces two powerful tools in Python: conditional statements (if, elif, else) and functions."
comments: true
---

# Create a Simple Calculator – Learn Conditionals and Functions

> **Tools You’ll Use:**
>
> * **Python 3** (we recommend Google Colab or any Python interpreter)
> * **Code editor/IDE** (such as VS Code, Thonny, or even a simple text editor)
> * **Web browser** (for documentation and debugging)

## Lesson Roadmap

* **Review conditionals:** Learn `if`, `elif`, and `else` statements.
* **Plan the calculator:** Decide which operations to support and how to handle input.
* **Define functions:** Write `def`-based functions for add, subtract, multiply, divide.
* **Write the code:** Use `if`/`elif` to call the right function based on user input.
* **Test the program:** Try different numbers and operators (including edge cases).
* **Recap & Quiz:** Summarize key ideas and answer a small quiz.
* **Mini challenge:** Extend the program (see the challenge at the end).

A simple calculator program can help solve everyday problems like *budgeting expenses or checking homework calculations*.  For example, creating a personal budget involves lots of addition and subtraction to track spending – using a calculator program can make this easier. As one budgeting guide notes, planning a budget helps manage your financial responsibilities (like rent and bills) and prepares you for financial success. In this lesson we’ll simulate a calculator in Python, reinforcing those real-world math skills.

&#x20;*Figure: A calculator helps with tasks like budgeting or homework problems.*

In this project, our program will ask the user for two numbers and an operator (`+`, `-`, `*`, or `/`), then compute the result.  We’ll use **conditional statements** (`if`, `elif`, `else`) to choose the operation and **functions** to organize the code. Let’s begin by understanding how conditionals work in Python.

## Using Conditional Statements (`if`, `elif`, `else`)

A **conditional statement** lets the program choose between actions. In Python, an `if` statement runs a block of code only when its condition is true.  For example:

```python
if x > 0:
    print("Positive number")
```

Here, `print` only happens if `x > 0`; otherwise it’s skipped. Python uses indentation (spaces) to mark these blocks. It’s easy to make an error by forgetting to indent the code under the `if`. For example, this wrong code causes an error:

```python
if x != 0:
total += x  # <=== ERROR: no indent under if
print(total)
```

Because the `print` line is not indented, Python thinks the `if` has an empty body and will raise an error. Always indent the block under `if` (4 spaces is standard):

```python
if x != 0:
    total += x
    print(total)
```

When you have multiple choices, Python lets you chain `if` with `elif` (else-if) and an optional `else`. The `elif` keyword is Python’s way of saying “if the previous conditions were not true, then try this next condition”.  And `else` will catch anything not caught by the earlier tests. In other words:

* Check the first `if` condition: if **true**, run its block and skip the rest.
* Otherwise check the next `elif` condition: if **true**, run that block.
* If none of the `if`/`elif` conditions match, go to the `else` block (if provided).

For example, an `if`/`elif`/`else` for three-way choice:

```python
if number > 0:
    print("Positive number")
elif number < 0:
    print("Negative number")
else:
    print("Zero")
```

Here only one branch runs: if the first condition is false, Python checks the `elif`; if that’s also false, it runs the `else` block.

&#x20;*Figure: Flowchart of an `if`/`else` decision.  If the test is true, the left branch executes; if false, the right branch executes.*

Let’s see this in our calculator: we’ll ask the user for an operator and use `if`/`elif` to pick the right function. A sample snippet might look like:

```python
if operator == "+":
    result = add(x, y)
elif operator == "-":
    result = subtract(x, y)
elif operator == "*":
    result = multiply(x, y)
elif operator == "/":
    result = divide(x, y)
else:
    print("Invalid operator")
```

In this code, exactly one block executes for each input. If none of the four conditions match (e.g. the user types something else), the `else` block catches it and prints an error message. (If we omitted the `else`, the program would simply do nothing for an unrecognized operator.)

* **Common mistakes:** Make sure you use `==` (equality) in the `if` conditions, not `=` (assignment). Also double-check indentation for every block. Forgetting an `elif` or `else` can lead to unexpected behavior (the program might skip all blocks if none match). And remember: after an `if` or `elif` line, you **must** indent the next lines; otherwise Python will error out.

You can learn more about Python’s `if`/`elif`/`else` syntax in beginner tutorials (see [W3Schools: Python Conditions](https://www.w3schools.com/python/python_conditions.asp) or [Programiz: If-Else Examples](https://www.programiz.com/python-programming/if-elif-else)).

**Quiz:** What happens if the user enters an operator that we don’t handle (for example, `^` or `%`)?

* (a) The program crashes.
* (b) The program skips all the `if`/`elif` checks and runs the `else` block, printing something like *“Invalid operator”*.
* (c) The program adds the numbers by default.

*Answer:* It goes to the `else` clause and prints the invalid operator message (assuming we’ve written an `else` branch to handle it). If we had no `else`, it would simply do nothing for that case.

## Defining and Calling Functions in Python

To keep our code organized, we’ll use **functions** for each math operation. A function is “a block of code that performs a specific task”.  Functions let us break a problem into smaller chunks that are easy to understand and reuse. In Python, you define a function with the `def` keyword and then call it by name.

For example, to define a function that adds two numbers:

```python
def add(a, b):
    return a + b
```

Here `add` is our function name, `a` and `b` are parameters, and `return a + b` gives back the result. According to documentation, *“a function is a block of code which only runs when it is called”*. We must **call** it to use it:

```python
result = add(3, 5)   # Calls the add function with a=3, b=5
print(result)        # Prints: 8
```

(Note: defining a function by itself does nothing until you call it.)

We’ll similarly define `subtract`, `multiply`, and `divide`:

```python
def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    return a / b   # note: will crash if b is 0!
```

By organizing operations into functions, our code is cleaner and each function does one job.  As W3Schools shows, you define functions with `def` and later call them by name. This means our main code can simply invoke `add(x, y)`, etc., instead of repeating the logic inline. It also makes it easy to test each function separately. (For example, you can check `add(2,2)` in the Python shell to make sure it returns 4.)

For more on functions, see [Programiz: Python Functions](https://www.programiz.com/python-programming/function) or [W3Schools: Python Functions](https://www.w3schools.com/python/python_functions.asp).

## Putting It All Together: Simple Calculator Code

Now let’s write the complete calculator program step by step:

```python
# 1. Define functions for each operation
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    return x / y   # beware division by zero!

# 2. Get input from the user
num1 = float(input("Enter first number: "))
operator = input("Enter operator (+, -, *, /): ")
num2 = float(input("Enter second number: "))

# 3. Use conditionals to decide which operation to perform
if operator == "+":
    result = add(num1, num2)
elif operator == "-":
    result = subtract(num1, num2)
elif operator == "*":
    result = multiply(num1, num2)
elif operator == "/":
    result = divide(num1, num2)
else:
    result = None
    print("Invalid operator. Please use +, -, * or /.")

# 4. Print the result if valid
if result is not None:
    print("Result:", result)
```

**How this works:** We define four small functions at the top. Then we read two numbers and the desired operator from the user. The chain of `if`/`elif` checks matches the operator string. If it’s `"+"`, we call `add(num1, num2)`, etc. The chosen function returns the answer, which we store in `result`. Finally, we print the result.

**Sample Runs:**

* **Example 1:**

  ```
  Enter first number: 6
  Enter operator (+, -, *, /): *
  Enter second number: 7
  Result: 42.0
  ```

  The program multiplies 6 by 7 and prints 42.0.

* **Example 2 (invalid operator):**

  ```
  Enter first number: 5
  Enter operator (+, -, *, /): x
  Enter second number: 2
  Invalid operator. Please use +, -, * or /.
  ```

  Since `x` is not recognized, the program runs the `else` block and prints an error message.

* **Example 3 (division by zero):**

  ```
  Enter first number: 8
  Enter operator (+, -, *, /): /
  Enter second number: 0
  ZeroDivisionError: division by zero
  ```

  (In our current code, dividing by zero causes a crash. We could improve this by adding a check `if num2 == 0` before calling `divide`. Handling such edge cases is part of good programming practice.)

**Common beginner mistakes in this code:**

* **Indentation errors:** Every `if` and `elif` line must have its block indented. Forgetting to indent will cause an error.
* **Using `=` instead of `==`:** In the `if operator == "+"` line, make sure to use the double equals (`==`). A single `=` would try to assign, which is a syntax error in this context.
* **String vs number:** We convert inputs to `float` so that arithmetic works. If you accidentally keep them as strings, `add(num1, num2)` might concatenate instead of summing.
* **Not calling functions:** After defining a function (with `def`), remember to call it. Simply writing `add` (without parentheses) won’t do anything.
* **Division by zero:** In our `divide` function we use `/`. If the user enters 0 as the second number, Python will raise `ZeroDivisionError`. You can handle this by checking `if num2 == 0` before dividing.

By the end of this code, our calculator can perform the four basic operations. We used **conditional statements** to route the logic and **functions** to keep the operations tidy.

## Real-World Applications

Building a calculator is more than an exercise in code; it mirrors tasks we do in daily life. For instance, **budgeting** involves repeatedly adding income and subtracting expenses. Using a programmatic calculator could automate this process. According to financial advice, “creating a budget helps you manage your financial responsibilities… and prepares you for financial success”. Our simple calculator is a step toward such practical tools.

In an educational setting, students often use calculators to verify their math homework. Writing your own calculator program reinforces how those calculations work under the hood. Every time you type numbers and see the result, you’re practicing the same addition, subtraction, multiplication, and division operations you’d learn in school.

## Recap of Key Concepts

* **Conditional statements (`if`/`elif`/`else`):**  We use these to *make decisions* in code. An `if` block runs only if its condition is true. You can chain `elif` and use `else` for any other case.
* **Functions:** We define functions with `def` to perform a specific task. The code inside a function only runs when we **call** the function. Functions help organize and reuse code.
* **Sample calculator code:** We wrote a program that reads two numbers and an operator, then uses an `if`/`elif` chain to call the correct function and print the result. This demonstrated getting user input, branching logic, and function calls.
* **Error handling:** We saw what happens with invalid operators or division by zero. It’s important to think about and handle such edge cases (for example, printing an error message or using `try/except`).
* **Real-world uses:** This project ties into real tasks like budgeting or homework calculations. Writing a calculator is a good practice project because it’s simple yet covers many basic programming concepts.

**Review Questions:**

* What does the `elif` keyword do in Python? (Answer: It checks another condition if the previous `if` was false.)
* How do you define a function that returns a value? (Answer: Start with `def`, give it a name and parameters, and use `return` inside.)
* What will our calculator program do if the user enters `/` and the second number is `0`? (Answer: It will crash with a `ZeroDivisionError`, unless we add code to catch or check for that.)

## Mini Challenge

**Try extending the calculator:**

* **Add exponentiation:** Handle an operator like `^` or `**` to raise the first number to the power of the second (you can use `x ** y` in Python).
* **Handle division by zero:** Modify the code so that if the operator is `/` and the second number is 0, it prints an error message instead of crashing. (Hint: check `if num2 == 0:` before dividing.)

These extensions will deepen your understanding of both conditionals and error checking.

Great work completing Lesson 2! Now you know how to use `if`/`elif`/`else` to control program flow and how to define and call functions in Python. Keep experimenting with your calculator and think about other features you could add.

**Sources:** Basic Python conditional and function usage are explained in tutorials like Programiz and W3Schools. Budgeting importance is discussed in the SNHU educational blog. These provide beginner-friendly details on the concepts we used.
