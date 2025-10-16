# Lecture 2: Conditional Statements in Python - If, Elif, and Match-Case

**Duration:** 90 minutes

**Prerequisites:** Week 1 - Python Basics (variables, data types, basic operators)

---

## Learning Objectives

By the end of this lecture, students should be able to:

1. **Write** basic if statements to control program flow based on conditions (15 min)
2. **Construct** complex conditional logic using if-else and if-elif-else structures (20 min)
3. **Apply** comparison and logical operators to create compound conditions (15 min)
4. **Implement** match-case statements (Python 3.10+) for pattern matching (15 min)
5. **Evaluate** which conditional structure is most appropriate for a given problem (10 min)
6. **Debug** common errors in conditional statements including indentation and logic errors (10 min)

---

## Section 1: Introduction to Control Flow (5 minutes)

### Overview
Introduction to the concept of control flow and why we need conditional statements in programming.

### Content
- **What is Control Flow?**
  - Sequential execution vs. conditional execution
  - Making decisions in code based on conditions
  - Real-world analogies (e.g., "If it rains, take an umbrella")

- **Why Conditional Statements Matter**
  - Programs need to respond to different inputs
  - Enabling dynamic behavior
  - Examples: login validation, game logic, form processing

---

## Section 2: Basic If Statements (15 minutes)

### Overview
Understanding the syntax and structure of basic if statements in Python.

### 2.1 If Statement Syntax

**Basic Structure:**
```python
if condition:
    # code to execute if condition is True
    statement1
    statement2
```

**Key Points:**
- Condition must evaluate to a boolean value (True/False)
- Colon (`:`) is required after the condition
- Indentation (typically 4 spaces) defines the code block
- No braces `{}` needed (unlike Java)

### 2.2 Comparison Operators

Python comparison operators:
```python
==    # Equal to
!=    # Not equal to
>     # Greater than
<     # Less than
>=    # Greater than or equal to
<=    # Less than or equal to
```

### 2.3 Examples

**Example 1: Simple Age Check**
```python
age = 18

if age >= 18:
    print("You are eligible to vote")
    print("Please register at your local office")
```

**Example 2: Temperature Warning**
```python
temperature = 35

if temperature > 30:
    print("It's hot outside!")
    print("Stay hydrated")
```

**Example 3: Password Length Validation**
```python
password = "mypass"

if len(password) < 8:
    print("Password is too short")
    print("Please use at least 8 characters")
```

### 2.4 Truthy and Falsy Values in Python

Python has a concept of "truthiness":
```python
# Falsy values: False, None, 0, 0.0, '', [], {}, ()
# Everything else is Truthy

name = "Alice"
if name:  # Truthy - string is not empty
    print(f"Hello, {name}!")

items = []
if items:  # Falsy - list is empty
    print("You have items")
```

---

## Section 3: If-Else Statements (10 minutes)

### Overview
Adding alternative execution paths with else clauses.

### 3.1 If-Else Syntax

```python
if condition:
    # code if condition is True
    statement1
else:
    # code if condition is False
    statement2
```

### 3.2 Examples

**Example 1: Even or Odd**
```python
number = 7

if number % 2 == 0:
    print(f"{number} is even")
else:
    print(f"{number} is odd")
```

**Example 2: Pass or Fail**
```python
score = 55

if score >= 60:
    print("Congratulations! You passed.")
    grade = "Pass"
else:
    print("Sorry, you did not pass.")
    grade = "Fail"

print(f"Your grade: {grade}")
```

**Example 3: Positive or Negative**
```python
value = -5

if value >= 0:
    print("The number is positive or zero")
else:
    print("The number is negative")
```

---

## Section 4: Elif (Else-If) Statements (12 minutes)

### Overview
Handling multiple conditions with elif chains.

### 4.1 Elif Syntax

```python
if condition1:
    # code if condition1 is True
    statement1
elif condition2:
    # code if condition2 is True (and condition1 is False)
    statement2
elif condition3:
    # code if condition3 is True (and previous conditions are False)
    statement3
else:
    # code if all conditions are False
    statement4
```

