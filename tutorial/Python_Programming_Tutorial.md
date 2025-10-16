# Python Programming Tutorial

## Introduction

Welcome to this comprehensive Python programming tutorial! This course covers fundamental programming concepts using Python, mirroring topics typically taught in introductory Java courses but adapted for Python's syntax and conventions.

Each section includes:
- Clear explanations of concepts
- Worked examples with code
- A practical task for you to complete

---

## 1. Integrated Development Environments (IDEs)

### What is an IDE?

An Integrated Development Environment (IDE) is software that provides comprehensive facilities for software development. Popular Python IDEs include:
- **PyCharm** (Professional and Community editions)
- **Visual Studio Code** (VS Code) with Python extension
- **IDLE** (comes with Python)
- **Jupyter Notebook** (great for learning and data science)

### Creating a New Python Project

**In PyCharm:**
1. Open PyCharm
2. Click "New Project"
3. Choose a location and name for your project
4. Select the Python interpreter
5. Click "Create"

**In VS Code:**
1. Open VS Code
2. Open a folder (File > Open Folder)
3. Create a new file with `.py` extension
4. Select your Python interpreter (bottom left of window)

### Your First Program

```python
# This is a comment - it doesn't execute
print("Hello, World!")
```

**Explanation:** The `print()` function displays output to the console.

### Task 1.1
Create a new Python file called `first_program.py` and write a program that prints your name, your course, and the current year on three separate lines.

---

## 2. String Variables

### What are Variables?

Variables are containers that store data values. In Python, you don't need to declare the type explicitly.

### Working with Strings

```python
# Creating string variables
name = "Alice"
greeting = "Hello"

# Printing variables
print(name)
print(greeting)

# Single or double quotes both work
message1 = 'Welcome'
message2 = "to Python"
```

### Task 2.1
Create variables to store your first name, last name, and favorite programming language. Print each variable on a separate line.

---

## 3. String Concatenation

### Combining Strings

In Python, you can combine strings using the `+` operator or other methods.

```python
first_name = "John"
last_name = "Smith"

# Using + operator
full_name = first_name + " " + last_name
print(full_name)  # Output: John Smith

# Using f-strings (modern Python)
greeting = f"Hello, {first_name} {last_name}!"
print(greeting)  # Output: Hello, John Smith!

# Using .format() method
message = "My name is {} {}".format(first_name, last_name)
print(message)
```

### Task 3.1
Create variables for a street name, city, and postal code. Concatenate them to form a complete address and print it in a nicely formatted way.

---

## 4. Appending Strings

### Building Strings Incrementally

```python
# Using += to append to strings
sentence = "Python"
sentence += " is"
sentence += " awesome"
print(sentence)  # Output: Python is awesome

# Building a longer message
story = "Once upon a time"
story += ", there was a programmer"
story += " who loved Python."
print(story)
```

### Task 4.1
Start with an empty string and use the `+=` operator to build a sentence word by word. Your sentence should be at least 8 words long and describe what you're learning.

---

## 5. Getting User Input

### The input() Function

The `input()` function allows you to get data from the user.

```python
# Getting user input
name = input("What is your name? ")
print(f"Hello, {name}!")

# Input always returns a string
age_string = input("How old are you? ")
print(f"You are {age_string} years old.")
```

### Task 5.1
Write a program that asks the user for their favorite food and favorite color, then prints a message using both pieces of information.

---

## 6. Data Types

### Understanding Python Data Types

Python has several built-in data types:

```python
# Integer (whole numbers)
age = 25
count = -10

# Float (decimal numbers)
price = 19.99
temperature = -5.5

# String (text)
name = "Python"

# Boolean (True or False)
is_student = True
has_license = False

# Checking the type
print(type(age))        # <class 'int'>
print(type(price))      # <class 'float'>
print(type(name))       # <class 'str'>
print(type(is_student)) # <class 'bool'>
```

### Converting User Input

```python
# Converting string to integer
age_str = input("Enter your age: ")
age = int(age_str)

# Converting string to float
price_str = input("Enter the price: ")
price = float(price_str)

# Shorthand version
height = float(input("Enter your height in meters: "))
```

### Task 6.1
Write a program that asks the user for their birth year (as an integer) and calculates their age in 2025. Print the result with an appropriate message.

---

## 7. Basic Calculations

### Arithmetic Operations

```python
# Basic operators
a = 10
b = 3

print(f"Addition: {a + b}")           # 13
print(f"Subtraction: {a - b}")        # 7
print(f"Multiplication: {a * b}")     # 30
print(f"Division: {a / b}")           # 3.333...
print(f"Integer Division: {a // b}")  # 3
print(f"Modulus (remainder): {a % b}")# 1
print(f"Exponentiation: {a ** b}")    # 1000

# Order of operations (PEMDAS)
result = 10 + 5 * 2
print(result)  # 20 (not 30)

result = (10 + 5) * 2
print(result)  # 30
```

### Task 7.1
Write a program that asks the user for the length and width of a rectangle, then calculates and prints both the perimeter and area.

---

## 8. Assignment Operators & Operator Precedence

### Compound Assignment Operators

```python
x = 10

# These are shortcuts
x += 5   # Same as: x = x + 5
print(x)  # 15

x -= 3   # Same as: x = x - 3
print(x)  # 12

x *= 2   # Same as: x = x * 2
print(x)  # 24

x /= 4   # Same as: x = x / 4
print(x)  # 6.0

x //= 2  # Same as: x = x // 2
print(x)  # 3.0

x %= 2   # Same as: x = x % 2
print(x)  # 1.0
```

### Operator Precedence

Python follows this order (highest to lowest):
1. Parentheses `()`
2. Exponentiation `**`
3. Multiplication, Division, Floor Division, Modulus `*`, `/`, `//`, `%`
4. Addition, Subtraction `+`, `-`

```python
result = 2 + 3 * 4 ** 2
print(result)  # 2 + 3 * 16 = 2 + 48 = 50
```

### Task 8.1
Write a program that asks the user for a number, then performs the following operations in order: add 10, multiply by 2, subtract 5, and divide by 3. Print the result at each step.

---

## 9. If Statements

### Making Decisions in Code

```python
# Basic if statement
age = 18

if age >= 18:
    print("You are an adult")

# If with comparison operators
temperature = 25

if temperature > 30:
    print("It's hot!")

# Multiple conditions can exist independently
score = 85

if score >= 90:
    print("Grade: A")

if score >= 80:
    print("Grade: B or higher")

if score >= 70:
    print("Grade: C or higher")
```

### Task 9.1
Write a program that asks the user for a number. If the number is positive, print "Positive". If the number is greater than 100, print "Large number".

---

## 10. If-Else Statements

### Two-Way Decisions

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")

# Elif for multiple conditions
grade = int(input("Enter your grade (0-100): "))

if grade >= 90:
    print("Excellent! Grade: A")
elif grade >= 80:
    print("Great! Grade: B")
elif grade >= 70:
    print("Good! Grade: C")
elif grade >= 60:
    print("Pass. Grade: D")
else:
    print("Fail. Grade: F")
```

### Task 10.1
Write a program that asks the user for a temperature in Celsius. If it's below 0, print "Freezing". If it's 0-15, print "Cold". If it's 16-25, print "Mild". If it's above 25, print "Warm".

---

## 11. Match Statements (Python's Switch)

### Pattern Matching (Python 3.10+)

Python 3.10 introduced the `match` statement, similar to Java's switch:

```python
day = input("Enter a day of the week: ")

