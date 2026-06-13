# Quiz

## Topic List

1. [**Basics of Python**](#basics-of-python)
2. [**Syntax**]()
3. [**Output**]()
4. [**Comments**]()
5. [**Variables and Data Types**]()
    1. [**Numbers**]()
    2. [**Strings**]()
    3. [**Booleans**]()
6. [**Operators**]()
7. [**Type Casting**]()
8. [**Grouped Data**]()
    1. [**Lists**]()
    2. [**Tuples**]()
    3. [**Sets**]()
    4. [**Key-Value Pairs (Dictionaries)**]()
9. [**Conditionals**]()
    1. [**If-Else**]()
    2. [**Match (Switch Case)**]()
10. [**Loops**]()
    1. [**For Loops**]()
    2. [**While Loops**]()
11. [**Ranges**]()
12. [**Arrays**]()
13. [**Iterators**]()
14. [**Modules (Packages)**]()

---

## Basics of Python

- Python was created by **Guido van Rossum**.
- It was first released in **1991**.
- The current release of Python is **3.14.6** as of **10 June 2026**.
- Official website: **https://www.python.org/**

<ins><b>Applications of Python:</b></ins>

- Server-side web app development,
- Workflow development using scripts,
- Database and fle management systems,
- Handle big data and perform complex mathematics,
- Rapid prototyping and production-ready software development.

<ins><b>Characteristics of Python:</b></ins>

- Works on **Windows**, **Mac**, **Linux**, and **Raspberry Pi**.
- Runs on an interpreter system, meaning that code can be executed as soon as it is written.
- Useful for quick prototyping.
- Relies on indentation, using whitespace, to define scope; such as the scope of _loops_, _functions_ and _classes_. Other programming languages often use curly-brackets for this purpose.

<ins><b>Advantages of Python:</b></ins>

- It was designed for readability, and has some similarities to the English language with influence from mathematics.
- It has syntax that allows developers to write programs with fewer lines than some other programming languages.
- Python can be treated in a **procedural way**, an **object-oriented way** or a **functional way**.

<ins><b>Common IDEs for Python Development:</b></ins>

- Thonny
- PyCharm
- Netbeans
- Eclipse

<ins><b>Checking Python installation:</b></ins>

```bash
python --version
```

- The alias for `python` is `py`.
- The exit command is `exit()`.

## Syntax

- <ins><b>Indentation:</b></ins> Refers to the spaces at the beginning of a code line. Python uses indentation to indicate a block of code. The most common number of spaces used is **4**, but it has to be at least **1**.

- <ins><b>Variable:</b></ins> A variable is created when you assign a value to it. **Python has no command for declaring a variable.**

    ```
    x = 5
    y = "Hello, World!"
    ```

- <ins><b>Comment:</b></ins> Comments start with a `#`, and Python will render the rest of the line as a comment.

    ```
    # === this is a comment. ===
    print("Hello, World!")
    ```

- <ins><b>Expression:</b></ins> Evaluates data to produce a single value.

    ```
    2 + 3
    ```

    ```
    len("apple")
    ```

- <ins><b>Statement:</b></ins> A statement is a complete instruction that tells the Python interpreter to perform a specific action. Python splits statements into two primary groups: **Simple statements** and **Compound statements**:
    1. <ins><b>Simple Statements:</b></ins>
        - **Assignment:** `age = 25`

        - **Expression:** `print("Hi!")`

        - **Loop Control:** `break`

        - **Import:** `import numpy as np`

    2. <ins><b>Compound Statements:</b></ins>
        - **Conditional**

            ```
            if score >= 90:
                print("Grade: A")
            ```

        - **Loop**

            ```
            for item in [1, 2, 3]:
                print(item)
            ```

        - **Context Manager**

            ```
            with open("data.txt") as file:
            content = file.read()
            ```
