# Lecture 3: While Loops and Logical Operators in Python

**Duration:** 55 minutes

---

## Table of Contents

| Section | Topic | Time Allocation |
|---------|-------|-----------------|
| 1 | Introduction and Overview | 5 minutes |
| 2 | While Loops in Python | 15 minutes |
| 3 | Do-While Loop Patterns in Python | 10 minutes |
| 4 | Logical Operators (NOT, AND, OR) | 15 minutes |
| 5 | Combining Logical Operators | 8 minutes |
| 6 | Summary and Wrap-up | 2 minutes |

**Total Duration:** 55 minutes

---

## Learning Objectives (SMART)

| Objective | Description |
|-----------|-------------|
| **O1** | By the end of this lecture, students will be able to construct at least 3 different while loops that execute based on various conditions with 90% accuracy |
| **O2** | Students will be able to implement Python code patterns that simulate do-while loop behavior in at least 2 different scenarios |
| **O3** | Students will correctly apply the logical operators `not`, `and`, and `or` to create compound conditional expressions in at least 5 different contexts |
| **O4** | Students will be able to combine multiple logical operators with proper precedence to control program flow in complex decision-making scenarios with 85% accuracy |
| **O5** | Students will demonstrate the ability to debug and trace through loop execution with logical conditions by identifying errors in at least 3 provided code examples |

---

## Learning Outcomes

Upon successful completion of this lecture, students will be able to:

| Code | Learning Outcome |
|------|------------------|
| **LO1** | Understand and explain the purpose and structure of while loops in Python |
| **LO2** | Write while loops with proper initialization, condition, and update patterns |
| **LO3** | Implement Python code patterns that achieve do-while functionality |
| **LO4** | Apply the `not`, `and`, and `or` logical operators to create boolean expressions |
| **LO5** | Combine multiple logical operators with correct precedence and evaluation order |
| **LO6** | Analyze and predict the behavior of loops containing complex logical conditions |
| **LO7** | Debug common errors in loop construction and logical operator usage |

---

## Section 1: Introduction and Overview (5 minutes)

### What We'll Cover Today

Today's lecture focuses on two fundamental programming concepts that give you greater control over program flow:

1. **Iteration with While Loops** - Repeating code based on conditions
2. **Logical Operators** - Combining multiple conditions to make complex decisions

### Why These Concepts Matter

- **Real-world applications**: Most programs need to repeat actions (processing lists, user input validation, game loops)
- **Conditional logic**: Programs often need to check multiple conditions simultaneously (authentication systems, search filters, data validation)
- **Foundation for complex programs**: These building blocks enable you to create sophisticated, dynamic applications

### Brief Recap

Before we dive in, let's quickly recall:
- **If statements**: Execute code once if a condition is true
- **For loops**: Iterate a specific number of times or over a collection
- **Today**: While loops repeat until a condition becomes false, and logical operators let us combine conditions

---

## Section 2: While Loops in Python (15 minutes)

### 2.1 Understanding While Loops

**What is a While Loop?**

A while loop repeatedly executes a block of code as long as a specified condition remains `True`. Unlike for loops, while loops are used when:
- You don't know in advance how many iterations are needed
- The loop should continue until a specific condition changes
- You're waiting for user input or external events

**Syntax:**

```python
while condition:
    # code block to execute
    # must include something that eventually makes condition False
```

**Key Components:**

1. **Condition**: A boolean expression evaluated before each iteration
2. **Loop body**: The code that executes when the condition is True
3. **Update mechanism**: Something that eventually changes the condition to False (to avoid infinite loops)

### 2.2 Basic While Loop Examples

**Example 1: Countdown Timer**

```python
count = 5

while count > 0:
    print(f"Countdown: {count}")
    count -= 1  # Update: decrements count

print("Blast off!")
```

**Output:**
```
Countdown: 5
Countdown: 4
Countdown: 3
Countdown: 2
Countdown: 1
Blast off!
```

**Trace through the execution:**
- Iteration 1: count=5, condition is True (5 > 0), print, count becomes 4
- Iteration 2: count=4, condition is True (4 > 0), print, count becomes 3
- ...continues until count=0, condition is False (0 > 0 is False), loop exits