match day.lower():
    case "monday":
        print("Start of the work week")
    case "tuesday" | "wednesday" | "thursday":
        print("Middle of the week")
    case "friday":
        print("TGIF!")
    case "saturday" | "sunday":
        print("Weekend!")
    case _:
        print("Invalid day")
```

### Alternative: Dictionary Mapping

For older Python versions:

```python
def get_day_message(day):
    messages = {
        "monday": "Start of the work week",
        "tuesday": "Second day",
        "wednesday": "Hump day",
        "thursday": "Almost Friday",
        "friday": "TGIF!",
        "saturday": "Weekend!",
        "sunday": "Weekend!"
    }
    return messages.get(day.lower(), "Invalid day")

day = input("Enter a day: ")
print(get_day_message(day))
```

### Task 11.1
Create a simple calculator using match statements (or if-elif statements). Ask the user for two numbers and an operation (+, -, *, /). Perform the operation and print the result.

---

## 12. While Loops

### Repeating Code with Conditions

```python
# Basic while loop
count = 1
while count <= 5:
    print(f"Count: {count}")
    count += 1

# User input validation
password = ""
while password != "python123":
    password = input("Enter password: ")
    if password != "python123":
        print("Incorrect! Try again.")

print("Access granted!")

# Infinite loop with break
while True:
    user_input = input("Type 'quit' to exit: ")
    if user_input.lower() == 'quit':
        break
    print(f"You typed: {user_input}")
```

### Task 12.1
Write a program that asks the user to guess a secret number (you choose the number). Keep asking until they guess correctly. After each wrong guess, tell them if their guess was too high or too low.

---

## 13. Do-While Loops (Python Equivalent)

### Loops That Run At Least Once

Python doesn't have a do-while loop, but we can simulate it:

```python
# Simulating do-while
while True:
    number = int(input("Enter a positive number: "))
    if number > 0:
        break
    print("That's not positive! Try again.")

print(f"You entered: {number}")

# Another approach
choice = None
while choice != 'quit':
    print("\n1. Option A")
    print("2. Option B")
    print("Type 'quit' to exit")
    choice = input("Your choice: ")
    
    if choice == '1':
        print("You selected Option A")
    elif choice == '2':
        print("You selected Option B")
    elif choice != 'quit':
        print("Invalid choice")
```

### Task 13.1
Create a menu-driven program that displays a menu of 3 options, gets the user's choice, and performs an action. The program should keep running until the user chooses to exit.

---

## 14. Logical Operators

### Combining Conditions

```python
# AND operator - both must be true
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive")

# OR operator - at least one must be true
is_weekend = True
is_holiday = False

if is_weekend or is_holiday:
    print("No work today!")

# NOT operator - inverts the boolean
is_raining = False

if not is_raining:
    print("It's a nice day")

# Complex conditions
temperature = 22
is_sunny = True

if temperature > 20 and is_sunny and not is_raining:
    print("Perfect day for a picnic!")

# Short-circuit evaluation
x = 10
if x > 0 and x < 100 and x % 2 == 0:
    print("x is a positive even number less than 100")
```

### Task 14.1
Write a program that asks for a user's age and whether they are a student. If they are under 18 OR they are a student, they get a discount. Print an appropriate message based on whether they qualify for the discount.

---

## 15. The String Class

### String Methods and Operations

```python
text = "Hello, Python Programming!"

# Case conversion
print(text.upper())      # HELLO, PYTHON PROGRAMMING!
print(text.lower())      # hello, python programming!
print(text.title())      # Hello, Python Programming!

# Checking content
print(text.startswith("Hello"))  # True
print(text.endswith("!"))        # True
print("Python" in text)          # True

# Finding and replacing
print(text.find("Python"))       # 7
print(text.replace("Python", "Java"))

# Splitting and joining
words = text.split()
print(words)  # ['Hello,', 'Python', 'Programming!']

new_text = "-".join(words)
print(new_text)  # Hello,-Python-Programming!

# Stripping whitespace
messy = "  hello  "
print(messy.strip())   # "hello"

# String formatting
name = "Alice"
age = 25
message = f"My name is {name} and I am {age} years old"
print(message)

# Getting string length
print(len(text))  # 27

# Accessing characters
print(text[0])    # H
print(text[-1])   # !
print(text[0:5])  # Hello
```

### Task 15.1
Write a program that asks the user for a sentence. Count and print: the number of characters, the number of words, and whether the sentence contains the word "python" (case-insensitive).

---

## 16. For Loops

### Iterating a Specific Number of Times

```python
# Basic for loop with range
for i in range(5):
    print(f"Iteration {i}")

# Output:
# Iteration 0
# Iteration 1
# Iteration 2
# Iteration 3
# Iteration 4

# Range with start and stop
for i in range(1, 6):
    print(i)  # Prints 1, 2, 3, 4, 5

# Range with start, stop, and step
for i in range(0, 10, 2):
    print(i)  # Prints 0, 2, 4, 6, 8

# Counting backwards
for i in range(10, 0, -1):
    print(i)  # Prints 10, 9, 8, ..., 1

# Iterating over a string
name = "Python"
for char in name:
    print(char)
```

### Task 16.1
Write a program that prints the multiplication table for a number entered by the user (from 1 to 12).

---

## 17. Further For Loops

### Nested Loops and Advanced Patterns

```python
# Nested loops
for i in range(1, 4):
    for j in range(1, 4):
        print(f"i={i}, j={j}")

# Creating patterns
for i in range(1, 6):
    print("*" * i)
# Output:
# *
# **
# ***
# ****
# *****

# Using enumerate for index and value
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")

# Loop with else clause (runs if loop completes normally)
for i in range(5):
    if i == 10:  # This never happens
        break
else:
    print("Loop completed normally")
```

### Task 17.1
Write a program that prints a multiplication grid from 1 to 10. Each row should show one times table.

---

## 18. Functions (Methods)

### Creating Reusable Code

```python
# Simple function
def greet():
    print("Hello!")

greet()  # Call the function

# Function with return value
def add_numbers():
    return 5 + 3

result = add_numbers()
print(result)  # 8

# More complex function
def calculate_circle_area():
    radius = 5
    pi = 3.14159
    area = pi * radius ** 2
    return area

area = calculate_circle_area()
print(f"Circle area: {area}")
```

### Task 18.1
Write a function called `is_even()` that returns `True` if a hardcoded number is even, and `False` otherwise. Test your function by calling it and printing the result.

---

## 19. Functions with Parameters

### Passing Data to Functions

```python
# Function with one parameter
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
greet("Bob")

# Function with multiple parameters
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # 8

# Function with default parameters
def power(base, exponent=2):
    return base ** exponent

print(power(5))      # 25 (uses default exponent=2)
print(power(5, 3))   # 125 (overrides default)

# More complex example
def calculate_grade(score, bonus=0):
    total = score + bonus
    if total >= 90:
        return 'A'
    elif total >= 80:
        return 'B'
    elif total >= 70:
        return 'C'
    elif total >= 60:
        return 'D'
    else:
        return 'F'

