# **Python Quick Reference**

Quick reference for Python fundamentals.

## Table of Contents
- [Data Types](#data-types)
- [Variables](#variables)
- [Built-in Functions](#built-in-functions)
- [Math Operators](#math-operators)
- [String Manipulation](#string-manipulation)
- [Boolean Operators](#boolean-operators)
- [Iteration](#iteration)
- [Lists](#lists)

## Data Types

Three common data types are strings, integers, and floats.

- **Strings** are sets of characters enclosed in quotation marks. Examples include:
  - `"Super!Password?123"`
  - `"Jane Doe"`
  - `"Once upon a time and a very good time it was there was a moocow coming down along the road."`

- **Integers** are whole numbers without quotation marks:
  - `1`, `-132`, `4358435789403`

- **Floats** are decimal numbers:
  - `3.4`, `5.34543`, `94948.2984758920`

- **Booleans** are True/False values:
  - `True == 1`, `False == 0` 


## Variables

Variables store information for you to use repeatedly. To define a variable, use an `=` sign to assign a value:

```python
my_variable = some_value
age = 7
name = "Heavy Robot"
weight = 324.2
```

Each of these examples includes a variable, the assignment operator (`=`), and its value. Together, they form an expression.

## Built-in Functions

Built-in Functions always have parentheses immediately after their names. Python includes many built-in functions. Their names are reserved keywords. Here are some common ones:

- `print()`: Prints to the console (but does not return anything).
- `input()`: Accepts user input.
- `int()`, `str()`, `float()`: Converts to data type.
- `max()`, `min()`: Returns maximum or minimum value from a list.
- `len()`: Returns the length of a string or list.
- `range()`: Returns a sequence of numbers.
- `enumerate()`: Returns both the index and the value of items in an iterable.
- `list()`: Converts an iterable to a list.
- `keys()`, `values()`: Returns the key or value of a dictionary entry.

Whatever goes inside the parentheses is called an **argument**. Multiple arguments are separated by a comma:

```python
length = len("Hello")  # One argument: a string.
# Returns the length of the string, which is 5.

print("Value:", 42)  # Two arguments: a string and a number.
# Displays "Value: 42" on the screen.

largest = max(4, 23, 8, 11, 2)  # Five arguments: a list of numbers.
# Returns the maximum value, which is 23.
```

When you create (i.e., define) a custom function, you can use any name that isn't already a built-in function, followed by `def` for "define". For example:

```python
def custom_adder(x,y):
    print(x + y) 

custom_adder(4,6) # Prints 10
```

## Math Operators

Various mathematical operations use these common operators:

`+`: Addition; 3 + 2 results in 5
`-`: Subtraction; 5 - 2 results in 3
`*`: Multiplication; 4 * 3 results in 12
`/`: Division; 5 / 2 results in a float 2.5
`//`: Floor (Rounded Down) Division; 5 // 2 results rounded down to 2
`%`: Modulus; 10 % 3 results in the remainder 1
`**`: Exponentiation; 2 ** 3 results in 8

And don't forget built-in libraries!

- **Random Library**: imports a PRNG (pseudorandom number generator) library of many built-in functions.

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

```
## String Manipulation 

### f-string Formatting 

F-strings are "formatted strings". Add the letter 'f' right before a string to let it take in dynamic variables or expressions, enclosed in braces {}. 

```python
food = "taco"
price = 5

## enclose your variable within the {} to display value
print(f"This {food} costs {price} dollars!?")
# Returns => This taco costs 5 dollars!?
```

### String Concatenation

Concatenate strings with a plus sign. 

```python
string1 = "Hello"
string2 = "World"

print(string1 + " " + string2 + "!")

# Prints Hello World! 
```

Note that the plus sign does not add strings together, even if they are numbers. 

```python
#integer datatype:
2 + 2 + 6 = 10

#string data type: 
'2' + '2' + '6' = 226
'two' + 'two' + 'six' = twotwosix
```

### String Splicing 

String splicing uses bracks, and the start and end index to cut up (slice) strings. 

```python
string = "abcdefghijklmnopqrstuvwxyz"

substring = string[11:16]   # => "lmnop"
substring2 = string[:4]     # => "abcd"
substring3 = string[22:]    # => "wxyz"
substring4 = string[-3:]    # => "xyz"

substring5 = string[::2]    # => "acegikmoqsuwy" (every second character)
substring6 = string[::-1]   # => "zyxwvutsrqponmlkjihgfedcba" (reversed string)
substring7 = string[1:8:2]  # => "bdfh" (every second character from index 1 to 7)
```

### String Functions

Various functions used to manipulate strings. Look up documentation for various uses and options. 

- `capitalize()`: Capitalizes word in string.
- `count()`: Counts occurance.
- `lower()`: Converts entire string to lowercase.
- `upper()`: Converts entire string to uppercase.
- `len()`: Returns integer of the length of a string. 
- `find()`: Returns integer of index location of a searched substring. 
- `replace()`: Returns a sequence of numbers.

Got it! Here are some common Boolean functions in that style:

## Boolean Operators

### Comparison Operators

- `==`: Equal to  
- `!=`: Not equal to  
- `>`: Greater than  
- `<`: Less than  
- `>=`: Greater than or equal to  
- `<=`: Less than or equal to

### Logical Operators

- `and`: Returns `True` if both operands are true. Example: `x and y`
- `or`: Returns `True` if at least one operand is true. Example: `x or y`
- `not`: Returns `True` if the operand is false. Example: `not x`
- `in`: Checks if a value exists within an iterable (like a string or list). Example: `x in list`
- `is`: Compares the identity of two objects. Example: `x is y`

### Boolean Functions

- `isdigit()`: Returns `True` if all characters in the string are digits. Example: `"1234".isdigit()`
- `isalpha()`: Returns `True` if all characters in the string are alphabetic. Example: `"abcd".isalpha()`
- `isalnum()`: Checks if all characters in a string are alphanumeric (letters and numbers).
- `isupper()`: Returns `True` if all characters in the string are uppercase. Example: `"HELLO".isupper()`
- `islower()`: Returns `True` if all characters in the string are lowercase. Example: `"hello".islower()`

## Iteration 

Iteration is when you repeat a set of instructions or steps multiple times, which helps you go through lists of items or perform tasks without writing the same code over and over again.

## While Loops  

Loops over iterable as long as a condition is True. Stops when the condition becomes False. 

```python
counter = 0

while counter < 5:
    counter += 1
    
print(counter)

# The while loop will run until the condition is False (when counter is not less than 5 anymore).
# Print statement returns 5 (not 4, since the loop increments before the condition fails).
```

## For Loops

Loops over iterable for a set number of times..

```python

numbers = [1, 2, 3]

for n in numbers:
    print(n * 2)

# The for loop will run until it reaches the end of the list, printing each number.
# Print statement returns:
# 2
# 4
# 6

```

**Using range()**

It is common to use the range() built-in function to return the indexes of an iterable. 

```python

numbers = [1, 2, 3]

for i in range(len(numbers)):
    print(i)

# The for loop will run until it reaches the end of the list, printing each index.
# Print statement returns:
# 0
# 1
# 2

```

### Lists
A list is a mutable (changeable) and iterable collection of data enclosed in square brackets, with elements separated by commas. Lists can contain items of different data types, including numbers, strings, and other lists.

```python
letters = ["a", "z", "d"]

print(letters[2]) 
# Displays "d", which is located at index 2

for letter in letters:
    print(letter.upper())

# Print statement displays letters in uppercase:
# A
# Z
# D

# Appending "m" to the list
letters.append("m")
# The list now becomes: ["a", "z", "d", "m"]
```

## List Functions 

- **`append(value)`**: Adds a value to the end of the list.  
  Example: `letters.append("m")`  
  Returns: `None` (the list now becomes `["a", "z", "d", "m"]`)
- **`pop(index)`**: Removes and returns the value at the last (or specified) index.  
  Example: `last_letter = letters.pop()`  
  Returns: `"m"` (if called after the previous example, the list now becomes `["a", "z", "d"]`)
- **`sort()`**: Sorts the list in ascending order (modifies the list in place).  
  Example: `letters.sort()`  
  Returns: `None` (the list now becomes `["a", "d", "z"]`)
- **`reverse()`**: Reverses the order of the list in place.  
  Example: `letters.reverse()`  
  Returns: `None` (the list now becomes `["z", "d", "a"]`)
- **`insert(index, value)`**: Inserts a value at a specified index.  
  Example: `letters.insert(1, "b")`  
  Returns: `None` (the list now becomes `["a", "b", "z", "d"]`)
- **`index(value)`**: Returns the index of the first occurrence of a specified value.  
  Example: `z_index = letters.index("z")`  
  Returns: `1`

## List Comprehension

Creates new list by applying an expression to each item in an iterable.

```python
squared_numbers = [n ** 2 for n in range(5)]  # Creates a list of squares: [0, 1, 4, 9, 16]
```



### More to come as we continue learning Python in class