**Example 2: Accumulating a Sum**

```python
total = 0
number = 1

while number <= 5:
    total += number
    print(f"Adding {number}, total is now {total}")
    number += 1

print(f"Final total: {total}")
```

**Output:**
```
Adding 1, total is now 1
Adding 2, total is now 3
Adding 3, total is now 6
Adding 4, total is now 10
Adding 5, total is now 15
Final total: 15
```

### 2.3 While Loops with User Input

**Example 3: Password Validation**

```python
password = ""

while password != "python123":
    password = input("Enter the password: ")
    if password != "python123":
        print("Incorrect password. Try again.")

print("Access granted!")
```

This loop continues until the user enters the correct password.

**Example 4: Number Guessing Game**

```python
secret_number = 42
guess = 0

while guess != secret_number:
    guess = int(input("Guess the secret number: "))
    
    if guess < secret_number:
        print("Too low!")
    elif guess > secret_number:
        print("Too high!")
    else:
        print("Correct! You guessed it!")
```

### 2.4 Infinite Loops and Break Statement

**Infinite Loop (Warning!):**

```python
# DON'T DO THIS - will run forever!
while True:
    print("This will never stop!")
```

**Using Break to Exit:**

```python
while True:
    user_input = input("Type 'quit' to exit: ")
    
    if user_input.lower() == 'quit':
        break  # Exits the loop immediately
    
    print(f"You typed: {user_input}")

print("Program ended")
```

The `break` statement immediately exits the loop, regardless of the condition.

### 2.5 Continue Statement

The `continue` statement skips the rest of the current iteration and moves to the next one:

```python
count = 0

while count < 10:
    count += 1
    
    if count % 2 == 0:
        continue  # Skip even numbers
    
    print(count)  # Only prints odd numbers

# Output: 1, 3, 5, 7, 9
```

### 2.6 Common While Loop Patterns

**Pattern 1: Sentinel-Controlled Loop**

```python
total = 0
value = int(input("Enter a number (0 to stop): "))

while value != 0:  # 0 is the sentinel value
    total += value
    value = int(input("Enter a number (0 to stop): "))

print(f"Sum: {total}")
```

**Pattern 2: Flag-Controlled Loop**

```python
found = False
count = 1

while not found and count <= 10:
    number = int(input(f"Attempt {count}: Enter the magic number: "))
    
    if number == 7:
        found = True
        print("You found it!")
    else:
        print("Try again!")
    
    count += 1

if not found:
    print("Out of attempts!")
```

---

## Section 3: Do-While Loop Patterns in Python (10 minutes)

### 3.1 Understanding Do-While Loops

**Concept:**

Unlike languages like Java or C++, Python doesn't have a built-in `do-while` loop. However, we often need the behavior where:
- The loop body executes **at least once**
- Then continues based on a condition

**Do-While in Other Languages (for reference):**

```java
// Java syntax
do {
    // code executes at least once
} while (condition);
```

### 3.2 Simulating Do-While in Python

**Method 1: While True with Break**

The most common and Pythonic approach:

```python
while True:
    # Code that executes at least once
    user_input = input("Do you want to continue? (yes/no): ")
    
    if user_input.lower() != 'yes':
        break  # Exit when condition is met
```

**Example: Menu System**

```python
while True:
    print("\n=== Main Menu ===")
    print("1. Option A")
    print("2. Option B")
    print("3. Exit")
    
    choice = input("Enter your choice: ")
    
    if choice == '1':
        print("You selected Option A")
    elif choice == '2':
        print("You selected Option B")
    elif choice == '3':
        print("Goodbye!")
        break
    else:
        print("Invalid choice")
```

**Method 2: Initialize to Trigger First Iteration**

```python
# Ensure the condition is True for the first iteration
choice = 'yes'

while choice.lower() == 'yes':
    number = int(input("Enter a positive number: "))
    print(f"You entered: {number}")
    
    choice = input("Continue? (yes/no): ")
```

**Method 3: Using a Flag Variable**

```python
first_time = True

while first_time or some_condition:
    first_time = False
    # Code executes at least once
    # Then continues if some_condition is True
```

### 3.3 Practical Examples

**Example 1: Input Validation**

Ensures valid input before proceeding:

