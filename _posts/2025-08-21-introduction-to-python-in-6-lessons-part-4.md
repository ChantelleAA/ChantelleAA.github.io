---
layout: post
title: "Introduction to Python in 6 Lessons - Part 4"
date: 2025-08-21
categories: [python, tutorial, mini-project]
excerpt: ""
---

# Manage a To-Do List – Lists and Basic Data Structures

## **Tools You’ll Use**

* **Python 3** (Google Colab, Jupyter Notebook, or local interpreter)
* **Code editor/IDE** (VS Code, Thonny, PyCharm, or text editor)
* **Web browser** (for checking docs & debugging help)

---

## **Lesson Roadmap**

1. Review: Why we need data structures.
2. Learn lists: what they are and how they store multiple values.
3. Build a simple to-do list manager with options to add, view, and remove tasks.
4. Practice looping through lists to display tasks.
5. Handle invalid input and empty lists.
6. Real-world tie-ins: using code to organize your life.
7. Recap & Quiz.
8. Mini challenge: extend the app with “mark as done” and sorting.

---

## **Why Lists Matter**

In the calculator and guessing game, we stored only a few numbers at a time. But what if you need to track **many values**: shopping items, homework tasks, or quiz questions?

A **list** is like a **container** (a basket or shelf) that can hold multiple items at once. You don’t need 10 separate variables (`task1`, `task2`, …). You just make one list:

```python
tasks = ["Buy milk", "Finish assignment", "Call friend"]
```

Python remembers the order and lets you add, remove, and loop through items.

👉 **Intuition tip:** Think of a list as a numbered shelf where each slot has a label (index).

* `tasks[0]` → first item: "Buy milk"
* `tasks[1]` → second item: "Finish assignment"

---

## **Step 1: Creating and Modifying Lists**

```python
tasks = []   # start with an empty list

# Add items
tasks.append("Read Python notes")
tasks.append("Do laundry")
print(tasks)   # ['Read Python notes', 'Do laundry']

# Remove an item
tasks.remove("Do laundry")
print(tasks)   # ['Read Python notes']
```

Tips:

* Use `.append(item)` to add new tasks.
* Use `.remove(item)` to delete a specific one.
* Use `len(tasks)` to check how many tasks are left.

---

## **Step 2: Planning the To-Do List App**

The program will:

1. Show a menu with choices (Add / View / Remove / Exit).
2. Let the user pick an action.
3. Perform the action and loop back to the menu.
4. Continue until the user chooses Exit.

---

## **Step 3: Writing the Code**

```python
tasks = []

print("Welcome to your To-Do List Manager!")

while True:
    print("\nMenu:")
    print("1. Add a task")
    print("2. View tasks")
    print("3. Remove a task")
    print("4. Exit")

    choice = input("Choose an option (1-4): ")

    if choice == "1":
        task = input("Enter a new task: ")
        tasks.append(task)
        print(f"'{task}' added to your list.")

    elif choice == "2":
        if len(tasks) == 0:
            print("No tasks yet!")
        else:
            print("Your tasks:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")

    elif choice == "3":
        if len(tasks) == 0:
            print("No tasks to remove.")
        else:
            print("Select a task number to remove:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
            index = int(input("Task number: ")) - 1
            if 0 <= index < len(tasks):
                removed = tasks.pop(index)
                print(f"Removed '{removed}'")
            else:
                print("Invalid number.")

    elif choice == "4":
        print("Goodbye! 👋")
        break

    else:
        print("Invalid choice. Please enter 1-4.")
```

---

## **Sample Run**

```
Welcome to your To-Do List Manager!

Menu:
1. Add a task
2. View tasks
3. Remove a task
4. Exit
Choose an option (1-4): 1
Enter a new task: Finish homework
'Finish homework' added to your list.

Menu:
1. Add a task
2. View tasks
3. Remove a task
4. Exit
Choose an option (1-4): 2
Your tasks:
1. Finish homework
```

---

## **Common Mistakes & Fixes**

* Forgetting `.append()` → assigning directly (`tasks = task`) replaces the whole list.
* Using wrong index in `.pop()` (remember lists start at 0).
* Removing an item that doesn’t exist causes an error. Always check with `if len(tasks) > 0:`.
* Infinite loop: forgetting the `break` when user exits.

👉 Debugging tip: Print the list after each action to check what’s inside.

---

## **Real-World Applications**

This small app mirrors real productivity tools (like Trello or Google Tasks). Managing lists of items is central to:

* Task managers.
* Shopping apps.
* School grading systems (list of students, scores).

Once you master lists, you’re on your way to handling larger data structures like **tables, databases, and JSON**.

---

## **Recap of Key Concepts**

* **Lists** store multiple items in one variable.
* `.append()` adds to a list; `.remove()` or `.pop()` removes.
* `len()` counts items.
* Loops (`for i, task in enumerate(tasks)`) let you process each item.
* Menu-driven programs use `while True` loops to repeat until Exit.

---

## **Review Questions**

1. What does `tasks.append("New Task")` do?
2. Why do lists start at index 0 in Python?
3. What happens if you try to `.pop()` from an empty list?

---

## **Mini Challenges**

1. **Mark as Done:** Add an option to mark a task complete (e.g., add ✅ after it).
2. **Sorting:** Add an option to sort tasks alphabetically with `tasks.sort()`.
3. **Save to File:** Save tasks to a text file so they remain after closing the program.
4. **Deadlines:** Let users add a due date (e.g., store tasks as `["Finish homework - Due Monday"]`).
