# Lecture 3: Python Worksheet

---

## Part 1: Quiz Questions

### Question 1

Fill in the blanks using the words from the word bank below:

A while loop repeatedly executes a block of code as long as a specified condition remains ________. Unlike for loops, while loops require an ________ mechanism to prevent infinite loops. The ________ statement can be used to exit a loop immediately, while the ________ statement skips the rest of the current iteration and moves to the next one.

**Word Bank:** `continue`, `True`, `break`, `update`, `False`, `condition`, `iterate`

---

### Question 2

Fill in the blanks using the words from the word bank below:

Python uses ________ evaluation for logical operators. For the AND operator, if the first expression is ________, the second expression is not evaluated. For the OR operator, if the first expression is ________, the second expression is not evaluated. The order of precedence for logical operators is: parentheses, then ________, then ________, and finally ________.

**Word Bank:** `short-circuit`, `NOT`, `AND`, `OR`, `True`, `False`, `long-circuit`, `MAYBE`

---

### Question 3

What is the output of the following code?

```python
count = 0
while count < 5:
    count += 2
    if count == 4:
        continue
    print(count)
```

a) 2, 4  
b) 2, 6  
c) 0, 2, 4  
d) 2, 4, 6  

---

### Question 4

Which of the following correctly simulates a do-while loop in Python that executes at least once?

a) 
```python
while condition:
    # code block
```

b)
```python
while True:
    # code block
    if condition:
        break
```

c)
```python
for i in range(1):
    # code block
    while condition:
        # more code
```

d)
```python
do:
    # code block
while condition
```

---

## Part 2: Code Tasks

### Task 1: Login Validation System

Write a program that simulates a login system with the following requirements:

- Allow the user a maximum of 3 attempts to enter the correct username and password
- The correct username is "student" and the correct password is "python2025"
- After each failed attempt, display how many attempts remain
- If the user enters correct credentials, display "Login successful!" and exit
- If all 3 attempts are used without success, display "Account locked. Please contact administrator."
- Use a while loop with logical operators to control the flow

**Hint:** You'll need to combine a counter for attempts with logical AND/OR operators to check both username and password.

---

### Task 2: Number Classification Game

Write a program that repeatedly asks the user to enter numbers until they choose to quit. For each number entered, classify it according to the following rules:

- If the number is positive AND even, print "Positive Even"
- If the number is positive AND odd, print "Positive Odd"
- If the number is negative AND even, print "Negative Even"
- If the number is negative AND odd, print "Negative Odd"
- If the number is zero, print "Zero"
- After each classification, ask if the user wants to continue (yes/no)
- The program should continue until the user enters "no"

**Requirements:**
- Use a do-while pattern (while True with break)
- Use appropriate logical operators (AND, OR, NOT) in your conditions
- Handle the case where the user inputs 0 separately

---

## Part 3: Summary Table

### Mapping Lecture Topics to Tutorial Tasks

| Lecture Topic | Relevant Tutorial Section | Task Reference |
|--------------|---------------------------|----------------|
| While Loops - Basic Syntax and Examples | Section 12: While Loops | Task 12.1 |
| Do-While Loop Patterns | Section 13: Do-While Loops (Python Equivalent) | Task 13.1 |
| Logical Operators (NOT, AND, OR) | Section 14: Logical Operators | Task 14.1 |
| Using Break Statement with While Loops | Section 12: While Loops | Task 12.1 |
| Combining Logical Operators with Loops | Section 14: Logical Operators | Task 14.1 |

---

**End of Worksheet**