print(calculate_grade(85))      # B
print(calculate_grade(85, 10))  # A
```

### Task 19.1
Write a function called `calculate_rectangle_area(length, width)` that returns the area of a rectangle. Write another function `calculate_rectangle_perimeter(length, width)` that returns the perimeter. Test both functions with different values.

---

## 20. Testing Functions

### Using Assertions and Unit Tests

```python
# Simple assertion testing
def add(a, b):
    return a + b

# Manual testing with assertions
assert add(2, 3) == 5, "Test failed: 2 + 3 should equal 5"
assert add(-1, 1) == 0, "Test failed: -1 + 1 should equal 0"
assert add(0, 0) == 0, "Test failed: 0 + 0 should equal 0"
print("All add() tests passed!")

# Using unittest module
import unittest

def multiply(a, b):
    return a * b

class TestMultiply(unittest.TestCase):
    def test_positive_numbers(self):
        self.assertEqual(multiply(3, 4), 12)
    
    def test_negative_numbers(self):
        self.assertEqual(multiply(-2, 5), -10)
    
    def test_zero(self):
        self.assertEqual(multiply(5, 0), 0)

# Run tests
if __name__ == '__main__':
    unittest.main(argv=[''], exit=False)
```

### Task 20.1
Write a function `is_palindrome(word)` that returns `True` if a word is a palindrome (reads the same forwards and backwards) and `False` otherwise. Write at least 3 assertions to test your function.

---

## 21. Lists (Arrays)

### Working with Collections

```python
# Creating lists
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# Accessing elements
print(fruits[0])   # apple
print(fruits[-1])  # cherry (last item)

# Modifying elements
fruits[1] = "blueberry"
print(fruits)  # ['apple', 'blueberry', 'cherry']

# Adding elements
fruits.append("date")           # Add to end
fruits.insert(1, "apricot")     # Insert at position

# Removing elements
fruits.remove("apple")          # Remove by value
last_fruit = fruits.pop()       # Remove and return last
specific_fruit = fruits.pop(0)  # Remove and return at index

# List operations
print(len(fruits))              # Length
print("banana" in fruits)       # Check membership

# Slicing
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(numbers[2:5])   # [2, 3, 4]
print(numbers[:4])    # [0, 1, 2, 3]
print(numbers[6:])    # [6, 7, 8, 9]
print(numbers[::2])   # [0, 2, 4, 6, 8] (every 2nd element)
```

### Task 21.1
Create a list of 5 student names. Write code to: add a new student at the end, remove the second student, print the first and last student, and print the total number of students.

---

## 22. List Iteration

### Looping Through Lists

```python
# Basic iteration
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)

# Iteration with index
for i in range(len(fruits)):
    print(f"{i}: {fruits[i]}")

# Better way with enumerate
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")

# Modifying list elements
numbers = [1, 2, 3, 4, 5]
for i in range(len(numbers)):
    numbers[i] = numbers[i] * 2
print(numbers)  # [2, 4, 6, 8, 10]

# List comprehension (concise way to create lists)
squares = [x**2 for x in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]

# Filtering with list comprehension
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
evens = [x for x in numbers if x % 2 == 0]
print(evens)  # [2, 4, 6, 8, 10]
```

### Task 22.1
Create a list of 10 numbers. Write code to: print all even numbers, calculate and print the sum of all numbers, and find and print the largest number.

---

## 23. For-Each Style Loops

### Pythonic Iteration

```python
# Python's for loop IS a for-each loop
names = ["Alice", "Bob", "Charlie"]

for name in names:
    print(f"Hello, {name}!")

# Iterating over different collections
# String
for char in "Python":
    print(char)

# Dictionary
person = {"name": "Alice", "age": 25, "city": "London"}

for key in person:
    print(f"{key}: {person[key]}")

# Better way for dictionaries
for key, value in person.items():
    print(f"{key}: {value}")

# Tuple unpacking
coordinates = [(1, 2), (3, 4), (5, 6)]
for x, y in coordinates:
    print(f"x={x}, y={y}")

# Using zip to iterate multiple lists
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]

for name, age in zip(names, ages):
    print(f"{name} is {age} years old")
```

### Task 23.1
Create two lists: one with 5 product names and one with 5 prices. Use a for-each style loop with `zip()` to print each product and its price in a formatted way.

---

## 24. Two-Dimensional Lists

### Lists of Lists

```python
# Creating a 2D list (matrix)
grid = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Accessing elements
print(grid[0][0])  # 1
print(grid[1][2])  # 6
print(grid[2][1])  # 8

# Modifying elements
grid[0][0] = 10
print(grid[0])  # [10, 2, 3]

# Iterating through 2D list
for row in grid:
    for element in row:
        print(element, end=" ")
    print()  # New line after each row

# With indices
for i in range(len(grid)):
    for j in range(len(grid[i])):
        print(f"grid[{i}][{j}] = {grid[i][j]}")

# Creating a 2D list with input
rows = 3
cols = 3
matrix = []
for i in range(rows):
    row = []
    for j in range(cols):
        value = int(input(f"Enter value for position [{i}][{j}]: "))
        row.append(value)
    matrix.append(row)
```

### Task 24.1
Create a 3x3 tic-tac-toe board (represented as a 2D list with strings "X", "O", or " "). Write code to print the board in a nice format, and then place an "X" at position [1][1] and print the board again.

---

## 25. Advanced Lists (like ArrayLists)

### Dynamic List Operations

```python
# Python lists are already dynamic (like ArrayList in Java)
my_list = []  # Empty list

# Adding elements
my_list.append(10)
my_list.append(20)
my_list.append(30)
print(my_list)  # [10, 20, 30]

# Inserting at specific position
my_list.insert(1, 15)
print(my_list)  # [10, 15, 20, 30]

# Extending with another list
my_list.extend([40, 50])
print(my_list)  # [10, 15, 20, 30, 40, 50]

# Removing elements
my_list.remove(15)  # Remove by value
print(my_list)  # [10, 20, 30, 40, 50]

# Checking if element exists
if 20 in my_list:
    print("20 is in the list")

# Finding index
index = my_list.index(30)
print(f"30 is at index {index}")

# Counting occurrences
my_list.append(20)
count = my_list.count(20)
print(f"20 appears {count} times")

# Clearing the list
# my_list.clear()
```

### Task 25.1
Create an empty list. Write a program that repeatedly asks the user to enter a number (or 'done' to finish). Store each number in the list, then print the list, its length, and the average of all numbers.

---

## 26. Searching Lists

### Finding Elements

```python
# Linear search
def linear_search(lst, target):
    for i in range(len(lst)):
        if lst[i] == target:
            return i  # Return index if found
    return -1  # Return -1 if not found

numbers = [10, 25, 30, 45, 50, 75]
result = linear_search(numbers, 30)
if result != -1:
    print(f"Found at index {result}")
else:
    print("Not found")

# Using built-in methods
if 30 in numbers:
    index = numbers.index(30)
    print(f"Found at index {index}")