### 4.2 Important Notes
- Python evaluates conditions **top to bottom**
- First True condition executes, then exits the entire if-elif-else block
- Order matters! More specific conditions should come first
- `else` is optional and catches all other cases

### 4.3 Examples

**Example 1: Letter Grading System**
```python
score = 85

if score >= 90:
    grade = 'A'
    print("Excellent work!")
elif score >= 80:
    grade = 'B'
    print("Great job!")
elif score >= 70:
    grade = 'C'
    print("Good effort!")
elif score >= 60:
    grade = 'D'
    print("You passed, but consider reviewing the material.")
else:
    grade = 'F'
    print("Unfortunately, you did not pass.")

print(f"Your grade is: {grade}")
```

**Example 2: Day of Week**
```python
day = 3

if day == 1:
    print("Monday - Start of the work week")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday - Midweek")
elif day == 4:
    print("Thursday")
elif day == 5:
    print("Friday - Almost weekend!")
elif day == 6:
    print("Saturday - Weekend!")
elif day == 7:
    print("Sunday - Weekend!")
else:
    print("Invalid day number")
```

**Example 3: BMI Calculator**
```python
bmi = 22.5

if bmi < 18.5:
    category = "Underweight"
elif bmi < 25:
    category = "Normal weight"
elif bmi < 30:
    category = "Overweight"
else:
    category = "Obese"

print(f"BMI Category: {category}")
```

---

## Section 5: Logical Operators (8 minutes)

### Overview
Combining multiple conditions using logical operators.

### 5.1 Python Logical Operators

```python
and    # Both conditions must be True
or     # At least one condition must be True
not    # Negates a condition
```

### 5.2 Examples

**Example 1: Using `and`**
```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive")
else:
    print("You cannot drive")
```

**Example 2: Using `or`**
```python
day = "Saturday"

if day == "Saturday" or day == "Sunday":
    print("It's the weekend!")
else:
    print("It's a weekday")
```

**Example 3: Using `not`**
```python
is_raining = False

if not is_raining:
    print("You don't need an umbrella")
else:
    print("Take an umbrella")
```

**Example 4: Complex Conditions**
```python
age = 20
is_student = True
income = 15000

if (age >= 18 and age <= 25) and (is_student or income < 20000):
    print("You qualify for a student discount")
else:
    print("Regular pricing applies")
```

### 5.3 Order of Operations
- `not` has highest precedence
- `and` is evaluated before `or`
- Use parentheses `()` for clarity

---

## Section 6: Nested If Statements (8 minutes)

### Overview
Placing if statements inside other if statements for complex decision-making.

### 6.1 Nested If Structure

```python
if condition1:
    if condition2:
        # code if both condition1 AND condition2 are True
        statement1
    else:
        # code if condition1 is True but condition2 is False
        statement2
else:
    # code if condition1 is False
    statement3
```

### 6.2 Examples

**Example 1: Age and ID Check**
```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("Entry granted")
    else:
        print("You need to show ID")
else:
    print("You must be 18 or older")
```

**Example 2: Login System**
```python
username = "admin"
password = "secure123"

if username == "admin":
    if password == "secure123":
        print("Login successful!")
        print("Welcome, Administrator")
    else:
        print("Incorrect password")
else:
    print("User not found")
```

### 6.3 When to Use Nested vs. Logical Operators

Often, nested if statements can be replaced with `and`:
```python
# Nested (less preferred)
if age >= 18:
    if has_license:
        print("Can drive")

# Using 'and' (preferred - more readable)
if age >= 18 and has_license:
    print("Can drive")
```

**Use nested if when:**
- Different error messages needed for each condition
- Additional logic required between checks
- Improving readability for complex scenarios

---

## Section 7: Match-Case Statements (15 minutes)

### Overview
Introduction to Python's match-case statement (Python 3.10+) as an alternative to multiple elif statements.

### 7.1 Why Match-Case?

**Comparison with Java Switch:**
- Java has `switch` statements
- Python (before 3.10) only had if-elif chains
- Python 3.10+ introduced `match-case` (structural pattern matching)
- More powerful than traditional switch statements

