# Functions Notes

Functions are actions (or "verbs") in a program that perform a specific task. They help organize code into reusable blocks.

For example:

```python
print("hello, world")
```

Here, `print` is a function that outputs the given text to the screen.

---

# Arguments

An argument is an input passed to a function that influences its behavior.

For example:

```python
print("Hello, Avinash!")
```

Here, `"Hello, Avinash!"` is the argument given to the `print` function, which then displays this text.

---

# Side Effects and Bugs

## Side Effects

A **side effect** occurs when a function modifies something outside its scope or has an unintended impact on the program. Side effects can include:

- Modifying global variables
- Changing a file on disk
- Updating a database
- Printing output to the console

### Example:

```python
x = 10

print("Before modification:", x)
x = 20  # Modifies the variable
print("After modification:", x)
```

## Bugs

A **bug** is an error in a program that causes it to produce incorrect or unexpected results. Bugs can occur for various reasons, such as logical errors, syntax errors, or runtime errors.

### Example:

```python
print(10 / 0)  # ZeroDivisionError: division by zero
```

In this example, dividing by zero raises a `ZeroDivisionError`, which is a bug that needs to be handled.

---

# Input Function

The `input()` function is used to take user input in Python. It allows the user to enter a value, which can then be stored in a variable.

### Example:

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

### Explanation:

- `input("Enter your name: ")` displays a prompt and waits for the user to type something.
- The entered value is stored in the `name` variable.
- `print("Hello, " + name + "!")` then prints a greeting using the entered name.

By default, `input()` returns a **string**. If you need a number, you must convert it using `int()` or `float()`:

```python
age = int(input("Enter your age: "))
print("You are", age, "years old.")
```

---

# Variables

A **variable** is a named storage location in memory that holds a value. It allows you to store and manipulate data in a program.

## Declaring a Variable

In Python, you can create a variable by assigning a value to a name:

```python
x = 10  # Integer
name = "Avinash"  # String
pi = 3.14  # Float
```

## Variable Naming Rules

- Must start with a **letter (a-z, A-Z)** or an **underscore (_)**
- Cannot start with a **number**
- Can contain **letters, numbers, and underscores**
- Case-sensitive (`age` and `Age` are different)
- Cannot use **Python keywords** (e.g., `if`, `else`, `while`)

### Valid Examples:

```python
my_var = 10
_name = "Python"
user123 = "Avinash"
```

### Invalid Examples:

```python
3var = 5  # ❌ Cannot start with a number
my-var = 10  # ❌ Cannot use hyphens
if = "hello"  # ❌ Cannot use keywords
```

## Changing Variable Values

Variables can be updated by assigning a new value:

```python
x = 5
x = "Now I am a string!"
print(x)  # Output: Now I am a string!
```

## Assigning Multiple Variables

You can assign multiple variables at once:

```python
a, b, c = 1, 2, 3
print(a, b, c)  # Output: 1 2 3
```

Or assign the same value to multiple variables:

```python
x = y = z = 100
print(x, y, z)  # Output: 100 100 100
```

## Data Types of Variables

Python automatically determines the type of a variable:

```python
num = 10       # Integer
name = "John"  # String
pi = 3.14      # Float
is_valid = True  # Boolean
```

To check a variable's type, use `type()`:

```python
print(type(num))  # Output: <class 'int'>
print(type(name))  # Output: <class 'str'>
```

## Constants

A **constant** is a variable whose value should not change. Python does not have built-in constants, but by convention, we use **uppercase names**:

```python
PI = 3.14159  # Constant (by convention)
GRAVITY = 9.8
```

Even though they can be changed, it's a common practice to treat them as unchangeable.

---

# Assignment Operator (`=`)

The **`=`** operator in Python is used to assign a value to a variable.

## Example:
```python
x = 10  # Assigns 10 to x
name = "Avinash"  # Assigns "Avinash" to name
```

---

# Comments in Python

Comments are used to explain code and make it more readable. They are ignored by Python during execution.

## Single-Line Comment:
Use `#` for single-line comments.

```python
# This is a comment
x = 10  # Assigns 10 to x
```

---

# String Concatenation in Python

Concatenation means **joining strings together** using the `+` operator.