# Binary search (requires sorted list)
def binary_search(lst, target):
    left = 0
    right = len(lst) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if lst[mid] == target:
            return mid
        elif lst[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

sorted_numbers = [5, 10, 15, 20, 25, 30, 35, 40]
result = binary_search(sorted_numbers, 20)
print(f"Found at index {result}")
```

### Task 26.1
Create a list of 10 random numbers between 1 and 100. Write a function that searches for a target number and returns how many comparisons were needed to find it (or to determine it's not there).

---

## 27. Iterators

### Working with Iterators

```python
# Creating an iterator from a list
my_list = [1, 2, 3, 4, 5]
my_iterator = iter(my_list)

# Using next() to get elements
print(next(my_iterator))  # 1
print(next(my_iterator))  # 2
print(next(my_iterator))  # 3

# Iterators in for loops (automatic)
for item in my_list:
    print(item)

# Custom iterator class
class Counter:
    def __init__(self, start, end):
        self.current = start
        self.end = end
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.current > self.end:
            raise StopIteration
        self.current += 1
        return self.current - 1

# Using custom iterator
counter = Counter(1, 5)
for num in counter:
    print(num)

# Generator functions (simpler way to create iterators)
def fibonacci(n):
    a, b = 0, 1
    count = 0
    while count < n:
        yield a
        a, b = b, a + b
        count += 1

# Using generator
for num in fibonacci(10):
    print(num, end=" ")
print()
```

### Task 27.1
Write a generator function `even_numbers(start, end)` that yields all even numbers between start and end. Test it by iterating over even numbers from 0 to 20.

---

## 28. File Input

### Reading from Files

```python
# Reading entire file
try:
    with open('data.txt', 'r') as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("File not found")

# Reading line by line
with open('data.txt', 'r') as file:
    for line in file:
        print(line.strip())  # strip() removes newline

# Reading into a list
with open('data.txt', 'r') as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())

# Reading and processing data
with open('numbers.txt', 'r') as file:
    numbers = []
    for line in file:
        number = int(line.strip())
        numbers.append(number)
    print(f"Sum: {sum(numbers)}")
    print(f"Average: {sum(numbers) / len(numbers)}")

# Reading CSV-style data
with open('data.csv', 'r') as file:
    for line in file:
        values = line.strip().split(',')
        print(values)
```

### Task 28.1
Create a text file called 'scores.txt' with 5 test scores (one per line). Write a program that reads the file and calculates the average score.

---

## 29. Writing Files

### Creating and Writing to Files

```python
# Writing to a file (overwrites existing content)
with open('output.txt', 'w') as file:
    file.write("Hello, World!\n")
    file.write("This is a new line.\n")

# Appending to a file
with open('output.txt', 'a') as file:
    file.write("This line is appended.\n")

# Writing a list to a file
names = ["Alice", "Bob", "Charlie"]
with open('names.txt', 'w') as file:
    for name in names:
        file.write(name + "\n")

# Writing formatted data
students = [
    {"name": "Alice", "grade": 85},
    {"name": "Bob", "grade": 92},
    {"name": "Charlie", "grade": 78}
]

with open('grades.txt', 'w') as file:
    for student in students:
        file.write(f"{student['name']}: {student['grade']}\n")

# Using print to write to file
with open('output.txt', 'w') as file:
    print("Line 1", file=file)
    print("Line 2", file=file)
```

### Task 29.1
Write a program that asks the user for 5 favorite movies and saves them to a file called 'movies.txt'. Then write another program that reads and displays all the movies from the file.

---

## 30. Debugging

### Finding and Fixing Errors

```python
# Syntax Errors - caught by Python before running
# if x == 5  # Missing colon

# Runtime Errors - happen during execution
# x = 10 / 0  # Division by zero

# Logical Errors - code runs but produces wrong results
def calculate_average(numbers):
    total = 0
    for num in numbers:
        total += num
    return total / len(numbers)  # What if numbers is empty?

# Using print statements for debugging
def buggy_function(x, y):
    print(f"Debug: x={x}, y={y}")  # Check values
    result = x + y
    print(f"Debug: result={result}")  # Check result
    return result

# Using assert for validation
def calculate_grade(score):
    assert 0 <= score <= 100, "Score must be between 0 and 100"
    if score >= 90:
        return 'A'
    elif score >= 80:
        return 'B'
    # ... etc

# Try-except for error handling
def safe_divide(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        print("Error: Cannot divide by zero")
        return None
    except TypeError:
        print("Error: Invalid types for division")
        return None

# Python debugger (pdb)
# import pdb
# pdb.set_trace()  # Execution will pause here
```

### Task 30.1
The following code has bugs. Find and fix them:
```python
def calculate_total(prices):
    total = 0
    for price in prices
        total += price
    return total

items = ["10", "20", "30"]
print("Total:", calculate_total(items))
```

---

## 31. Type Conversion

### Converting Between Types

```python
# String to number
age_str = "25"
age_int = int(age_str)
price_str = "19.99"
price_float = float(price_str)

# Number to string
age = 25
age_str = str(age)
message = "I am " + str(age) + " years old"

# String to boolean (not direct)
# Use comparison instead
yes_str = "yes"
is_yes = (yes_str.lower() == "yes")

# List to string
words = ["Hello", "World"]
sentence = " ".join(words)
print(sentence)  # "Hello World"

# String to list
text = "Hello World"
chars = list(text)
words = text.split()

# Integer to binary, octal, hex
number = 42
binary = bin(number)    # '0b101010'
octal = oct(number)     # '0o52'
hexadecimal = hex(number)  # '0x2a'

# Rounding and converting floats
value = 3.7
print(int(value))     # 3 (truncates)
print(round(value))   # 4 (rounds)

# Safe conversion with error handling
def safe_int_convert(value):
    try:
        return int(value)
    except ValueError:
        return None

result = safe_int_convert("abc")
if result is None:
    print("Conversion failed")
```

### Task 31.1
Write a program that asks the user for a decimal number. Convert and display it as an integer (truncated), a rounded integer, and a string. Also show the original number's type.

---

## 32. Formatting Data

### Making Output Look Nice

```python
# F-strings (Python 3.6+)
name = "Alice"
age = 25
height = 1.65

print(f"Name: {name}, Age: {age}, Height: {height}m")

# Formatting numbers
pi = 3.14159265359
print(f"Pi to 2 decimal places: {pi:.2f}")
print(f"Pi to 4 decimal places: {pi:.4f}")

big_number = 1234567890
print(f"Formatted with commas: {big_number:,}")

# Padding and alignment
print(f"{'Left':<10}|")    # Left aligned
print(f"{'Center':^10}|")  # Center aligned
print(f"{'Right':>10}|")   # Right aligned

# Padding with zeros
number = 42
print(f"{number:05d}")  # 00042

# Formatting in columns
products = [
    ("Apple", 1.50, 10),
    ("Banana", 0.75, 25),
    ("Cherry", 3.00, 5)
]

print(f"{'Product':<10} {'Price':>8} {'Quantity':>10}")
print("-" * 30)
for name, price, qty in products:
    print(f"{name:<10} ${price:>7.2f} {qty:>10}")

# Percentage formatting
ratio = 0.856
print(f"Success rate: {ratio:.1%}")

# Date formatting
from datetime import datetime
now = datetime.now()
print(f"Date: {now:%Y-%m-%d}")
print(f"Time: {now:%H:%M:%S}")
print(f"Full: {now:%Y-%m-%d %H:%M:%S}")
```

### Task 32.1
Create a list of 3 students with their names and grades. Print them in a nicely formatted table with headers, aligned columns, and grades shown to 1 decimal place.

---

## 33. Classes

### Object-Oriented Programming

```python
# Defining a class
class Student:
    def __init__(self, name, age):
        self.name = name  # Instance variable
        self.age = age
    
    def introduce(self):
        print(f"Hi, I'm {self.name} and I'm {self.age} years old")

# Creating objects (instances)
student1 = Student("Alice", 20)
student2 = Student("Bob", 22)

# Accessing attributes and methods
print(student1.name)  # Alice
student1.introduce()  # Hi, I'm Alice and I'm 20 years old

# Class with more functionality
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance
    
    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"Deposited ${amount}. New balance: ${self.balance}")
        else:
            print("Invalid amount")
    
    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient funds")
        elif amount > 0:
            self.balance -= amount
            print(f"Withdrew ${amount}. New balance: ${self.balance}")
        else:
            print("Invalid amount")
    
    def get_balance(self):
        return self.balance

