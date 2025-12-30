---
layout: post
title: "Introduction to Python in 6 Lessons - Part 5"
date: 2025-08-21
categories: [python-course, python, tutorial, mini-project]
excerpt: "From essays to tweets, most of the world’s data is text. In this lesson you’ll learn how to clean, count, and analyze words in Python and even save results to a file while building the foundation for real-world text analytics and NLP."
comments: true
order: 5
difficulty: "Beginner"
lesson_title: "Analyze Text – Strings and Basic File Handling"
concepts: "String methods, file I/O, text processing, word counting, data persistence"
duration: "20-25 min"
---

# Analyze Text – Strings and Basic File Handling**

---

## **Tools You’ll Use**

* **Python 3** (Colab, Jupyter, or interpreter)
* **Code editor/IDE** (VS Code, Thonny, PyCharm, or text editor)
* **Sample text files** (or just paste text directly)

---

## **Lesson Roadmap**

1. Why text matters in programming.
2. String basics: storing and manipulating text.
3. Useful string methods: `.lower()`, `.split()`, `.count()`.
4. Plan a word counter: count words, characters, and frequencies.
5. Work with files: reading from and writing to `.txt`.
6. Error handling: what if the file doesn’t exist?
7. Real-world applications: essays, blogs, coding interviews.
8. Recap & quiz.
9. Mini challenge: exclude stopwords, save results neatly.

---

## **Why Strings Matter**

Most of the world’s data is **text** — books, emails, tweets, logs. As a programmer, you’ll often process text: searching for words, cleaning it, or counting it.

A **string** in Python is just text inside quotes:

```python
sentence = "Python is fun!"
```

👉 **Intuition tip:** Think of strings as a **necklace of beads**, where each bead is a character. You can count them, split them into pieces, or rearrange them.

---

## **Step 1: String Basics**

```python
text = "Hello World"

print(text.lower())   # "hello world"
print(text.upper())   # "HELLO WORLD"
print(len(text))      # 11 characters
print(text.split())   # ['Hello', 'World']
print(text.count("o"))  # 2
```

Common string tasks:

* `.lower()` → normalize case (important for comparisons).
* `.split()` → break into words.
* `.count(word)` → count appearances.
* `len()` → count characters.

---

## **Step 2: Plan the Word Counter**

We want to analyze text by:

1. Counting words.
2. Counting characters.
3. Finding the most frequent word.
4. Saving results to a file.

---

## **Step 3: Writing the Code**

```python
text = input("Paste some text: ")

# Convert to lowercase for consistency
text = text.lower()

# Split into words
words = text.split()

# Count total words and characters
word_count = len(words)
char_count = len(text)

# Find most frequent word
freq = {}
for word in words:
    freq[word] = freq.get(word, 0) + 1

most_common = max(freq, key=freq.get)

print("Total words:", word_count)
print("Total characters:", char_count)
print("Most frequent word:", most_common, "(", freq[most_common], "times )")
```

---

## **Step 4: File Handling**

Python can **read** and **write** text files.

### Reading:

```python
with open("sample.txt", "r") as f:
    data = f.read()
    print(data)
```

### Writing:

```python
with open("results.txt", "w") as f:
    f.write("Word count: " + str(word_count))
```

👉 **Tip:** Always use `with open(...)` — it auto-closes files and prevents memory leaks.

---

## **Sample Run**

Input:

```
Data science is fun. Python makes data science easier.
```

Output:

```
Total words: 8
Total characters: 52
Most frequent word: data (2 times)
```

---

## **Common Mistakes & Fixes**

* Forgetting `.lower()` → “Data” and “data” are treated as different words.
* Splitting without cleanup → punctuation like “fun.” stays attached. (You can later use regex for cleaning.)
* File not found → use `try/except` to handle missing files gracefully.

👉 Debugging tip: Print `words[:10]` to quickly see how text was split.

---

## **Real-World Applications**

* Writers checking word count for essays.
* Bloggers analyzing common words in posts.
* Social media analysts finding most-used hashtags.
* Programmers parsing **logs** to detect errors.

This project introduces the **basics of text analytics**, which power advanced fields like **Natural Language Processing (NLP)**.

---

## **Recap of Key Concepts**

* **Strings:** store text data and have useful methods.
* **Counting words/characters:** simple but powerful text analysis.
* **Dictionaries:** used here to track frequencies.
* **File handling:** reading/writing text to store results.

---

## **Review Questions**

1. Why do we convert text to lowercase before counting?
2. What happens if you try to read a file that doesn’t exist?
3. Which data structure is best for counting word frequencies?

---

## **Mini Challenges**

1. **Stopword removal:** Ignore words like “the”, “is”, “and”.
2. **Top 5 words:** Print not just the most common, but the top 5 frequent words.
3. **Save analysis:** Write results (word count, top words) into a new file.
4. **Punctuation cleanup:** Remove `.,!?` before splitting words.
