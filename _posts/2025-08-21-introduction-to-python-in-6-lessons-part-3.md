---
layout: post
title: "Introduction to Python in 6 Lessons - Part 3"
date: 2025-08-21
categories: [python-course, python, tutorial, mini-project]
excerpt: "Turn Python into a game partner! In this lesson, you’ll build a fun Guess-the-Number game and learn how loops, randomness, and logic make your code think and respond."
comments: true
order: 3
difficulty: "Beginner"
lesson_title: "Build a Guess-the-Number Game – Loops and Randomness"
concepts: "While loops, random module, comparison operators, control flow"
duration: "20-25 min"
---

# Build a Guess-the-Number Game – Loops and Randomness

## **Tools You’ll Use**

* **Python 3** (Google Colab, Jupyter Notebook, or any Python interpreter)
* **Code editor/IDE** (VS Code, Thonny, PyCharm, or even a text editor)
* **Web browser** (for documentation and debugging help)

---

## **Lesson Roadmap**

1. Review loops: why repetition is important in programming.
2. Generate random numbers with Python’s `random` module.
3. Plan the game: input, feedback, winning condition.
4. Write the code: loop until correct.
5. Add features: attempt counter, hints, quit option.
6. Test with different runs and edge cases.
7. Recap key ideas with a quiz.
8. Mini challenge: difficulty levels & scoreboard.

---

## **Why Loops Matter**

When we wrote the calculator in Lesson 2, the program ran **once** and ended. But in many programs, we want repetition:

* Try again until successful login.
* Keep asking until the user gives valid input.
* Run through all items in a list.

This is where **loops** come in. Think of loops as **“automatic patience”**: instead of us retyping the same code, Python runs it for us repeatedly until the job is done.

---

## **Types of Loops in Python**

1. **`while` loop** → repeat **as long as a condition is true**.

   ```python
   count = 1
   while count <= 5:
       print("Attempt:", count)
       count += 1
   ```

   (This runs 5 times because the condition stops when `count > 5`.)

2. **`for` loop** → repeat over a fixed collection (like a list or range).

   ```python
   for i in range(5):
       print("Attempt:", i)
   ```

   (This runs 5 times automatically, from 0 to 4.)

👉 In our game, we’ll use a **while loop** because we don’t know in advance how many guesses the player will need.

---

## **Step 1: Random Numbers in Python**

A game needs **unpredictability**. If the secret number were always the same, it would be boring. Python’s `random` module solves this:

```python
import random
number = random.randint(1, 100)   # random number between 1 and 100
print(number)   # test: see what number is picked
```

Each run gives a different number. (If you keep getting the same number, check that you’re not hardcoding it.)

---

## **Step 2: Plan the Game**

Game rules:

1. Computer picks a number between 1 and 100.
2. User guesses until correct.
3. After each guess:

   * Too low → tell them “Try a bigger number”.
   * Too high → tell them “Try a smaller number”.
   * Correct → congratulate them and show attempts.

**Flowchart:**

```
Pick random number → Ask for guess → Compare → Feedback
          ↑                                   ↓
          └────────── loop until correct ─────┘
```

---

## **Step 3: First Version of the Code**

```python
import random

secret_number = random.randint(1, 100)

print("Welcome to Guess the Number!")
print("I'm thinking of a number between 1 and 100.")

guess = None
attempts = 0

while guess != secret_number:
    guess = int(input("Enter your guess: "))
    attempts += 1

    if guess < secret_number:
        print("Too low! Try again.")
    elif guess > secret_number:
        print("Too high! Try again.")
    else:
        print(f"🎉 Congratulations! You guessed it in {attempts} tries.")
```

---

## **Step 4: Thinking Like a Programmer**

* The variable `attempts` is our **memory** of how many guesses were made.
* The loop’s condition `while guess != secret_number` ensures the game keeps running **until success**.
* Feedback (`if/elif/else`) helps the user narrow down the possibilities — this is **binary search thinking**: cut the search space in half each time.

👉 Intuition tip: If the number is between 1 and 100, a clever player can always guess it in at most **7 tries** by halving the range each time (like guessing 50 first, then 25 or 75, etc.).

---

## **Sample Runs**

**Example 1:**

```
Welcome to Guess the Number!
I'm thinking of a number between 1 and 100.
Enter your guess: 50
Too high! Try again.
Enter your guess: 25
Too low! Try again.
Enter your guess: 35
🎉 Congratulations! You guessed it in 3 tries.
```

**Example 2 (lucky guess):**

```
Enter your guess: 72
🎉 Congratulations! You guessed it in 1 try.
```

---

## **Common Mistakes & Debugging Tips**

* **Forgetting int() conversion:** `input()` always returns a string → `if guess < secret_number` will crash unless you convert it.
* **Infinite loop:** If you forget to update `guess` inside the loop, it runs forever.
* **Hardcoded number:** If you set `secret_number = 50` for testing but forget to remove it, the game is no longer random.
* **Edge case:** What if the user enters text instead of a number? (The program crashes. You can fix this later with `try/except`.)

**Debugging tip:** Use `print(secret_number)` during testing to see the hidden answer. Remove it when finished.

---

## **Step 5: Adding Features**

Let’s add more polish:

### 1. Limit attempts (Hard mode)

```python
max_attempts = 5

while guess != secret_number and attempts < max_attempts:
    # guessing logic as before...
```

At the end, check if they ran out of attempts:

```python
if guess != secret_number:
    print("Game over! The number was", secret_number)
```

### 2. Allow quitting

```python
user_input = input("Enter your guess (or 'q' to quit): ")

if user_input.lower() == 'q':
    print("You gave up! The number was", secret_number)
    break
```

### 3. Smarter feedback (difference-based)

```python
if abs(guess - secret_number) <= 5:
    print("Very close!")
```

---

## **Real-World Applications**

This game models **trial-and-error with feedback**, just like in real life:

* Teachers giving hints on homework (“too big, try smaller”).
* Login systems giving limited attempts before lockout.
* Scientific experiments narrowing down hypotheses.

It shows why programming is useful: computers can patiently **repeat checks thousands of times**, while humans might give up.

---

## **Recap of Key Concepts**

* **Loops:** `while` keeps running until the condition is false.
* **Randomness:** `random.randint()` makes programs less predictable.
* **Control flow:** Feedback (`if/elif/else`) inside loops guides user interaction.
* **Counters:** Track attempts to measure performance.

---

## **Review Questions**

1. Why do we use a `while` loop instead of a `for` loop here?
2. What happens if you forget to increment `attempts`?
3. How many guesses do you need at most to find a number between 1 and 100 if you play optimally?

---

## **Mini Challenges**

1. **Difficulty levels**

   * Easy = unlimited guesses
   * Medium = 10 guesses
   * Hard = 5 guesses
     (Use `if` statements to set `max_attempts`.)

2. **Leaderboard**
   Track the fewest attempts across multiple rounds.

3. **Range selection**
   Let the player choose the range (1–50, 1–500, etc.).

4. **Hint system**
   After 3 wrong guesses, give a clue: “The number is divisible by 2” or “The number is greater than 50”.
*draft the worked-out code for Mini Challenge 1 (Difficulty Levels)** so your students see a full extension project, like we did with the calculator lesson’s exponentiation challenge?

