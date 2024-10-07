# **Quick Reference Python Concepts and Commands**

### Data Types

Three common data types are strings, integers, and floats.

- **Strings** are sets of characters enclosed in quotation marks. Examples include:
  - `"Super!Password?123"`
  - `"Jane Doe"`
  - `"Once upon a time and a very good time it was there was a moocow coming down along the road."`

- **Integers** are whole numbers without quotation marks:
  - `1`, `-132`, `4358435789403`

- **Floats** are decimal numbers:
  - `3.4`, `5.34543`, `94948.2984758920`

### Variables

Variables store information for you to use repeatedly. To define a variable, use an `=` sign to assign a value:

```python
my_variable = some_value
age = 7
name = "Heavy Robot"
weight = 324.2
```

Each of these examples includes a variable, the assignment operator (`=`), and its value. Together, they form an expression.

### Functions

Functions always have parentheses immediately after their names. Python includes many built-in functions. Here are some common ones:

- `print()`: Prints to the console (but does not return anything).
- `input()`: Accepts user input.
- `int()`, `str()`, `float()`: Converts to data type.
- `max()`, `min()`: Returns maximum or minimum value from a list.
- `len()`: Returns the length of a string or list.
- `list()`: Converts an iterable to a list.
- `range()`: Returns a sequence of numbers.
- `enumerate()`: Returns both the index and the value of items in an iterable.
- `keys()`, `values()`: Returns the key or value of a dictionary entry.

Whatever goes inside the parentheses is called an **argument**. Multiple arguments are separated by a comma:

```python
print("This string is one argument")

second_argument = "This is the second argument"
print("This is the first argument", second_argument) # This print statement has two arguments, a string and a variable.

max(1,5,3,2,2) # This function has five arguments. It would return the maximum, 5. 
```

When you create (i.e., define) your own function, you can use any name that isn't already a built-in function, followed by `def`. For example:

```python
def add_two_numbers(x,y):
    print(x + y) 

add_two_numbers(4,6) # prints 10

def calculate_bmi(): 
    # code to calculate body mass index goes here

```

### Math Operators

Various mathematical operations using these common operators:

- **Addition (`+`)**: `3 + 2` results in `5`
- **Subtraction (`-`)**: `5 - 2` results in `3`
- **Multiplication (`*`)**: `4 * 3` results in `12`
- **Division (`/`)**:  `10 / 2` results in a float `5.0` 
- **Floor Division (`//`)**: `10 // 3` results in floor (rounded down) division `3`
- **Modulus (`%`)**: `10 % 3` results in the remainder `1`
- **Exponentiation (`**`)**: `2 ** 3` results in `8`

And don't forget built-in libraries.

- **Random**: import a PRNG (pseudorandom number generator) library of many built-in functions.

```python
import random

random_integer = random.randint(1, 10)  # Example: 7
random_float = random.random()  # Example: 0.456
random_float_range = random.uniform(1.0, 10.0)  # Example: 5.678
random_choice = random.choice(['apple', 'banana', 'cherry'])  # Example: 'banana'
my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)  # List might be shuffled to [3, 1, 5, 2, 4]

```

- **Math Library**: import built-in mathematical functions beyond basic operations.

```python
import math

square_root = math.sqrt(16)  # Returns 4.0
pi_value = math.pi  # Approximately 3.14159
square_root = math.sqrt(25)  # Returns 5.0
sine_value = math.sin(math.pi / 2)  # Returns 1.0
factorial_value = math.factorial(5)  # Returns 120