```python
while True:
    age = int(input("Enter your age (1-120): "))
    
    if 1 <= age <= 120:
        break  # Valid input, exit loop
    else:
        print("Invalid age. Please try again.")

print(f"Your age is {age}")
```

**Example 2: Bank ATM Simulation**

```python
balance = 1000.00

while True:
    print(f"\nCurrent balance: ${balance:.2f}")
    print("1. Withdraw")
    print("2. Deposit")
    print("3. Check Balance")
    print("4. Exit")
    
    choice = input("Select option: ")
    
    if choice == '1':
        amount = float(input("Withdrawal amount: $"))
        if amount <= balance:
            balance -= amount
            print(f"Withdrew ${amount:.2f}")
        else:
            print("Insufficient funds!")
    
    elif choice == '2':
        amount = float(input("Deposit amount: $"))
        balance += amount
        print(f"Deposited ${amount:.2f}")
    
    elif choice == '3':
        print(f"Balance: ${balance:.2f}")
    
    elif choice == '4':
        print("Thank you for banking with us!")
        break
    
    else:
        print("Invalid option")
```

---

## Section 4: Logical Operators (NOT, AND, OR) (15 minutes)

### 4.1 Introduction to Logical Operators

**Purpose:**

Logical operators allow you to combine multiple boolean expressions to create more complex conditions.

**The Three Logical Operators:**

| Operator | Symbol | Description |
|----------|--------|-------------|
| NOT | `not` | Reverses the boolean value |
| AND | `and` | True if both conditions are True |
| OR | `or` | True if at least one condition is True |

### 4.2 The NOT Operator

**Syntax:** `not expression`

**How it works:**
- If expression is `True`, `not expression` is `False`
- If expression is `False`, `not expression` is `True`

**Truth Table:**

| Expression | not Expression |
|------------|----------------|
| True | False |
| False | True |

**Examples:**

```python
is_raining = False
print(not is_raining)  # True

age = 25
print(not (age < 18))  # True (because age < 18 is False)

has_license = True
if not has_license:
    print("Cannot drive")  # Won't execute
else:
    print("Can drive")  # Executes
```

**Practical Example:**

```python
username = input("Enter username: ")

if not username:  # Checks if username is empty
    print("Username cannot be empty!")
else:
    print(f"Welcome, {username}!")
```

### 4.3 The AND Operator

**Syntax:** `expression1 and expression2`

**How it works:**
- Returns `True` only if **both** expressions are `True`
- Returns `False` if **any** expression is `False`

**Truth Table:**

| Expression 1 | Expression 2 | Result |
|--------------|--------------|--------|
| True | True | True |
| True | False | False |
| False | True | False |
| False | False | False |

**Examples:**

```python
age = 25
has_license = True

# Both conditions must be True
if age >= 18 and has_license:
    print("You can drive")

temperature = 22
is_sunny = True

if temperature > 20 and is_sunny:
    print("Perfect day for a picnic!")
```

**Range Checking:**

```python
score = 85

# Check if score is in range [80, 90]
if score >= 80 and score <= 90:
    print("Grade: B")

# More Pythonic way:
if 80 <= score <= 90:
    print("Grade: B")
```

**Multiple AND Conditions:**

```python
has_id = True
has_ticket = True
age = 25

if age >= 18 and has_id and has_ticket:
    print("You may enter the concert")
```

### 4.4 The OR Operator

**Syntax:** `expression1 or expression2`

**How it works:**
- Returns `True` if **at least one** expression is `True`
- Returns `False` only if **both** expressions are `False`

**Truth Table:**

| Expression 1 | Expression 2 | Result |
|--------------|--------------|--------|
| True | True | True |
| True | False | True |
| False | True | True |
| False | False | False |

**Examples:**

```python
is_weekend = True
is_holiday = False

# At least one must be True
if is_weekend or is_holiday:
    print("No work today!")

day = "Saturday"

if day == "Saturday" or day == "Sunday":
    print("It's the weekend!")
```

**Multiple OR Conditions:**

```python
grade = input("Enter your letter grade: ")

if grade == 'A' or grade == 'B' or grade == 'C':
    print("You passed!")
else:
    print("You need to retake the course")
```

