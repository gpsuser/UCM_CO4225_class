# Python Programming: Lecture 1 - Development Environment, Variables, Data Types, Strings, Input & Output

**Duration:** 90 minutes

**Prerequisites:** None

---

## Learning Objectives

By the end of this lecture, students will be able to:

1. **Set up and navigate** a Python Integrated Development Environment (IDE) to create and run Python programs
2. **Write and execute** a basic "Hello World" program in Python
3. **Create and manipulate** string variables using concatenation and formatting techniques
4. **Apply** proper commenting practices to document Python code
5. **Implement** escape characters to format string output
6. **Capture user input** using the `input()` function
7. **Identify and use** Python's core data types (strings, integers, floats, booleans)
8. **Perform** mathematical calculations using Python's arithmetic operators
9. **Understand** operator precedence and use assignment operators effectively

---

## Section 1: Introduction to Python and IDEs 

### 1.1 What is Python?

Python is a high-level, interpreted programming language known for its:

- **Readability**: Clean, English-like syntax
- **Versatility**: Used in web development, data science, automation, AI, and more
- **Large ecosystem**: Extensive libraries and community support
- **Beginner-friendly**: Minimal syntax overhead compared to languages like Java or C++

### 1.2 Integrated Development Environments (IDEs)

An IDE is a software application that provides comprehensive facilities for software development. Key features include:

- **Code editor** with syntax highlighting
- **Debugger** for finding and fixing errors
- **Code completion** for faster writing
- **Project management** tools
- **Integrated terminal/console**

**Popular Python IDEs:**

- **PyCharm** (JetBrains) - Full-featured, professional IDE
- **Visual Studio Code** - Lightweight, extensible editor
- **Jupyter Notebook** - Interactive, web-based environment (great for data science)
- **Spyder** - Scientific Python IDE
- **IDLE** - Python's built-in IDE (basic but sufficient for learning)

### 1.3 Setting Up Your Environment

**Basic Steps:**

1. Ensure Python is installed (Python 3.8 or higher recommended)
   - Check by opening terminal/command prompt and typing: `python --version` or `python3 --version`