# Using the class
account = BankAccount("Alice", 1000)
account.deposit(500)
account.withdraw(200)
print(f"Current balance: ${account.get_balance()}")
```

### Task 33.1
Create a `Book` class with attributes: title, author, and pages. Add a method `info()` that prints the book's information. Create 3 book objects and call the info() method on each.

---

## 34. Enumerations

### Using Enums

```python
from enum import Enum

# Defining an enum
class Day(Enum):
    MONDAY = 1
    TUESDAY = 2
    WEDNESDAY = 3
    THURSDAY = 4
    FRIDAY = 5
    SATURDAY = 6
    SUNDAY = 7

# Using enums
today = Day.MONDAY
print(today)        # Day.MONDAY
print(today.name)   # MONDAY
print(today.value)  # 1

# Comparing enums
if today == Day.MONDAY:
    print("Start of the week!")

# Iterating through enums
for day in Day:
    print(f"{day.name}: {day.value}")

# More practical example
class OrderStatus(Enum):
    PENDING = "pending"
    PROCESSING = "processing"
    SHIPPED = "shipped"
    DELIVERED = "delivered"
    CANCELLED = "cancelled"

class Order:
    def __init__(self, order_id):
        self.order_id = order_id
        self.status = OrderStatus.PENDING
    
    def ship(self):
        if self.status == OrderStatus.PROCESSING:
            self.status = OrderStatus.SHIPPED
            print(f"Order {self.order_id} has been shipped")
        else:
            print(f"Cannot ship order with status {self.status.value}")
    
    def get_status(self):
        return self.status.value

# Using the Order class
order = Order(12345)
print(order.get_status())  # pending
order.status = OrderStatus.PROCESSING
order.ship()  # Order 12345 has been shipped
```

### Task 34.1
Create an enum called `Priority` with values: LOW, MEDIUM, HIGH, URGENT. Create a `Task` class that has a title and priority. Create 3 tasks with different priorities and print them.

---

## 35. Mini Project - Student Management System

### Putting It All Together

```python
from enum import Enum

class Grade(Enum):
    A = 90
    B = 80
    C = 70
    D = 60
    F = 0

class Student:
    def __init__(self, name, student_id):
        self.name = name
        self.student_id = student_id
        self.grades = []
    
    def add_grade(self, grade):
        if 0 <= grade <= 100:
            self.grades.append(grade)
        else:
            print("Invalid grade")
    
    def get_average(self):
        if len(self.grades) == 0:
            return 0
        return sum(self.grades) / len(self.grades)
    
    def get_letter_grade(self):
        avg = self.get_average()
        if avg >= Grade.A.value:
            return 'A'
        elif avg >= Grade.B.value:
            return 'B'
        elif avg >= Grade.C.value:
            return 'C'
        elif avg >= Grade.D.value:
            return 'D'
        else:
            return 'F'
    
    def display_info(self):
        print(f"\nStudent: {self.name}")
        print(f"ID: {self.student_id}")
        print(f"Grades: {self.grades}")
        print(f"Average: {self.get_average():.2f}")
        print(f"Letter Grade: {self.get_letter_grade()}")

class StudentManagementSystem:
    def __init__(self):
        self.students = []
    
    def add_student(self, student):
        self.students.append(student)
    
    def find_student(self, student_id):
        for student in self.students:
            if student.student_id == student_id:
                return student
        return None
    
    def display_all_students(self):
        if len(self.students) == 0:
            print("No students in system")
        for student in self.students:
            student.display_info()

# Example usage
sms = StudentManagementSystem()

# Create and add students
s1 = Student("Alice", 1001)
s1.add_grade(95)
s1.add_grade(87)
s1.add_grade(92)

s2 = Student("Bob", 1002)
s2.add_grade(78)
s2.add_grade(84)
s2.add_grade(81)

sms.add_student(s1)
sms.add_student(s2)

# Display all students
sms.display_all_students()
```

### Task 35.1
Extend the Student Management System by adding a `remove_student(student_id)` method that removes a student from the system. Also add a method to find the student with the highest average grade.

---

## 36. Sorting

### Ordering Data

```python
# Sorting lists
numbers = [64, 34, 25, 12, 22, 11, 90]

# Built-in sort (modifies list)
numbers.sort()
print(numbers)  # [11, 12, 22, 25, 34, 64, 90]

# Sort in descending order
numbers.sort(reverse=True)
print(numbers)  # [90, 64, 34, 25, 22, 12, 11]

# sorted() function (returns new list)
original = [3, 1, 4, 1, 5, 9, 2, 6]
sorted_list = sorted(original)
print(original)     # [3, 1, 4, 1, 5, 9, 2, 6] - unchanged
print(sorted_list)  # [1, 1, 2, 3, 4, 5, 6, 9]

# Sorting strings
names = ["Charlie", "Alice", "Bob", "David"]
names.sort()
print(names)  # ['Alice', 'Bob', 'Charlie', 'David']

# Sorting with custom key
students = [
    {"name": "Alice", "grade": 85},
    {"name": "Bob", "grade": 92},
    {"name": "Charlie", "grade": 78}
]

# Sort by grade
students.sort(key=lambda x: x["grade"])
for student in students:
    print(f"{student['name']}: {student['grade']}")

# Bubble sort implementation
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

test_list = [64, 34, 25, 12, 22, 11, 90]
print(bubble_sort(test_list))
```

### Task 36.1
Create a list of 10 random numbers between 1 and 100. Implement a selection sort algorithm to sort them in ascending order. Print the list before and after sorting.

---

## 37. Inheritance

### Code Reuse Through Class Hierarchies

```python
# Base class (parent class)
class Animal:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def make_sound(self):
        print("Some generic sound")
    
    def info(self):
        print(f"Name: {self.name}, Age: {self.age}")

# Derived class (child class)
class Dog(Animal):
    def __init__(self, name, age, breed):
        super().__init__(name, age)  # Call parent constructor
        self.breed = breed
    
    def make_sound(self):
        print("Woof! Woof!")
    
    def fetch(self):
        print(f"{self.name} is fetching the ball")

class Cat(Animal):
    def __init__(self, name, age, color):
        super().__init__(name, age)
        self.color = color
    
    def make_sound(self):
        print("Meow!")
    
    def scratch(self):
        print(f"{self.name} is scratching furniture")

# Using inheritance
dog = Dog("Buddy", 3, "Golden Retriever")
dog.info()         # Inherited method
dog.make_sound()   # Overridden method
dog.fetch()        # Dog-specific method