**Membership Test Alternative:**

```python
# More Pythonic way using 'in'
if grade in ['A', 'B', 'C']:
    print("You passed!")
```

### 4.5 Short-Circuit Evaluation

**Important Concept:**

Python uses short-circuit evaluation:
- **AND**: If first expression is `False`, second is not evaluated
- **OR**: If first expression is `True`, second is not evaluated

**Example:**

```python
age = 15

# Second condition won't be evaluated if age < 18
if age >= 18 and has_valid_license():  # has_valid_license() won't run
    print("Can drive")

# Second condition won't be evaluated if age > 65
if age > 65 or has_disability():  # has_disability() won't run if age > 65
    print("Eligible for discount")
```

**Practical Use - Avoiding Errors:**

```python
numbers = [1, 2, 3, 4, 5]
index = 3

# Safe: checks length before accessing index
if index < len(numbers) and numbers[index] > 0:
    print("Valid positive number")
```

---

## Section 5: Combining Logical Operators (8 minutes)

### 5.1 Operator Precedence

When combining logical operators, Python follows this order:

1. **Parentheses** `()`
2. **NOT** `not`
3. **AND** `and`
4. **OR** `or`

**Example:**

```python
# Without parentheses
result = True or False and False
print(result)  # True (AND evaluated first)

# With parentheses to change order
result = (True or False) and False
print(result)  # False
```

### 5.2 Complex Conditional Examples

**Example 1: Age and Income Eligibility**

```python
age = 25
income = 35000
has_cosigner = False

# Complex eligibility check for loan
if (age >= 21 and income >= 30000) or has_cosigner:
    print("Loan approved")
else:
    print("Loan denied")
```

**Example 2: Login System**

```python
username = "admin"
password = "12345"
is_locked = False
attempts = 2

if not is_locked and username == "admin" and password == "12345":
    print("Login successful")
elif attempts >= 3 or is_locked:
    print("Account locked")
else:
    print("Invalid credentials")
```

**Example 3: Temperature and Weather**

```python
temperature = 28
is_raining = False
is_windy = False

# Good outdoor conditions
if temperature >= 20 and temperature <= 30 and not is_raining and not is_windy:
    print("Perfect weather for outdoor activities!")
elif is_raining or is_windy:
    print("Better stay indoors")
elif temperature < 20:
    print("Too cold!")
else:
    print("Too hot!")
```

### 5.3 Combining with While Loops

**Example 1: Controlled Loop with Multiple Conditions**

```python
count = 0
user_wants_continue = True
max_attempts = 5

while user_wants_continue and count < max_attempts:
    print(f"Attempt {count + 1}")
    
    result = input("Continue? (yes/no): ")
    user_wants_continue = (result.lower() == 'yes')
    count += 1

if count >= max_attempts:
    print("Maximum attempts reached")
else:
    print("User chose to stop")
```

**Example 2: Game Loop**

```python
health = 100
has_won = False
has_lost = False

while health > 0 and not has_won and not has_lost:
    print(f"Health: {health}")
    
    action = input("Action (attack/defend/quit): ")
    
    if action == "attack":
        # Game logic
        health -= 10
    elif action == "defend":
        health += 5
    elif action == "quit":
        has_lost = True
    
    # Check win condition
    if health > 150:
        has_won = True

if has_won:
    print("Victory!")
elif health <= 0:
    print("Game Over!")
else:
    print("You quit the game")
```

### 5.4 De Morgan's Laws

Understanding logical equivalences:

```python
# These are equivalent:
not (A and B) == (not A) or (not B)
not (A or B) == (not A) and (not B)

# Example:
age = 15
has_license = False

# Original
if not (age >= 18 and has_license):
    print("Cannot drive")

# Equivalent using De Morgan's Law
if age < 18 or not has_license:
    print("Cannot drive")
```

### 5.5 Best Practices

1. **Use parentheses for clarity:**
   ```python
   if (age >= 18 and has_license) or (has_permit and with_adult):
       print("Can drive")
   ```

2. **Break complex conditions into variables:**
   ```python
   is_adult = age >= 18
   has_valid_credentials = has_license or (has_permit and with_adult)
   
   if is_adult and has_valid_credentials:
       print("Can drive")
   ```