### 7.2 Basic Match-Case Syntax

```python
match variable:
    case value1:
        # code if variable == value1
        statement1
    case value2:
        # code if variable == value2
        statement2
    case _:
        # default case (like 'else')
        statement3
```

### 7.3 Examples

**Example 1: Day of Week (Improved)**
```python
day = 3

match day:
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case 4:
        print("Thursday")
    case 5:
        print("Friday")
    case 6 | 7:  # Multiple values
        print("Weekend!")
    case _:
        print("Invalid day")
```

**Example 2: Menu Selection**
```python
choice = "B"

match choice:
    case "A":
        print("You selected: Create new account")
    case "B":
        print("You selected: Login")
    case "C":
        print("You selected: View profile")
    case "D":
        print("You selected: Exit")
    case _:
        print("Invalid option. Please try again.")
```

**Example 3: HTTP Status Codes**
```python
status_code = 404

match status_code:
    case 200:
        print("OK - Success")
    case 201:
        print("Created")
    case 400:
        print("Bad Request")
    case 401:
        print("Unauthorized")
    case 404:
        print("Not Found")
    case 500:
        print("Internal Server Error")
    case _:
        print("Unknown status code")
```

### 7.4 Advanced Match-Case Features

**Matching Multiple Values (OR patterns):**
```python
month = "December"

match month:
    case "December" | "January" | "February":
        print("Winter")
    case "March" | "April" | "May":
        print("Spring")
    case "June" | "July" | "August":
        print("Summer")
    case "September" | "October" | "November":
        print("Autumn")
    case _:
        print("Invalid month")
```

**Matching with Guards (conditions):**
```python
score = 85

match score:
    case s if s >= 90:
        print("Grade: A")
    case s if s >= 80:
        print("Grade: B")
    case s if s >= 70:
        print("Grade: C")
    case s if s >= 60:
        print("Grade: D")
    case _:
        print("Grade: F")
```

### 7.5 Match-Case vs. If-Elif

**When to use match-case:**
- Checking a single variable against multiple values
- More readable for 3+ cases
- Working with discrete values (numbers, strings)

**When to use if-elif:**
- Complex conditions with multiple variables
- Range comparisons (>, <, etc.)
- Python version < 3.10
- Combining logical operators

---

## Section 8: Common Pitfalls and Debugging (10 minutes)

### Overview
Identifying and fixing common errors in conditional statements.

### 8.1 Indentation Errors

```python
# WRONG
if age >= 18:
print("Adult")  # IndentationError

# CORRECT
if age >= 18:
    print("Adult")
```

### 8.2 Using Assignment Instead of Comparison

```python
# WRONG
if age = 18:  # SyntaxError: invalid syntax
    print("Exactly 18")

# CORRECT
if age == 18:
    print("Exactly 18")
```

### 8.3 Missing Colons

```python
# WRONG
if age >= 18  # SyntaxError: expected ':'
    print("Adult")

# CORRECT
if age >= 18:
    print("Adult")
```

### 8.4 Incorrect Condition Order

```python
# PROBLEMATIC - later conditions never reached
score = 95

if score >= 60:
    grade = "D"  # This executes for 95!
elif score >= 90:
    grade = "A"  # Never reached

# CORRECT - most specific first
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 60:
    grade = "D"
```

### 8.5 Floating Point Comparisons

```python
# PROBLEMATIC
if 0.1 + 0.2 == 0.3:  # False due to floating point precision
    print("Equal")

# BETTER
if abs((0.1 + 0.2) - 0.3) < 0.0001:
    print("Approximately equal")
```

---

## Section 9: Best Practices (5 minutes)

### Guidelines for Writing Clean Conditional Code

1. **Keep conditions simple and readable**
   - Break complex conditions into variables
   ```python
   # Less readable
   if user.age >= 18 and user.verified and not user.suspended and user.country == "US":
       allow_access()
   
   # More readable
   is_adult = user.age >= 18
   is_verified = user.verified
   is_active = not user.suspended
   is_domestic = user.country == "US"
   
   if is_adult and is_verified and is_active and is_domestic:
       allow_access()
   ```