cat = Cat("Whiskers", 2, "Orange")
cat.info()
cat.make_sound()
cat.scratch()

# More complex example
class Vehicle:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
        self.is_running = False
    
    def start(self):
        self.is_running = True
        print(f"{self.brand} {self.model} started")
    
    def stop(self):
        self.is_running = False
        print(f"{self.brand} {self.model} stopped")

class Car(Vehicle):
    def __init__(self, brand, model, doors):
        super().__init__(brand, model)
        self.doors = doors
    
    def honk(self):
        print("Beep beep!")

class Motorcycle(Vehicle):
    def __init__(self, brand, model, cc):
        super().__init__(brand, model)
        self.cc = cc
    
    def wheelie(self):
        print("Doing a wheelie!")

car = Car("Toyota", "Camry", 4)
car.start()
car.honk()
car.stop()
```

### Task 37.1
Create a `Person` base class with name and age. Create two derived classes: `Student` (with student_id and major) and `Teacher` (with subject and years_experience). Add appropriate methods to each class.

---

## 38. Method Overriding

### Customizing Inherited Behavior

```python
# Base class
class Shape:
    def __init__(self, color):
        self.color = color
    
    def area(self):
        return 0
    
    def perimeter(self):
        return 0
    
    def description(self):
        return f"A {self.color} shape"

# Derived classes with overridden methods
class Rectangle(Shape):
    def __init__(self, color, width, height):
        super().__init__(color)
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)
    
    def description(self):
        base_desc = super().description()  # Call parent method
        return f"{base_desc} - Rectangle with area {self.area()}"

class Circle(Shape):
    def __init__(self, color, radius):
        super().__init__(color)
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2
    
    def perimeter(self):
        return 2 * 3.14159 * self.radius
    
    def description(self):
        return f"A {self.color} circle with area {self.area():.2f}"

# Using the classes
rect = Rectangle("blue", 5, 3)
print(rect.description())
print(f"Area: {rect.area()}")
print(f"Perimeter: {rect.perimeter()}")

circle = Circle("red", 4)
print(circle.description())
print(f"Area: {circle.area():.2f}")
print(f"Perimeter: {circle.perimeter():.2f}")

# Example with __str__ override
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price
    
    def __str__(self):
        return f"Product: {self.name}, Price: ${self.price:.2f}"

product = Product("Laptop", 999.99)
print(product)  # Calls __str__ automatically
```

### Task 38.1
Create a base class `Employee` with a method `calculate_salary()` that returns a base salary of 30000. Create two derived classes: `Manager` (salary = base + 20000) and `Developer` (salary = base + 15000). Override the calculate_salary() method in each derived class.

---

## 39. Saving Objects to Files

### Persistence with Pickle

```python
import pickle

# Simple class
class Student:
    def __init__(self, name, age, grades):
        self.name = name
        self.age = age
        self.grades = grades
    
    def __str__(self):
        return f"Student: {self.name}, Age: {self.age}, Grades: {self.grades}"

# Creating objects
students = [
    Student("Alice", 20, [85, 90, 92]),
    Student("Bob", 21, [78, 84, 81]),
    Student("Charlie", 19, [92, 95, 88])
]

# Saving objects to file
with open('students.pkl', 'wb') as file:
    pickle.dump(students, file)

print("Objects saved to file")

# Loading objects from file
with open('students.pkl', 'rb') as file:
    loaded_students = pickle.load(file)

print("\nLoaded objects from file:")
for student in loaded_students:
    print(student)

# Saving a single object
student1 = Student("David", 22, [88, 91, 85])

with open('single_student.pkl', 'wb') as file:
    pickle.dump(student1, file)

with open('single_student.pkl', 'rb') as file:
    loaded_student = pickle.load(file)

print(f"\nLoaded single student: {loaded_student}")

# Alternative: JSON for simple data
import json

# For simple data structures (dictionaries)
students_dict = [
    {"name": "Alice", "age": 20, "grades": [85, 90, 92]},
    {"name": "Bob", "age": 21, "grades": [78, 84, 81]}
]

# Save as JSON
with open('students.json', 'w') as file:
    json.dump(students_dict, file, indent=2)

# Load from JSON
with open('students.json', 'r') as file:
    loaded_data = json.load(file)

print("\nLoaded from JSON:")
print(loaded_data)
```

### Task 39.1
Create a `Book` class with title, author, and year. Create a list of 3 books, save them to a file using pickle, then load them back and display them.

---

## 40. Method Overloading

### Multiple Methods with Different Parameters

Python doesn't have traditional method overloading like Java, but we can achieve similar results:

```python
# Using default arguments
class Calculator:
    def add(self, a, b=0, c=0):
        return a + b + c

calc = Calculator()
print(calc.add(5))         # 5
print(calc.add(5, 3))      # 8
print(calc.add(5, 3, 2))   # 10

# Using *args for variable arguments
class MathOperations:
    def add(self, *args):
        return sum(args)
    
    def multiply(self, *args):
        result = 1
        for num in args:
            result *= num
        return result

math_ops = MathOperations()
print(math_ops.add(1, 2, 3, 4, 5))        # 15
print(math_ops.multiply(2, 3, 4))         # 24

# Using type checking for different behaviors
class Printer:
    def print_data(self, data):
        if isinstance(data, int):
            print(f"Integer: {data}")
        elif isinstance(data, str):
            print(f"String: {data}")
        elif isinstance(data, list):
            print(f"List: {', '.join(map(str, data))}")
        else:
            print(f"Unknown type: {data}")

printer = Printer()
printer.print_data(42)
printer.print_data("Hello")
printer.print_data([1, 2, 3])

# Using functools.singledispatch (Python 3.4+)
from functools import singledispatch

@singledispatch
def process(arg):
    print(f"Default: {arg}")

@process.register(int)
def _(arg):
    print(f"Integer: {arg * 2}")

@process.register(str)
def _(arg):
    print(f"String: {arg.upper()}")

@process.register(list)
def _(arg):
    print(f"List sum: {sum(arg)}")

process(5)           # Integer: 10
process("hello")     # String: HELLO
process([1, 2, 3])   # List sum: 6
```

### Task 40.1
Create a `Shape` class with a method `create()` that can accept different numbers of parameters: 1 parameter for Circle (radius), 2 for Rectangle (width, height), or 3 for Triangle (side1, side2, side3). Use *args to handle this.

---

## 41. Polymorphism

### Using Different Types Interchangeably

```python
# Polymorphism through inheritance
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

class Cow(Animal):
    def speak(self):
        return "Moo!"

# Polymorphism in action
animals = [Dog(), Cat(), Cow(), Dog()]

for animal in animals:
    print(animal.speak())

# Function that works with any animal
def make_animal_speak(animal):
    print(animal.speak())

make_animal_speak(Dog())
make_animal_speak(Cat())

