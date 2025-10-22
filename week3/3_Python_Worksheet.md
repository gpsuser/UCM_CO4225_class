# Lecture 3: Python Worksheet

---

## Part 1: Quiz

### Question 1

Complete the following paragraph by filling in the blanks with the appropriate words from the word bank below.

A while loop repeatedly executes a block of code as long as a specified __________ remains True. Unlike for loops, while loops are ideal when you don't know in advance how many __________ are needed. The loop must include an __________ mechanism to eventually make the condition False, otherwise you risk creating an __________ loop. You can use the __________ statement to exit a loop immediately, or the __________ statement to skip the rest of the current iteration.

**Word Bank:** `infinite`, `continue`, `iterations`, `break`, `condition`, `update`

---

### Question 2

Complete the following paragraph by filling in the blanks with the appropriate words from the word bank below.

Python uses __________ evaluation when processing logical operators. For the AND operator, if the first expression is __________, the second expression is not evaluated. For the OR operator, if the first expression is __________, the second expression is not evaluated. The order of precedence for logical operators is: parentheses, then __________, then __________, and finally __________.

**Word Bank:** `OR`, `NOT`, `AND`, `True`, `False`, `short-circuit`

---

### Question 3

What is the output of the following code?

```python
count = 3
while count > 0:
    print(count)
    count -= 1
    if count == 1:
        break
print("Done")
```

a) 3  
   2  
   Done

b) 3  
   2  
   1  
   Done

c) 3  
   Done

d) 2  
   1  
   Done

---

### Question 4

Which of the following expressions evaluates to `True`?

a) `not True and False`

b) `True and False or True`

c) `not (True or False)`

d) `False and True or False`

---

## Part 2: Tasks

### Task 1: Login System with Attempt Limit

Create a login system that gives users a maximum of 3 attempts to enter the correct username and password. The program should:
- Keep track of the number of attempts
- Allow the user to try again if credentials are wrong
- Lock the account after 3 failed attempts
- Grant access if credentials are correct

**Correct credentials:**
- Username: `student`
- Password: `python2024`

**Code Scaffolding:**

```python
# Login system with attempt limit
max_attempts = 3
attempts = 0
correct_username = "student"
correct_password = "python2024"

while attempts < max_attempts:
    # Your code here
    pass

# Check final result here
```

**Sample Output 1 (Failed login):**
```
Attempt 1/3
Enter username: admin
Enter password: 12345
Invalid credentials. Try again.

Attempt 2/3
Enter username: student
Enter password: wrong
Invalid credentials. Try again.

Attempt 3/3
Enter username: test
Enter password: test
Invalid credentials. Try again.

Account locked due to too many failed attempts.
```

**Sample Output 2 (Successful login):**
```
Attempt 1/3
Enter username: student
Enter password: python2024
Login successful! Welcome, student.
```

---

### Task 2: Number Range Validator

Write a program that repeatedly asks the user to enter a number between 1 and 100 (inclusive). The program should:
- Check if the number is in the valid range AND is even
- If valid and even, congratulate the user and display the number
- If valid but odd, tell the user it must be even
- If outside the range, tell the user it's out of range
- Keep asking until a valid even number is entered
- Use logical operators to check multiple conditions

**Code Scaffolding:**

```python
# Number range validator
valid_input = False

while not valid_input:
    number = int(input("Enter a number between 1 and 100: "))
    
    # Your validation logic here using logical operators
    
print(f"Thank you! You entered: {number}")
```

**Sample Output:**
```
Enter a number between 1 and 100: 150
Error: Number must be between 1 and 100.

Enter a number between 1 and 100: 45
Error: Number must be even.

Enter a number between 1 and 100: -5
Error: Number must be between 1 and 100.

Enter a number between 1 and 100: 88
Success! You entered a valid even number: 88
Thank you! You entered: 88
```

---

## Part 3: Summary Table

### Lecture Topics and Related Tutorial Tasks

| Lecture Topic | Tutorial Section | Task Reference |
|---------------|------------------|----------------|
| While Loops - Basic syntax and structure | Section 12: While Loops | Task 12.1: Number guessing game |
| Do-While Loop Patterns - Menu systems | Section 13: Do-While Loops | Task 13.1: Menu-driven program |
| Logical Operators - AND and OR usage | Section 14: Logical Operators | Task 14.1: Discount eligibility checker |

---

**End of Worksheet**
