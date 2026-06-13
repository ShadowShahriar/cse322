# Quiz

## Topic List

1. [**Basics of Python**](#basics-of-python)
2. [**Syntax**](#syntax)
3. [**Output**](#output)
4. [**Comments**](#comments)
5. [**Variables and Data Types**](#variables-and-data-types)
    1. [**Numbers**](#numbers)
    2. [**Strings**](#strings)
        - [**String Slicing**](#string-slicing)
        - [**String Manipulation**](#string-manipulation)
        - [**F-Strings**](#f-strings)
        - [**Escape Characters**](#escape-characters)
        - [**Common String Methods**](#common-string-methods)
    3. [**Booleans**](#booleans)
6. [**Operators**](#operators)
7. [**Type Casting**](#type-casting)
8. [**Collections**](#collections)
    1. [**Lists**](#lists)
    2. [**Tuples**](#tuples)
    3. [**Sets**](#sets)
    4. [**Key-Value Pairs (Dictionaries)**](#dictionaries)
9. **Conditionals**
    1. [**If-Else**](#if-else)
    2. [**Match (Switch Case)**](#match)
10. **Loops**
    1. [**For Loops**](#for-loops)
    2. [**While Loops**](#while-loops)
11. [**Functions**](#functions)
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

```
python --version
```

- The alias for `python` is `py`.
- The exit command is `exit()`.

---

## Syntax

- <ins><b>Indentation:</b></ins> Refers to the spaces at the beginning of a code line. Python uses indentation to indicate a block of code. The most common number of spaces used is **4**, but it has to be at least **1**.

- <ins><b>Variable:</b></ins> A variable is created when we assign a value to it. **Python has no command for declaring a variable.**

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

- <ins><b>Semicolons:</b></ins> Semicolons are **optional** in Python. We can write multiple statements on one line by separating them with `;` but this is rarely used.

---

## Output

- We can use the `print()` function to display text or output values. By default, the `print()` function ends with a new line. If we want to print multiple words on the same line, we can use the end parameter:

    ```
    print("Hello World!", end=" ")
    print("I will print on the same line.")
    ```

- Text in Python must be inside quotes. We can use either `"` double quotes or `'` single quotes. However, unlike text, we don't put numbers inside quotes.

    ```
    print(3)
    print(358)
    print(50000)
    ```

- We can combine text and numbers in one output by separating them with a comma.

    ```
    print("I am", 35, "years old.")
    ```

---

## Comments

- Comments starts with a `#`, and Python will ignore them:

    ```
    # === this is a comment ===
    print("Hello, World!")
    ```

- Comments can be placed at the end of a line, and Python will ignore the rest of the line:

    ```
    print("Hello, World!") # === this is a comment ===
    ```

- Python does not really have a syntax for multiline comments. To add a multiline comment we could insert a `#` for each line.

    ```
    # This is a comment
    # written in
    # more than just one line
    print("Hello, World!")
    ```

- Since Python will ignore string literals that are not assigned to a variable, we can add a multiline string (**triple quotes**) in the code, and place out comment inside it:

    ```
    """
    This is a comment
    written in
    more than just one line
    """
    print("Hello, World!")
    ```

---

## Variables and Data Types

> Variables are containers for storing data values.

- Python has no command for **declaring a variable**.
- A variable is created the moment we first **assign a value to it**.
- Variables do not need to be declared with any particular type, and can even **change type after they have been set**.
- String variables can be declared either by using single or double quotes.
- Variable names are **case-sensitive**.

<ins><b>Rules for variable names:</b></ins>

- A variable name must start with a letter or the underscore character,
- A variable name cannot start with a number,
- A variable name can only contain alpha-numeric characters and underscores, (**A-Z, a-z, 0-9, and \_**)
- Variable names are case-sensitive, (`age`, `Age` and `AGE` are three different variables)
- A variable name cannot be any of the **Python keywords.**

<ins><b>Name cases:</b></ins>

- **Camel Case:** Each word, except the first, starts with a capital letter.
- **Pascal Case:** Each word starts with a capital letter.
- **Snake Case:** Each word is separated by an underscore character.

<ins><b>Value assignment:</b></ins>

1. **Many Values to Multiple Variables:**

    ```
    x, y, z = "Orange", "Banana", "Cherry"
    print(x)
    print(y)
    print(z)
    ```

2. **One Value to Multiple Variables**

    ```
    x = y = z = "Orange"
    print(x)
    print(y)
    print(z)
    ```

<ins><b>Global variables:</b></ins> Variables that are created outside of a function are known as global variables. Global variables can be used by everyone, both inside of functions and outside.

> If we create a variable with **the same name** inside a function, this variable will be local, and can only be used inside the function. The global variable with the same name **will remain as it was**, global and **with the original value**.

<ins><b>Global keyword:</b></ins> Normally, when we create a variable inside a function, that variable is local, and can only be used inside that function.

- To create a global variable inside a function, we can use the `global` keyword.
- We can use the `global` keyword if you want to change a global variable inside a function.

```
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

<ins><b>Built-in data types:</b></ins>

- **Text:** `str`
- **Numeric:** `int`, `float`, `complex`
- **Sequence:** `list`, `tuple`, `range`
- **Map:** `dict`
- **Set:** `set`, `frozenset`
- **Boolean:** `bool`
- **Binary:** `bytes`, `bytearray`, `memoryview`
- **None:** `NoneType`

Printing the data type of a variable `x`:

```
x = 5
print(type(x))
```

---

## Numbers

Three numeric types in Python:

- <ins><b>int:</b></ins> a whole number, positive or negative, without decimals, of unlimited length.

    ```
    x = 1
    y = 35656222554887711
    z = -3255522
    ```

- <ins><b>float:</b></ins> a number, positive or negative, containing one or more decimals. `float` can also be scientific numbers with an `e` to indicate the power of **10**.

    ```
    x = 1.10
    y = 1.0
    z = -35.59

    x = 35e3
    y = 12E4
    z = -87.7e100
    ```

- <ins><b>complex:</b></ins> numbers that are written with a `j` as the imaginary part.

    ```
    x = 3+5j
    y = 5j
    z = -5j
    ```

- We can convert from one type to another with the `int()`, `float()`, and `complex()` methods.

- A built-in module called `random` that can be used to make random numbers.

    ```
    import random

    # === display a random number from 1 to 9 ===
    print(random.randrange(1, 10))
    ```

---

## Strings

> Strings in Python are arrays of unicode characters. However, Python does not have a character data type, **a single character** is simply a string with a length of **1**.

- We can use quotes inside a string, as long as they don't match the quotes surrounding the string:

    ```
    print("It's alright")
    print("He is called 'Johnny'")
    print('He is called "Johnny"')
    ```

- We can assign a multiline string to a variable by using three quotes:

    ```
    a = """Lorem ipsum dolor sit amet,
    consectetur adipiscing elit,
    sed do eiusmod tempor incididunt
    ut labore et dolore magna aliqua."""

    print(a)
    ```

- <ins><b>Looping Through a String:</b></ins>

    ```
    for x in "banana":
    print(x)
    ```

- <ins><b>String Length:</b></ins>

    ```
    a = "Hello, World!"
    print(len(a))
    ```

- <ins><b>Check String:</b></ins> To check if a certain phrase or character is present in a string, we can use the keyword `in`.

    ```
    # ====
    # check if "free" is present:
    # ====

    txt = "The best things in life are free!"
    print("free" in txt)

    # ====
    # check if "expensive" is NOT present:
    # ====

    txt = "The best things in life are free!"
    print("expensive" not in txt)
    ```

### String Slicing

Consider this string:

```
b = "Hello, World!"
```

Get the characters from **position 2** to **position 5** (_not included_):

```
print(b[2:5])
```

Get the characters from the start to **position 5** (_not included_):

```
print(b[:5])
```

Get the characters from **position 2**, and all the way to the end:

```
print(b[2:])
```

Get the characters:<br>From: **"o"** in "World!" (**position -5**)<br>To, but not included: **"d"** in "World!" (**position -2**):

```
b = "Hello, World!"
print(b[-5:-2])
```

### String Manipulation

- **Upper Case:** `upper()`
- **Lower Case:** `lower()`
- **Remove Whitespace:** `strip()`
- **Replace:** `replace(from, to)`
- **Split:** `split(separator)`
- **Concatenation:** `string1 + string2`

### F-Strings

> We can combine strings and numbers by using **f-strings** or the `format()` method.

```
age = 36
txt = f"My name is John, I am {age}"
print(txt)
```

Display the price with 2 decimals:

```
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)
```

Perform a math operation in the placeholder, and return the result:

```
txt = f"The price is {20 * 59} dollars"
print(txt)
```

### Escape Characters

- **\'** (Single quote)
- **\\\\** (Backslash)
- **\n** (New line)
- **\r** (Carriage Return)
- **\t** (Tab)
- **\b** (Backspace)
- **\f** (Form feed)
- **\ooo** (Octal value)
- **\xhh** (Hex value)

### Common String Methods

- **capitalize()**
- **count()**
- **find()**
- **islower()**
- **isupper()**
- **format()**
- **upper()**
- **lower()**
- **startswith()**
- **endswith()**
- **strip()**
- **title()**
- **swapcase()**

---

## Booleans

Almost any value is evaluated to `True` if it has some sort of content.

- Any string is `True`, except **empty strings**.
- Any number is `True`, except **0**.
- Any list, tuple, set, and dictionary are `True`, except **empty ones**.

There are not many values that evaluate to `False`, except empty values, such as `()`, `[]`, `{}`, `""`, the number `0`, and the value `None`.

One more value, or _object_ in this case, evaluates to `False`, and that is if you have an object that is made from a class with a `__len__` function that returns `0` or `False`:

> Python has many built-in functions that return a boolean value, like the `isinstance()` function, which can be used to determine if an object is of a certain data type.

---

## Operators

> If two operators have the same precedence, the expression is evaluated from left to right.

- <ins><b>Arithmetic operators:</b></ins> Arithmetic operators are used with numeric values to perform common mathematical operations.

    ```
    print(x + y)
    print(x - y)
    print(x * y)
    print(x / y)
    print(x % y)
    print(x ** y)
    print(x // y)
    ```

    - **/** - Division (always returns a float)
    - **//** - Floor division (always returns the nearest floor integer)

- <ins><b>Assignment operators:</b></ins> Assignment operators are used to assign values to variables.
    - **Python 3.8** introduced the `:=` operator, known as the **walrus operator**. It assigns values to variables as part of a larger expression: `print(x := 3)`

- <ins><b>Ternary operators:</b></ins> The ternary operator is **not** an actual operator, it is a conditional expression, or a shorthand if statement.

    ```
    num = 6
    x = "Weekend" if num > 5 else "Workday"
    print(x)
    ```

- <ins><b>Comparison operators:</b></ins> Comparison operators are used to compare two values.

    ```
    x = 5
    y = 3
    print(x == y)
    print(x != y)
    print(x > y)
    print(x < y)
    print(x >= y)
    print(x <= y)

    x = 5
    print(1 < x < 10)
    print(1 < x and x < 10)
    ```

- <ins><b>Logical operators:</b></ins> Logical operators are used to combine conditional statements.
    - **AND:** Returns `True` if both statements are true

    - **OR:** Returns `True` if one of the statements is true.

    - **NOT:** Reverse the result, returns `False` if the result is true.

- <ins><b>Identity operators:</b></ins> Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location.
    - **is:** Returns `True` if both variables are the same object.

    - **is not:** Returns `True` if both variables are not the same object.

- <ins><b>Membership operators:</b></ins> Membership operators are used to test if a sequence is presented in an object.
    - **in:** Returns `True` if a sequence with the specified value is present in the object.

    - **not in:** Returns `True` if a sequence with the specified value is not present in the object.

- <ins><b>Bitwise operators:</b></ins> Bitwise operators are used to compare (**binary**) numbers.

| Operator | Name                 | Description                                                                                             | Example |
| -------- | -------------------- | ------------------------------------------------------------------------------------------------------- | ------- |
| &        | AND                  | Sets each bit to 1 if both bits are 1                                                                   | x & y   |
| \|       | OR                   | Sets each bit to 1 if one of two bits is 1                                                              | x \| y  |
| ^        | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         | x ^ y   |
| ~        | NOT                  | Inverts all the bits                                                                                    | ~x      |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        | x << 2  |
| \>>      | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2  |

---

## Type Casting

Casting in python is therefore done using constructor functions:

- **int():** constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number)

- **float():** constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)

- **str():** constructs a string from a wide variety of data types, including strings, integer literals and float literals.

---

## Collections

There are **4 built-in data types** in Python used to store collections of data and they are **List**, **Tuple**, **Set**, and **Dictionary**, all with different qualities and usage.

### Lists

```
thislist = ["apple", "banana", "cherry"]
thislist = list(("apple", "banana", "cherry")) # constructor
```

✅ ordered<br>
✅ changeable<br>
✅ allow duplicate values

### Tuples

Tuples are used to store multiple items in a single variable.

```
thistuple = ("apple", "banana", "cherry")
thistuple = ("apple",)
```

✅ ordered<br>
⛔ unchangeable<br>
✅ allow duplicate values

### Sets

Sets are used to store multiple items in a single variable.

```
thisset = {"apple", "banana", "cherry"}
```

⛔ unordered<br>
⛔ unchangeable\*<br>
⛔ unindexed<br>
⛔ does not allow duplicate values

> Set _items_ are unchangeable, but we can remove items and add new items.

### Dictionaries

Dictionaries are used to store data values in `key:value` pairs.

```
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```

✅ ordered\*<br>
✅ changeable<br>
⛔ does not allow duplicate values

> As of Python version **3.7**, dictionaries are ordered. In Python **3.6 and earlier**, dictionaries are unordered.

---

## If-Else

`if`, `elif`, and `else`:

```
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```

Shorthand `if`:

```
a = 5
b = 2
if a > b: print("a is greater than b")
```

Shorthand `if ... else`:

```
a = 2
b = 330
print("A") if a > b else print("B")
```

Assign a value with `if ... else`:

```
variable = value_if_true if condition else value_if_false
```

Nested `if` statements:

```
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

`pass` statement:

```
a = 33
b = 200

if b > a:
  pass
```

> The `pass` statement is a **null operation** - nothing happens when it executes. It serves as a placeholder.

---

## Match

The `match` statement is used to perform different actions based on different conditions. Instead of writing many `if..else` statements, you can use the `match` statement.

```
match expression:
  case x:
    code block
  case y:
    code block
  case z:
    code block
  case _:      # === default block ===
    code block
```

**Combining values:**

```
day = 4
match day:
  case 1 | 2 | 3 | 4 | 5:
    print("Today is a weekday")
  case 6 | 7:
    print("I love weekends!")
```

---

## For Loops

A `for` loop is used for iterating over a sequence (that is either a _list_, a _tuple_, a _dictionary_, a _set_, or a _string_).

```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```

### Looping a string

```
for x in "banana":
  print(x)
```

### break

Exit the loop when `x` is "banana":

```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break
```

### continue

Do not print "banana":

```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
```

### range()

To loop through a set of code a specified number of times, we can use the `range()` function, The `range()` function returns a sequence of numbers, starting from **0** by default, and increments by **1** (by default), and ends at a specified number.

```
for x in range(6): # 0 to 5
  print(x)
```

The `range()` function defaults to increment the sequence by **1**, however it is possible to specify the increment value by adding a third parameter: `range(0, 6, 2)`

### else

the `else` keyword in a for loop specifies a block of code to be executed when the loop is finished.

Print all numbers from **0** to **5**, and print a message when the loop has ended:

```
for x in range(6):
  print(x)
else:
  print("Finally finished!")
```

> The `else` block will **NOT** be executed if the loop is stopped by a `break` statement.

### Nested loops

```
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
```

### pass

```
for x in [0, 1, 2]:
  pass
```

---

## While Loops

> With the `while` loop, we can execute a set of statements as long as a condition is true.

```
i = 1
while i < 6:
  print(i)
  i += 1
```

### break

Exit the loop when `i` is `3`.

```
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

### continue

Continue to the next iteration if `i` is `3`.

```
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

### else

Print a message once the condition is false.

```
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```

---

## Functions

- A function is a block of code which only runs when it is called.
- A function can return data as a result.
- A function helps avoiding code repetition.

```
def my_function():
  print("Hello from a function")
```

- A function name must start with a letter or underscore,
- A function name can only contain letters, numbers, and underscores,
- Function names are **case-sensitive**. (`myFunction` and `myfunction` are different)

Functions can send data back to the code that called them using the `return` statement.

```
def get_greeting():
  return "Hello from a function"

message = get_greeting()
print(message)
```

If a function doesn't have a return statement, it returns `None` by default.

Function definitions cannot be empty. If we need to create a function placeholder without any code, use the pass statement:

```
def my_function():
  pass
```
