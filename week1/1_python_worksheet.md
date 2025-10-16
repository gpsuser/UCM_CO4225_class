# Lecture 1: Python Worksheet

---

## Quiz Section

### Question 1: Fill in the Blanks

Complete the following sentences by selecting the correct words from the word bank below.

Python uses the **________** function to display output to the console. Variables in Python are created without declaring their **________** explicitly, which is called **________** typing. When you want to get data from the user, you use the **________** function, which always returns data as a **________**.

**Word Bank:** `string`, `print()`, `dynamic`, `input()`, `type`

---

### Question 2: Fill in the Blanks

Complete the following sentences by selecting the correct words from the word bank below.

In Python, you can combine strings using the **________** operator or by using **________**, which is the modern and recommended approach. When you need to include special characters like newlines in a string, you use **________** characters that start with a backslash. Python follows the **________** rule for operator precedence, where operations inside **________** are performed first.

**Word Bank:** `f-strings`, `PEMDAS`, `parentheses`, `escape`, `+`

---

### Question 3: Multiple Choice

Which of the following statements about Python data types is **correct**?

A) The `int()` function rounds decimal numbers to the nearest integer  
B) The `input()` function automatically converts user input to the appropriate data type  
C) Python's division operator `/` always returns a float, even when dividing two integers  
D) String variables must be declared with the `str` keyword before use

---

### Question 4: Multiple Choice

Consider the following Python code:

```python
x = 10
x += 5
x *= 2
x //= 3
```

What is the final value of `x`?

A) 10  
B) 15  
C) 20  
D) 30

---

## Task Section

### Task 1: Temperature Converter with Formatting

Write a Python program that:

1. Asks the user to enter a temperature in Fahrenheit
2. Converts it to both Celsius and Kelvin using the formulas:
   - Celsius = (Fahrenheit - 32) × 5/9
   - Kelvin = Celsius + 273.15
3. Displays the results formatted to 2 decimal places with appropriate labels

**Example Output:**
```
Enter temperature in Fahrenheit: 98.6
98.60°F = 37.00°C = 310.15K
```

**Hints:**
- Use f-strings for formatting
- Use `:.2f` to format to 2 decimal places
- Remember to convert the input to a float

---

### Task 2: Personal Information Card

Write a Python program that:

1. Asks the user for their first name, last name, age, and favorite hobby
2. Calculates their birth year (assume current year is 2025)
3. Creates a formatted "information card" that displays:
   - Full name (first and last name combined)
   - Age and birth year
   - Favorite hobby
   - A personalized message using their information

**Example Output:**
```
Enter your first name: Alice
Enter your last name: Smith
Enter your age: 20
Enter your favorite hobby: painting

=================================
      INFORMATION CARD
=================================
Name:          Alice Smith
Age:           20 years old
Born in:       2005
Hobby:         painting
=================================
Alice, may your passion for painting bring you joy!
```

**Hints:**
- Use string concatenation or f-strings
- Calculate birth year: 2025 - age
- Use escape characters (`\t`, `\n`) or repetition (`*` operator) for formatting

---

## Summary Table

### Lecture Topics and Tutorial Tasks

| Lecture Topic | Tutorial Section(s) |
|--------------|---------------------|
| IDEs and Project Setup | Task 1.1: Creating a new Python file |
| String Variables | Task 2.1: Creating and printing variables |
| String Concatenation | Task 3.1: Concatenating address components |
| Appending Strings | Task 4.1: Building a sentence incrementally |
| User Input | Task 5.1: Getting favorite food and color |
| Data Types | Task 6.1: Age calculation from birth year |
| Basic Calculations | Task 7.1: Rectangle perimeter and area |
| Assignment Operators | Task 8.1: Sequential operations on a number |
| Comments and Documentation | Referenced throughout tutorial (Section 4) |
| Escape Characters | Referenced in Section 5 examples |
| String Formatting | Referenced in Section 3.3 and throughout |

---

**End of Worksheet**