```python
first_name = "Avinash"
last_name = "Kumar"
full_name = first_name + " " + last_name
print(full_name)  # Output: Avinash Kumar
```

---

# `str` in Python

The `str` function is used to convert values into **strings**.

### Example:
```python
num = 100
text = str(num)
print(text)  # Output: '100'
print(type(text))  # Output: <class 'str'>
```

---

# The `print()` Function in Python  

The `print()` function displays output and allows customization using optional parameters:  

## Key Parameters  
- **`sep`** → Specifies the separator between multiple values (default: space).  
- **`end`** → Defines what is printed at the end (default: newline `\n`).  

## Examples  

```python
print("Hello", "Avinash", sep="-")  
# Output: Hello-Avinash  

print("Python", "is", "fun", end="!")  
# Output: Python is fun!  

print("Line 1", end=" ")  
print("Line 2")  
# Output: Line 1 Line 2  
```

# Print Formatting in Python

Python provides several ways to format strings for output. Here are the most common methods:

## 1. Using `+` Operator (Concatenation)

```python
name = "Avinash"
age = 25
print("Hello, " + name + "! You are " + str(age) + " years old.")
```

- `+` joins strings together.
- `str(age)` converts `age` (an integer) to a string.

## 2. Using `,` in `print()` (Automatic Space Insertion)

```python
name = "Avinash"
age = 25
print("Hello,", name, "! You are", age, "years old.")
```

- Automatically adds spaces between values.
- No need for `str()` conversion.

## 3. Using `.format()` Method

```python
name = "Avinash"
age = 25
print("Hello, {}! You are {} years old.".format(name, age))
```

- `{}` placeholders are replaced by values inside `.format()`.

## 4. Using f-Strings (Recommended)

```python
name = "Avinash"
age = 25
print(f"Hello, {name}! You are {age} years old.")
```

- `f"..."` allows inserting variables directly into strings.
- Cleaner and more readable than `.format()`.

# Escape Characters in Strings

Escape characters allow you to include special characters in strings.

| Escape Sequence | Meaning |
|----------------|---------|
| `\n` | New Line |
| `\t` | Tab Space |
| `\\` | Backslash (`\`) |
| `\'` | Single Quote (`'`) |
| `\"` | Double Quote (`"`) |

### Example:
```python
print("Hello,\nAvinash!")
# Output:
# Hello,
# Avinash!
```

# Type Conversion in Python

Sometimes, you need to convert one data type into another.

### Common Type Conversion Functions:
- `int(x)`: Converts `x` to an integer.
- `float(x)`: Converts `x` to a floating-point number.
- `str(x)`: Converts `x` to a string.
- `bool(x)`: Converts `x` to `True` or `False`.

### Example:
```python
num = "10"
converted_num = int(num)  # Now, converted_num is an integer
print(converted_num + 5)  # Output: 15
```

# Boolean Values (`True` and `False`)

Python has two Boolean values:
```python
print(True)  # Output: True
print(False)  # Output: False
```

## Boolean Operators:
- `and` (Both conditions must be `True`)
- `or` (At least one condition must be `True`)
- `not` (Negates the condition)

### Example:
```python
x = 10
y = 20
print(x > 5 and y < 30)  # True
print(x > 5 or y > 30)   # True
print(not(x > 5))        # False
```
# Removing Whitespace in Python  

## `.strip()` Method  
Removes leading and trailing whitespace from a string.  

### Example  
```python
text = "  Hello, World!  "
clean_text = text.strip()  
print(clean_text)  # Output: "Hello, World!"
```
# Capitalizing Strings in Python  

## `.capitalize()` Method  
Converts the first character to uppercase and the rest to lowercase.  

### Example  
```python
text = "hello world"
print(text.capitalize())  # Output: "Hello world"

```
# Title Case Strings in Python  

## `.title()` Method  
Converts the first letter of each word to uppercase and the rest to lowercase.  

### Example  
```python
text = "hello world"
print(text.title())  # Output: "Hello World"

```
# Splitting Strings in Python  

## `.split()` Method  
Splits a string into a list based on a specified delimiter (default: space).  

### Example  
```python
text = "hello world"
words = text.split()
print(words)  # Output: ['hello', 'world']

```