3. **Use De Morgan's Laws to simplify:**
   ```python
   # Instead of: not (x > 10 and y < 5)
   # Use: x <= 10 or y >= 5
   ```

---

## Section 6: Summary and Wrap-up (2 minutes)

### Key Takeaways

**While Loops:**
- Execute code repeatedly while a condition is True
- Must include mechanism to eventually make condition False
- Use `break` to exit early, `continue` to skip iterations
- Common patterns: sentinel-controlled, flag-controlled

**Do-While Patterns in Python:**
- Python uses `while True` with `break` for do-while behavior
- Ensures code executes at least once
- Essential for menu systems and input validation

**Logical Operators:**
- **NOT** (`not`): Reverses boolean value
- **AND** (`and`): True only if both conditions are True
- **OR** (`or`): True if at least one condition is True
- Short-circuit evaluation optimizes performance

**Combining Operators:**
- Precedence: Parentheses > NOT > AND > OR
- Use parentheses for clarity
- Break complex conditions into named variables
- Apply De Morgan's Laws to simplify logic

### Next Steps

Practice these concepts by:
1. Writing loops that process user input until a sentinel value
2. Creating programs with complex conditional logic
3. Combining loops and logical operators in realistic scenarios

---

## Time Allocation and Learning Outcomes Summary

| Time | Section | Topics Covered | Learning Outcomes |
|------|---------|----------------|-------------------|
| 5 min | Introduction | Overview, motivation, recap | LO1 |
| 15 min | While Loops | Syntax, examples, break/continue, patterns | LO1, LO2, LO7 |
| 10 min | Do-While Patterns | Simulating do-while, practical examples | LO3 |
| 15 min | Logical Operators | NOT, AND, OR, truth tables, short-circuit | LO4, LO6 |
| 8 min | Combining Operators | Precedence, complex conditions, best practices | LO5, LO6, LO7 |
| 2 min | Summary | Review, key takeaways | All LOs |

**Total: 55 minutes**

---

## Resources for Further Reading and Practice

### Official Documentation
- [Python While Statements](https://docs.python.org/3/reference/compound_stmts.html#while) - Official Python documentation
- [Python Boolean Operations](https://docs.python.org/3/library/stdtypes.html#boolean-operations-and-or-not) - Logical operators reference

### Online Tutorials
- [Real Python: Python While Loops](https://realpython.com/python-while-loop/)
- [W3Schools: Python While Loops](https://www.w3schools.com/python/python_while_loops.asp)
- [GeeksforGeeks: Python Logical Operators](https://www.geeksforgeeks.org/python-logical-operators/)

### Interactive Practice
- [HackerRank: Python Practice](https://www.hackerrank.com/domains/python) - While loop challenges
- [LeetCode: Easy Problems](https://leetcode.com/problemset/all/?difficulty=Easy) - Algorithm practice
- [Codewars: Python Kata](https://www.codewars.com/kata/search/python) - Loop and logic challenges

### Video Resources
- [Corey Schafer: Python Loops](https://www.youtube.com/watch?v=6iF8Xb7Z3wQ)
- [Programming with Mosh: Python Tutorial](https://www.youtube.com/watch?v=_uQrJ0TkZlc)

### Books (Relevant Chapters)
- **Python Crash Course** by Eric Matthes - Chapter 7 (While Loops and User Input)
- **Automate the Boring Stuff with Python** by Al Sweigart - Chapter 2 (Flow Control)
- **Learning Python** by Mark Lutz - Chapter 13 (Iteration and Comprehensions)

### Practice Exercises
Create programs that use while loops and logical operators:
1. **Password Validator**: Check multiple conditions (length, uppercase, lowercase, digits)
2. **Number Guessing Game**: With limited attempts and hint system
3. **Shopping Cart**: Menu system with subtotal calculation and checkout
4. **Prime Number Checker**: Using loops and divisibility logic
5. **ATM Simulator**: Complete banking system with authentication

### Additional Topics to Explore
- List comprehensions with conditional logic
- The `else` clause in while loops
- Nested while loops and their applications
- Performance optimization with short-circuit evaluation
- Debugging techniques for infinite loops

---

**End of Lecture**