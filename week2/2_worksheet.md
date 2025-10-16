# Lecture 2: Python Worksheet

---

## Section 1: Quiz Questions

### Question 1: Cloze Exercise (Fill in the Blanks)

Complete the following paragraph by filling in the blanks with the appropriate words from the word bank below.

---

* In Python, conditional statements allow programs to make __________ based on whether certain conditions are true or false. 
* The basic structure of an if statement requires a __________ after the condition and uses __________ to define the code block. 
* When we need to check multiple conditions sequentially, we use __________ statements, which are evaluated from top to bottom. 
* Python 3.10+ introduced the __________ statement as an alternative to multiple elif chains.

**Word Bank (scrambled):**

- match-case
- indentation
- decisions
- colon
- elif

---

### Question 2: Cloze Exercise (Fill in the Blanks)

Complete the following code snippet by filling in the blanks with the appropriate operators from the word bank below.

```python
age = 20
has_license = True
is_student = False

# Check if person can rent a car
if age __________ 21 __________ has_license:
    print("You can rent a car")

# Check if person qualifies for discount
if is_student __________ age < 25:
    print("You qualify for a discount")

# Check if not a student
if __________ is_student:
    print("Regular pricing applies")
```

**Word Bank (scrambled):**

- or
- not
- and
- >=

---

### Question 3: Multiple Choice

What will be the output of the following code?

```python
score = 85

if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
else:
    print("D")
```

**Options:**

- A) A
- B) B
- C) C
- D) D
- E) B and C

---

### Question 4: Multiple Choice

Which of the following statements about Python's match-case is TRUE?

**Options:**

- A) Match-case statements are available in all Python versions
- B) The underscore `_` in a match-case acts as a default case that catches all unmatched values
- C) Match-case statements can only match integer values
- D) Match-case statements require curly braces `{}` around each case
- E) You cannot match multiple values in a single case statement

---

## Section 2: Coding Tasks

### Task 1: Temperature Classifier

Write a Python program that asks the user for a temperature in Celsius and classifies it according to the following criteria:

- **Below 0°C:** Print "Freezing - Ice may form"
- **0°C to 10°C:** Print "Cold - Wear a jacket"
- **11°C to 20°C:** Print "Cool - Long sleeves recommended"
- **21°C to 30°C:** Print "Comfortable - Perfect weather"
- **Above 30°C:** Print "Hot - Stay hydrated"

Additionally, if the temperature is exactly 25°C, also print "Ideal room temperature!"

**Requirements:**

- Use if-elif-else statements
- Handle the special case for 25°C appropriately
- Use appropriate comparison operators

**Example Output:**
```
Enter temperature in Celsius: 25
Comfortable - Perfect weather
Ideal room temperature!
```

---

### Task 2: Movie Ticket Price Calculator

Write a Python program that calculates the price of a movie ticket based on the following criteria:

**Age-based pricing:**

- Children (under 12): $8
- Teenagers (12-17): $10
- Adults (18-64): $15
- Seniors (65 and over): $10

**Additional rules:**

- If it's a weekend (user inputs "Saturday" or "Sunday"), add $3 to the ticket price
- If the customer is a student (user inputs "yes" when asked), apply a 10% discount to the final price
- The student discount applies to all age groups

**Requirements:**

- Ask the user for their age, the day of the week, and whether they are a student
- Use if-elif-else statements for age-based pricing
- Use logical operators (and/or) where appropriate
- Calculate and display the final ticket price formatted to 2 decimal places

**Example Output:**
```
Enter your age: 16
Enter day of week: Saturday
Are you a student? (yes/no): yes
Your ticket price: $11.70
```

---

## Section 3: Summary Table

### Mapping of Lecture Topics to Tutorial Tasks

| Lecture Topic | Relevant Tutorial Section(s) |
|--------------|------------------------------|
| Basic If Statements | **Section 9: If Statements** - Task 9.1 |
| If-Else Statements | **Section 10: If-Else Statements** - Task 10.1 |
| Elif (Else-If) Statements | **Section 10: If-Else Statements** - Task 10.1 |
| Logical Operators | **Section 14: Logical Operators** - Task 14.1 |
| Match-Case Statements | **Section 11: Match Statements** - Task 11.1 |

---

## Additional Practice

For more practice on conditional statements, complete the following tutorial sections:

- Section 9: If Statements (Task 9.1)
- Section 10: If-Else Statements (Task 10.1)
- Section 11: Match Statements (Task 11.1)
- Section 14: Logical Operators (Task 14.1)

---

**Estimated Time:** 20-30 minutes