2. **Avoid deep nesting (max 2-3 levels)**
   - Use early returns or combine conditions

3. **Use descriptive variable names**
   ```python
   # Poor
   if x > 0:
       print("yes")
   
   # Better
   if balance > 0:
       print("Account has positive balance")
   ```

4. **Consider the order of conditions**
   - Most common cases first (for performance)
   - Most specific cases first (for correctness)

5. **DRY Principle (Don't Repeat Yourself)**
   - Avoid duplicate code in branches

---

## Section 10: Practical Application and Summary (7 minutes)

### Real-World Scenario: Simple Calculator

```python
num1 = float(input("Enter first number: "))
operation = input("Enter operation (+, -, *, /): ")
num2 = float(input("Enter second number: "))

match operation:
    case "+":
        result = num1 + num2
        print(f"{num1} + {num2} = {result}")
    case "-":
        result = num1 - num2
        print(f"{num1} - {num2} = {result}")
    case "*":
        result = num1 * num2
        print(f"{num1} * {num2} = {result}")
    case "/":
        if num2 != 0:
            result = num1 / num2
            print(f"{num1} / {num2} = {result}")
        else:
            print("Error: Cannot divide by zero")
    case _:
        print("Invalid operation")
```

### Key Takeaways

- **If statements** allow conditional execution
- **Elif** provides multiple alternative conditions
- **Else** catches all remaining cases
- **Logical operators** combine conditions
- **Match-case** (Python 3.10+) offers pattern matching
- **Indentation** is crucial in Python
- **Condition order** matters in if-elif chains

---

## Resources for Further Learning

### Official Documentation
- [Python Control Flow](https://docs.python.org/3/tutorial/controlflow.html)
- [PEP 636 - Structural Pattern Matching](https://peps.python.org/pep-0636/)
- [Python Truth Value Testing](https://docs.python.org/3/library/stdtypes.html#truth-value-testing)

### Interactive Practice
- [Python.org Tutorial - Control Flow](https://docs.python.org/3/tutorial/controlflow.html)
- [W3Schools Python If...Else](https://www.w3schools.com/python/python_conditions.asp)
- [Real Python - Conditional Statements](https://realpython.com/python-conditional-statements/)
- [Exercism Python Track](https://exercism.org/tracks/python) - Conditionals exercises

### Video Tutorials
- [Corey Schafer - Python Conditionals](https://www.youtube.com/user/schafer5)
- [Programming with Mosh - Python Conditions](https://www.youtube.com/c/programmingwithmosh)

### Coding Challenges
- [HackerRank - Python If-Else](https://www.hackerrank.com/domains/python)
- [LeetCode - Easy Problems](https://leetcode.com/problemset/all/) (filter by Easy)
- [Codewars Python Kata](https://www.codewars.com/) (8 kyu and 7 kyu)

### Books
- **"Python Crash Course" by Eric Matthes** - Chapter 5: If Statements
- **"Automate the Boring Stuff with Python"** - Chapter 2: Flow Control
- **"Think Python" by Allen Downey** - Chapter 5: Conditionals and Recursion

---

## Time Allocation Summary

| Section | Duration | Cumulative |
|---------|----------|------------|
| 1. Introduction to Control Flow | 5 min | 5 min |
| 2. Basic If Statements | 15 min | 20 min |
| 3. If-Else Statements | 10 min | 30 min |
| 4. Elif Statements | 12 min | 42 min |
| 5. Logical Operators | 8 min | 50 min |
| 6. Nested If Statements | 8 min | 58 min |
| 7. Match-Case Statements | 15 min | 73 min |
| 8. Common Pitfalls and Debugging | 10 min | 83 min |
| 9. Best Practices | 5 min | 88 min |
| 10. Practical Application and Summary | 7 min | **95 min** |

*Note: Total includes 5 minutes buffer for questions and transitions*

---

## Preparation for Next Lecture

Students should:
1. Practice writing if-elif-else chains with at least 5 conditions
2. Experiment with match-case statements (if using Python 3.10+)
3. Review comparison and logical operators
4. Be prepared to discuss loops and iteration (next topic)