# Polymorphism with different shapes
class Shape:
    def area(self):
        pass
    
    def perimeter(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2
    
    def perimeter(self):
        return 2 * 3.14159 * self.radius

# Using polymorphism
shapes = [
    Rectangle(5, 3),
    Circle(4),
    Rectangle(10, 2),
    Circle(7)
]

total_area = 0
for shape in shapes:
    area = shape.area()
    print(f"Area: {area:.2f}")
    total_area += area

print(f"Total area: {total_area:.2f}")

# Duck typing (Python's approach to polymorphism)
class PaymentProcessor:
    def process_payment(self, amount):
        pass

class CreditCardProcessor(PaymentProcessor):
    def process_payment(self, amount):
        print(f"Processing ${amount} via Credit Card")

class PayPalProcessor(PaymentProcessor):
    def process_payment(self, amount):
        print(f"Processing ${amount} via PayPal")

class CryptoProcessor(PaymentProcessor):
    def process_payment(self, amount):
        print(f"Processing ${amount} via Cryptocurrency")

def checkout(processor, amount):
    processor.process_payment(amount)

checkout(CreditCardProcessor(), 100.50)
checkout(PayPalProcessor(), 75.25)
checkout(CryptoProcessor(), 200.00)
```

### Task 41.1
Create a base class `Vehicle` with a method `move()`. Create three derived classes: `Car`, `Boat`, and `Plane`, each with their own implementation of `move()`. Create a list of different vehicles and call `move()` on each one.

---

## 42. Basic GUI with Tkinter

### Creating Graphical User Interfaces

```python
import tkinter as tk
from tkinter import messagebox

# Simple window
def simple_window():
    window = tk.Tk()
    window.title("My First GUI")
    window.geometry("300x200")
    
    label = tk.Label(window, text="Hello, GUI!", font=("Arial", 16))
    label.pack(pady=20)
    
    window.mainloop()

# Window with button
def button_window():
    def button_clicked():
        label.config(text="Button was clicked!")
    
    window = tk.Tk()
    window.title("Button Example")
    window.geometry("300x200")
    
    label = tk.Label(window, text="Click the button")
    label.pack(pady=10)
    
    button = tk.Button(window, text="Click Me!", command=button_clicked)
    button.pack(pady=10)
    
    window.mainloop()

# Window with entry (text input)
def entry_window():
    def submit_clicked():
        name = entry.get()
        messagebox.showinfo("Hello", f"Hello, {name}!")
    
    window = tk.Tk()
    window.title("Entry Example")
    window.geometry("300x200")
    
    label = tk.Label(window, text="Enter your name:")
    label.pack(pady=10)
    
    entry = tk.Entry(window, width=30)
    entry.pack(pady=10)
    
    button = tk.Button(window, text="Submit", command=submit_clicked)
    button.pack(pady=10)
    
    window.mainloop()

# Calculator GUI
def calculator_gui():
    def calculate():
        try:
            num1 = float(entry1.get())
            num2 = float(entry2.get())
            operation = operation_var.get()
            
            if operation == "+":
                result = num1 + num2
            elif operation == "-":
                result = num1 - num2
            elif operation == "*":
                result = num1 * num2
            elif operation == "/":
                if num2 == 0:
                    messagebox.showerror("Error", "Cannot divide by zero")
                    return
                result = num1 / num2
            
            result_label.config(text=f"Result: {result:.2f}")
        except ValueError:
            messagebox.showerror("Error", "Please enter valid numbers")
    
    window = tk.Tk()
    window.title("Calculator")
    window.geometry("300x250")
    
    tk.Label(window, text="Number 1:").pack(pady=5)
    entry1 = tk.Entry(window, width=20)
    entry1.pack(pady=5)
    
    tk.Label(window, text="Number 2:").pack(pady=5)
    entry2 = tk.Entry(window, width=20)
    entry2.pack(pady=5)
    
    tk.Label(window, text="Operation:").pack(pady=5)
    operation_var = tk.StringVar(value="+")
    operations_frame = tk.Frame(window)
    operations_frame.pack(pady=5)
    
    for op in ["+", "-", "*", "/"]:
        tk.Radiobutton(operations_frame, text=op, variable=operation_var, 
                      value=op).pack(side=tk.LEFT)
    
    tk.Button(window, text="Calculate", command=calculate).pack(pady=10)
    
    result_label = tk.Label(window, text="Result: ", font=("Arial", 12))
    result_label.pack(pady=10)
    
    window.mainloop()

# Uncomment to run
# calculator_gui()
```

### Task 42.1
Create a GUI application with a text entry field and a button. When the button is clicked, display the text in uppercase in a label below the button.

---

## 43. ComboBox (Dropdown) Selections

### Creating Dropdown Menus

```python
import tkinter as tk
from tkinter import ttk, messagebox

def combobox_example():
    def on_select():
        selected = combo.get()
        result_label.config(text=f"You selected: {selected}")
    
    window = tk.Tk()
    window.title("ComboBox Example")
    window.geometry("300x200")
    
    label = tk.Label(window, text="Choose a programming language:")
    label.pack(pady=10)
    
    # Create ComboBox
    languages = ["Python", "Java", "C++", "JavaScript", "C#"]
    combo = ttk.Combobox(window, values=languages, state="readonly")
    combo.set("Python")  # Default value
    combo.pack(pady=10)
    
    button = tk.Button(window, text="Select", command=on_select)
    button.pack(pady=10)
    
    result_label = tk.Label(window, text="")
    result_label.pack(pady=10)
    
    window.mainloop()

# Country and city selection
def cascading_combobox():
    def on_country_select(event):
        country = country_combo.get()
        if country == "USA":
            city_combo['values'] = ["New York", "Los Angeles", "Chicago"]
        elif country == "UK":
            city_combo['values'] = ["London", "Manchester", "Birmingham"]
        elif country == "Canada":
            city_combo['values'] = ["Toronto", "Vancouver", "Montreal"]
        city_combo.set("")  # Clear selection
    
    def submit():
        country = country_combo.get()
        city = city_combo.get()
        if country and city:
            messagebox.showinfo("Selection", f"You selected: {city}, {country}")
        else:
            messagebox.showwarning("Warning", "Please select both country and city")
    
    window = tk.Tk()
    window.title("Cascading ComboBox")
    window.geometry("300x250")
    
    tk.Label(window, text="Select Country:").pack(pady=5)
    countries = ["USA", "UK", "Canada"]
    country_combo = ttk.Combobox(window, values=countries, state="readonly")
    country_combo.pack(pady=5)
    country_combo.bind("<<ComboboxSelected>>", on_country_select)
    
    tk.Label(window, text="Select City:").pack(pady=5)
    city_combo = ttk.Combobox(window, state="readonly")
    city_combo.pack(pady=5)
    
    tk.Button(window, text="Submit", command=submit).pack(pady=20)
    
    window.mainloop()

# Uncomment to run
# combobox_example()
```

### Task 43.1
Create a GUI application with two ComboBoxes: one for selecting a category (Electronics, Clothing, Books) and one for selecting items within that category. When the category changes, update the items ComboBox with relevant items.

---

## 44. Modal Dialogs with Message Boxes

### Using Dialog Boxes

```python
import tkinter as tk
from tkinter import messagebox, simpledialog

def messagebox_example():
    window = tk.Tk()
    window.title("MessageBox Examples")
    window.geometry("300x300")
    
    def show_info():
        messagebox.showinfo("Information", "This is an info message")
    
    def show_warning():
        messagebox.showwarning("Warning", "This is a warning message")
    
    def show_error():
        messagebox.showerror("Error", "This is an error message")
    
    def ask_question():
        result = messagebox.askyesno("Question", "Do you want to continue?")
        if result:
            messagebox.showinfo("Result", "You clicked Yes")
        else:
            messagebox.showinfo("Result", "You clicked No")
    
    def ask_ok_cancel():
        result = messagebox.askokcancel("Confirm", "Are you sure?")
        label.config(text=f"Result: {result}")
    
    def ask_retry_cancel():
        result = messagebox.askretrycancel("Retry", "Operation failed. Retry?")
        label.config(text=f"Retry: {result}")
    
    tk.Button(window, text="Show Info", command=show_info, width=20).pack(pady=5)
    tk.Button(window, text="Show Warning", command=show_warning, width=20).pack(pady=5)
    tk.Button(window, text="Show Error", command=show_error, width=20).pack(pady=5)
    tk.Button(window, text="Ask Yes/No", command=ask_question, width=20).pack(pady=5)
    tk.Button(window, text="Ask OK/Cancel", command=ask_ok_cancel, width=20).pack(pady=5)
    tk.Button(window, text="Ask Retry/Cancel", command=ask_retry_cancel, width=20).pack(pady=5)
    
    label = tk.Label(window, text="")
    label.pack(pady=10)
    
    window.mainloop()

# Simple dialog for input
def input_dialog_example():
    window = tk.Tk()
    window.title("Input Dialog")
    window.geometry("300x200")
    
    def get_string():
        name = simpledialog.askstring("Input", "Enter your name:")
        if name:
            result_label.config(text=f"Hello, {name}!")
    
    def get_integer():
        age = simpledialog.askinteger("Input", "Enter your age:", minvalue=0, maxvalue=120)
        if age:
            result_label.config(text=f"You are {age} years old")
    
    def get_float():
        height = simpledialog.askfloat("Input", "Enter your height (m):", minvalue=0.0, maxvalue=3.0)
        if height:
            result_label.config(text=f"Your height is {height}m")
    
    tk.Button(window, text="Enter Name", command=get_string, width=20).pack(pady=10)
    tk.Button(window, text="Enter Age", command=get_integer, width=20).pack(pady=10)
    tk.Button(window, text="Enter Height", command=get_float, width=20).pack(pady=10)
    
    result_label = tk.Label(window, text="")
    result_label.pack(pady=10)
    
    window.mainloop()

# Uncomment to run
# messagebox_example()
# input_dialog_example()
```

### Task 44.1
Create a simple quiz application. Display a question in the GUI, and when the user clicks "Submit", use a messagebox to tell them if they're correct or incorrect.

---

## 45. Dynamic GUI Elements

### Creating Interface Elements Programmatically

```python
import tkinter as tk
from tkinter import ttk

def dynamic_widgets():
    window = tk.Tk()
    window.title("Dynamic Widgets")
    window.geometry("400x400")
    
    widgets_frame = tk.Frame(window)
    widgets_frame.pack(pady=10)
    
    widgets_list = []
    
    def add_label():
        label = tk.Label(widgets_frame, text=f"Label {len(widgets_list) + 1}", 
                        bg="lightblue", padx=10, pady=5)
        label.pack(pady=5)
        widgets_list.append(label)
    
    def add_button():
        def button_action():
            tk.messagebox.showinfo("Clicked", f"Button {len(widgets_list)} was clicked!")
        
        button = tk.Button(widgets_frame, text=f"Button {len(widgets_list) + 1}",
                          command=button_action)
        button.pack(pady=5)
        widgets_list.append(button)
    
    def add_entry():
        entry = tk.Entry(widgets_frame, width=30)
        entry.insert(0, f"Entry {len(widgets_list) + 1}")
        entry.pack(pady=5)
        widgets_list.append(entry)
    
    def clear_all():
        for widget in widgets_list:
            widget.destroy()
        widgets_list.clear()
    
    # Control buttons
    control_frame = tk.Frame(window)
    control_frame.pack(pady=10)
    
    tk.Button(control_frame, text="Add Label", command=add_label).pack(side=tk.LEFT, padx=5)
    tk.Button(control_frame, text="Add Button", command=add_button).pack(side=tk.LEFT, padx=5)
    tk.Button(control_frame, text="Add Entry", command=add_entry).pack(side=tk.LEFT, padx=5)
    tk.Button(control_frame, text="Clear All", command=clear_all).pack(side=tk.LEFT, padx=5)
    
    window.mainloop()

# Todo list example
def todo_list_app():
    window = tk.Tk()
    window.title("Todo List")
    window.geometry("400x500")
    
    tasks = []
    
    def add_task():
        task_text = entry.get()
        if task_text:
            task_frame = tk.Frame(tasks_container)
            task_frame.pack(fill=tk.X, pady=2)
            
            var = tk.BooleanVar()
            checkbutton = tk.Checkbutton(task_frame, variable=var)
            checkbutton.pack(side=tk.LEFT)
            
            label = tk.Label(task_frame, text=task_text, anchor="w")
            label.pack(side=tk.LEFT, fill=tk.X, expand=True)
            
            def delete_task():
                task_frame.destroy()
                tasks.remove((task_frame, var, label))
            
            delete_btn = tk.Button(task_frame, text="Delete", command=delete_task)
            delete_btn.pack(side=tk.RIGHT)
            
            tasks.append((task_frame, var, label))
            entry.delete(0, tk.END)
    
    def clear_completed():
        for task_frame, var, label in tasks[:]:
            if var.get():
                task_frame.destroy()
                tasks.remove((task_frame, var, label))
    
    # Entry frame
    entry_frame = tk.Frame(window)
    entry_frame.pack(pady=10, padx=10, fill=tk.X)
    
    entry = tk.Entry(entry_frame)
    entry.pack(side=tk.LEFT, fill=tk.X, expand=True)
    entry.bind('<Return>', lambda e: add_task())
    
    add_btn = tk.Button(entry_frame, text="Add", command=add_task)
    add_btn.pack(side=tk.RIGHT, padx=5)
    
    # Control buttons
    control_frame = tk.Frame(window)
    control_frame.pack(pady=5)
    
    tk.Button(control_frame, text="Clear Completed", command=clear_completed).pack()
    
    # Tasks container
    tasks_container = tk.Frame(window)
    tasks_container.pack(fill=tk.BOTH, expand=True, padx=10, pady=10)
    
    window.mainloop()

# Uncomment to run
# todo_list_app()
```

### Task 45.1
Create a contact list application where users can dynamically add contacts (name and phone number). Each contact should appear in the list with a "Delete" button next to it.

---

## Conclusion

Congratulations on completing this Python programming tutorial! You've covered:

- **Basics**: Variables, data types, operators
- **Control Flow**: If statements, loops, match statements
- **Functions**: Creating and using functions, parameters, testing
- **Collections**: Lists, 2D lists, iteration
- **File I/O**: Reading and writing files
- **OOP**: Classes, inheritance, polymorphism
- **GUI**: Tkinter basics, widgets, events
- **Advanced**: Enums, sorting, object persistence

## Next Steps

1. **Practice**: Complete all the tasks in this tutorial
2. **Build Projects**: Create your own programs combining these concepts
3. **Explore Libraries**: Learn about NumPy, Pandas, Django, Flask, etc.
4. **Read Documentation**: https://docs.python.org/3/
5. **Join Communities**: Python forums, Stack Overflow, Reddit's r/learnpython

Keep coding and exploring!