2. Choose and install an IDE (we'll use PyCharm Community or VS Code for this course)
3. Create your first project
4. Configure the Python interpreter

**Project Structure:**
```
my_first_project/
│
├── main.py          # Your main Python file
├── venv/            # Virtual environment (optional but recommended)
└── README.md        # Project documentation
```

---

## Section 2: Your First Python Program - Hello World 

### 2.1 Creating and Running Hello World

**Step-by-step process:**

1. Create a new Python file (e.g., `hello.py`)
2. Write the code
3. Run the program

**Example:**
```python
print("Hello, World!")
```

**Output:**
```
Hello, World!
```

### 2.2 Understanding the Code

- `print()` is a built-in Python function that outputs text to the console
- Strings (text) are enclosed in quotes - either single `'` or double `"`
- No semicolons needed at the end of statements (unlike Java)
- No main method or class structure required (unlike Java)

### 2.3 Running Python Code

**Method 1: Using the IDE**

- Click the "Run" button or use the keyboard shortcut (Shift+F10 in PyCharm, F5 in VS Code)

**Method 2: Using the Command Line**
```bash
python hello.py
```
or
```bash
python3 hello.py
```

---

## Section 3: Variables and String Manipulation

### 3.1 Creating Variables

Variables are containers for storing data. Python uses dynamic typing - you don't need to declare the type.

**Syntax:**
```python
variable_name = value
```

**Examples:**
```python
# String variables
name = "Alice"
greeting = "Hello"
city = 'London'

# Multiple assignments
first_name = "John"
last_name = "Smith"
age = 25
```

**Variable Naming Rules:**

- Must start with a letter or underscore
- Can contain letters, numbers, and underscores
- Case-sensitive (`name` and `Name` are different)
- Cannot use Python keywords (like `print`, `if`, `for`, etc.)
- Use snake_case for multi-word variables (Python convention)

### 3.2 String Concatenation

**Method 1: Using the + operator**
```python
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
print(full_name)  # Output: John Doe
```

**Method 2: Using multiple arguments in print()**
```python
first_name = "John"
last_name = "Doe"
print(first_name, last_name)  # Output: John Doe
# Note: print() automatically adds spaces between arguments
```

**Building Complex Strings:**
```python
name = "Alice"
age = 25
message = "My name is " + name + " and I am " + str(age) + " years old."
print(message)  # Output: My name is Alice and I am 25 years old.
```

### 3.3 String Formatting (Modern Approaches)

**f-strings (Python 3.6+) - RECOMMENDED:**
```python
name = "Bob"
age = 30
city = "New York"

# Clean and readable
message = f"My name is {name}, I am {age} years old, and I live in {city}."
print(message)
```

**format() method:**
```python
message = "My name is {}, I am {} years old.".format(name, age)
print(message)
```

### 3.4 String Methods

```python
text = "Hello, World!"

# Common string methods
print(text.upper())      # HELLO, WORLD!
print(text.lower())      # hello, world!
print(text.replace("World", "Python"))  # Hello, Python!
print(len(text))         # 13 (length of string)
```

**Example Application - Birthday Message:**
```python
name = "Sarah"
age = 21

print(f"Happy Birthday, {name}!")
print(f"You are now {age} years old.")
print(f"Wishing you an amazing year ahead!")
```

---

## Section 4: Comments and Code Documentation

### 4.1 Why Comments Matter

Comments are notes in your code that Python ignores during execution. They help:
- Explain complex logic
- Document your code for others (and your future self)
- Temporarily disable code during testing
- Provide context and reasoning

### 4.2 Single-Line Comments

```python
# This is a single-line comment
print("Hello")  # This comment explains the code on this line

# Comments can be used to disable code
# print("This won't run")
```

### 4.3 Multi-Line Comments

**Method 1: Multiple single-line comments**
```python
# This is a longer comment
# that spans multiple lines
# explaining something complex
```

**Method 2: Multi-line strings (docstrings)**
```python
"""
This is a multi-line comment
using triple quotes.
Often used for documentation.
"""

'''
Single quotes work too
for multi-line strings
'''
```

### 4.4 Best Practices

```python
# GOOD: Explains WHY
# Calculate discount for loyalty customers (10% off)
discount = price * 0.10

# BAD: States the obvious
# Multiply price by 0.10
discount = price * 0.10

# GOOD: Clear and concise
# Initialize student database connection
connection = connect_to_database()

# BAD: Redundant
# Set x to 5
x = 5
```

---

## Section 5: Escape Characters and Special Formatting

### 5.1 Common Escape Characters

Escape characters start with a backslash `\` and represent special characters:

```python
# Newline \n
print("Line 1\nLine 2\nLine 3")
# Output:
# Line 1
# Line 2
# Line 3

# Tab \t
print("Name:\tAlice\nAge:\t25")
# Output:
# Name:   Alice
# Age:    25

# Backslash \\
print("This is a backslash: \\")
# Output: This is a backslash: \

# Quotes inside strings
print("She said, \"Hello!\"")
# Output: She said, "Hello!"

print('It\'s a beautiful day')
# Output: It's a beautiful day
```

### 5.2 Raw Strings

Use raw strings (prefix with `r`) to ignore escape characters:

```python
# Regular string
path = "C:\new\folder\test"  # \n and \t are interpreted as escape chars
print(path)  # Unexpected output

# Raw string
path = r"C:\new\folder\test"
print(path)  # Output: C:\new\folder\test
```

### 5.3 Practical Example

```python
# Receipt formatting
item = "Coffee"
price = 3.50
quantity = 2

print("=" * 30)
print("RECEIPT")
print("=" * 30)
print(f"Item:\t\t{item}")
print(f"Price:\t\t${price}")
print(f"Quantity:\t{quantity}")
print("-" * 30)
print(f"Total:\t\t${price * quantity}")
print("=" * 30)
```

---

## Section 6: User Input

### 6.1 The input() Function

The `input()` function allows your program to receive data from the user:

```python
# Basic syntax
variable = input("Prompt message: ")
```

**Example:**
```python
name = input("What is your name? ")
print(f"Hello, {name}!")

# Sample interaction:
# What is your name? Alice
# Hello, Alice!
```

### 6.2 Input is Always a String

**Important:** The `input()` function always returns a string, even if the user enters a number.

```python
age = input("How old are you? ")
print(type(age))  # <class 'str'>

# If you need a number, you must convert it
age = int(input("How old are you? "))
print(type(age))  # <class 'int'>
```

### 6.3 Interactive Example

```python
# Personal greeting program
first_name = input("Enter your first name: ")
last_name = input("Enter your last name: ")
age = input("Enter your age: ")

print(f"\nProfile Summary:")
print(f"Name: {first_name} {last_name}")
print(f"Age: {age} years old")
print(f"\nNice to meet you, {first_name}!")
```

---

## Section 7: Data Types in Python 

### 7.1 Dynamic Typing

Unlike Java, Python uses dynamic typing - you don't declare variable types explicitly. Python infers the type based on the value.

```python
x = 5           # int
x = "hello"     # now it's a str
x = 3.14        # now it's a float
```

### 7.2 Core Data Types

**1. Integer (int)**
- Whole numbers (positive, negative, or zero)
- No size limit (unlike Java)

```python
age = 25
temperature = -5
big_number = 999999999999999999
print(type(age))  # <class 'int'>
```

**2. Float (float)**
- Decimal numbers
- Used for precise calculations

```python
price = 19.99
pi = 3.14159
temperature = 98.6
print(type(price))  # <class 'float'>
```

**3. String (str)**
- Text data
- Immutable sequence of characters

```python
name = "Alice"
message = 'Hello, World!'
multi_line = """This is a
multi-line string"""
print(type(name))  # <class 'str'>
```

**4. Boolean (bool)**
- True or False values
- Used in conditional logic

```python
is_student = True
has_license = False
print(type(is_student))  # <class 'bool'>
```

### 7.3 Type Checking and Conversion

**Checking types:**
```python
x = 42
print(type(x))  # <class 'int'>
print(isinstance(x, int))  # True
```

**Type conversion (casting):**
```python
# String to integer
age_str = "25"
age_int = int(age_str)
print(age_int + 5)  # 30

# Integer to string
number = 100
text = str(number)
print("The number is " + text)

# String to float
price_str = "19.99"
price_float = float(price_str)
print(price_float * 2)  # 39.98

# Float to integer (truncates decimal)
value = int(3.9)  # value = 3

# Integer to boolean
bool(0)   # False
bool(1)   # True
bool(42)  # True
```

### 7.4 Common Type Errors

```python
# This will cause an error:
age = "25"
next_year = age + 1  # TypeError: can only concatenate str to str

# Fix with type conversion:
age = "25"
next_year = int(age) + 1  # 26
```

---

## Section 8: Calculations and Operators

### 8.1 Arithmetic Operators

```python
a = 10
b = 3

# Addition
print(a + b)  # 13

# Subtraction
print(a - b)  # 7

# Multiplication
print(a * b)  # 30

# Division (always returns float)
print(a / b)  # 3.333...

# Floor division (returns integer, rounds down)
print(a // b)  # 3

# Modulus (remainder)
print(a % b)  # 1

# Exponentiation
print(a ** b)  # 1000 (10 to the power of 3)
```

### 8.2 Operator Precedence

Python follows PEMDAS order:
1. **P**arentheses `()`
2. **E**xponentiation `**`
3. **M**ultiplication `*`, **D**ivision `/`, Floor Division `//`, **M**odulus `%` (left to right)
4. **A**ddition `+`, **S**ubtraction `-` (left to right)

```python
result = 2 + 3 * 4  # 14 (not 20)
result = (2 + 3) * 4  # 20

result = 10 - 4 - 2  # 4 (left to right: 10 - 4 = 6, then 6 - 2 = 4)

result = 2 ** 3 ** 2  # 512 (right to left: 3 ** 2 = 9, then 2 ** 9 = 512)
```

### 8.3 Assignment Operators

**Compound assignment operators:**
```python
x = 10

# Add and assign
x += 5   # x = x + 5  → x is now 15

# Subtract and assign
x -= 3   # x = x - 3  → x is now 12

# Multiply and assign
x *= 2   # x = x * 2  → x is now 24

# Divide and assign
x /= 4   # x = x / 4  → x is now 6.0

# Floor divide and assign
x //= 2  # x = x // 2 → x is now 3.0

# Modulus and assign
x %= 2   # x = x % 2  → x is now 1.0

# Exponent and assign
x **= 3  # x = x ** 3 → x is now 1.0
```

### 8.4 Practical Calculation Examples

**Example 1: Basic Calculator**
```python
# Get two numbers from user
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Perform calculations
print(f"\nResults:")
print(f"{num1} + {num2} = {num1 + num2}")
print(f"{num1} - {num2} = {num1 - num2}")
print(f"{num1} * {num2} = {num1 * num2}")
print(f"{num1} / {num2} = {num1 / num2}")
```

**Example 2: Temperature Converter**
```python
# Celsius to Fahrenheit
celsius = float(input("Enter temperature in Celsius: "))
fahrenheit = (celsius * 9/5) + 32
print(f"{celsius}°C = {fahrenheit}°F")
```

**Example 3: Area Calculator**
```python
# Rectangle area
length = float(input("Enter length: "))
width = float(input("Enter width: "))
area = length * width
perimeter = 2 * (length + width)

print(f"Area: {area}")
print(f"Perimeter: {perimeter}")
```

---

## Section 9: Putting It All Together - Complete Example

### 9.1 Shopping Cart Program

```python
"""
Simple Shopping Cart Calculator
This program calculates the total cost of items with tax
"""

# Display welcome message
print("=" * 40)
print("SHOPPING CART CALCULATOR")
print("=" * 40)

# Get user input
item_name = input("\nEnter item name: ")
quantity = int(input("Enter quantity: "))
price_per_item = float(input("Enter price per item: $"))
tax_rate = 0.08  # 8% tax

# Calculate totals
subtotal = quantity * price_per_item
tax_amount = subtotal * tax_rate
total = subtotal + tax_amount

# Display receipt
print("\n" + "=" * 40)
print("RECEIPT")
print("=" * 40)
print(f"Item:\t\t{item_name}")
print(f"Quantity:\t{quantity}")
print(f"Price Each:\t${price_per_item:.2f}")
print("-" * 40)
print(f"Subtotal:\t${subtotal:.2f}")
print(f"Tax (8%):\t${tax_amount:.2f}")
print("=" * 40)
print(f"TOTAL:\t\t${total:.2f}")
print("=" * 40)
print("\nThank you for shopping with us!")
```

### 9.2 Sample Output

```
========================================
SHOPPING CART CALCULATOR
========================================

Enter item name: Laptop
Enter quantity: 2
Enter price per item: $899.99

========================================
RECEIPT
========================================
Item:           Laptop
Quantity:       2
Price Each:     $899.99
----------------------------------------
Subtotal:       $1799.98
Tax (8%):       $144.00
========================================
TOTAL:          $1943.98
========================================

Thank you for shopping with us!
```

---

## Time Allocation Summary

| Section | Topic | Time (minutes) |
|---------|-------|----------------|
| 1 | Introduction to Python and IDEs | 10 |
| 2 | Hello World Program | 10 |
| 3 | Variables and String Manipulation | 5 |
| 4 | Comments and Documentation | 5 |
| 5 | Escape Characters and Formatting | 5 |
| 6 | User Input | 10 |
| 7 | Data Types in Python | 10 |
| 8 | Calculations and Operators | 10 |
| 9 | Worksheet | 20 |
| **TOTAL** | | **85 minutes + 5 min break** |


---

## Resources for Further Reading and Practice

### Official Documentation
- **Python Official Tutorial**: https://docs.python.org/3/tutorial/
- **Python Built-in Functions**: https://docs.python.org/3/library/functions.html
- **Python String Methods**: https://docs.python.org/3/library/stdtypes.html#string-methods

### IDE Documentation
- **PyCharm Getting Started**: https://www.jetbrains.com/help/pycharm/quick-start-guide.html
- **VS Code Python Tutorial**: https://code.visualstudio.com/docs/python/python-tutorial

### Interactive Learning Platforms
- **Python.org Beginner's Guide**: https://wiki.python.org/moin/BeginnersGuide
- **Real Python - Python Basics**: https://realpython.com/learning-paths/python-basics/
- **Codecademy Python Course**: https://www.codecademy.com/learn/learn-python-3
- **HackerRank Python Practice**: https://www.hackerrank.com/domains/python

### Practice Challenges

1. **Easy**: Write a program that asks for your name and age, then calculates what year you were born
2. **Easy**: Create a tip calculator that computes 15%, 18%, and 20% tips
3. **Medium**: Build a BMI (Body Mass Index) calculator that also provides health category feedback
4. **Medium**: Create a program that converts between miles/kilometers, pounds/kilograms, and Fahrenheit/Celsius

### Recommended Textbook Chapters

- **"Python Crash Course" by Eric Matthes** (3rd Edition)
  - Chapter 1: Getting Started
  - Chapter 2: Variables and Simple Data Types
- **"Automate the Boring Stuff with Python" by Al Sweigart**
  - Chapter 0: Introduction
  - Chapter 1: Python Basics

### Video Tutorials

- **Corey Schafer's Python Tutorial for Beginners**: https://www.youtube.com/watch?v=YYXdXT2l-Gg
- **freeCodeCamp Python Course**: https://www.youtube.com/watch?v=rfscVS0vtbw

### Style Guide

- **PEP 8 - Python Style Guide**: https://pep8.org/
  - Learn Python coding conventions and best practices

---

## Key Takeaways

By the end of this lecture, you should understand:

✓ How to set up and use a Python IDE  
✓ The structure of a basic Python program  
✓ How to create and manipulate variables  
✓ String operations and formatting with f-strings  
✓ The importance of code comments  
✓ How to use escape characters for special formatting  
✓ Capturing and processing user input  
✓ Python's core data types and type conversion  
✓ Performing calculations with arithmetic operators  
✓ Operator precedence and assignment operators  

**Remember**: Programming is a skill learned through practice. Work through the practice challenges and experiment with the concepts covered in this lecture!