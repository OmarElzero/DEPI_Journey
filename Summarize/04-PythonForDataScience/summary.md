# Python for Data Science, AI & Development

## Introduction to Python
Python has become the language of choice for data science and AI development due to its readability, extensive libraries, and flexible programming paradigms.

### Why Python?
- **Readability**: Clean syntax that resembles English
- **Versatility**: Can be used for web development, data analysis, AI, scientific computing
- **Rich Ecosystem**: Extensive libraries specifically designed for data science (NumPy, pandas, matplotlib)
- **Community Support**: Large community with abundant resources and documentation

### Programming Fundamentals

#### Basic Syntax and Data Types

1. **Print Statements and String Operations**
```python
print("Hello world!")  # Basic print
print('Sum =', 20+30)  # Print with multiple arguments
print(f"The answer is {10+20}")  # f-string formatting
```

2. **Variables and Assignment**
```python
x = 5  # Integer
name = "Data Science"  # String
is_valid = True  # Boolean
```

3. **Core Data Types**
   - **Numbers**: `int`, `float`, `complex`
   - **Strings**: Text sequences (`str`)
   - **Boolean**: `True` or `False`
   - **None**: Represents absence of value

4. **Basic Operations**
   - Arithmetic: `+`, `-`, `*`, `/`, `//` (floor division), `%` (modulo), `**` (exponent)
   - String operations: concatenation (`+`), repetition (`*`), slicing (`[:]`)

5. **User Input and Type Conversion**
```python
name = input("Enter your name: ")  # Always returns string
age = int(input("Enter your age: "))  # Convert to integer
```

## Data Structures

### Lists
Ordered, mutable collections that can contain mixed data types.

```python
names = ['mahmoud', 'ali', 'ahmed', 'mohamed']
names.append('Basma')  # Add element
names.insert(1, 'Sara')  # Insert element at position
names.remove('ali')  # Remove element by value
popped_name = names.pop()  # Remove and return last element
```

**List Operations**:
- Slicing: `names[1:3]`
- Length: `len(names)`
- Sorting: `names.sort()` or `sorted(names)`
- Membership: `'ali' in names`
- List comprehension: `squares = [x**2 for x in range(1,11)]`

### Dictionaries
Key-value pairs that allow fast lookups by key.

```python
user = {
    'Name': 'Ali',
    'Age': 25,
    'Address': 'Egypt'
}

# Access, modify, add values
print(user['Name'])
user['Age'] = 26
user['Occupation'] = 'Data Scientist'

# Dictionary methods
user.keys()  # Returns keys
user.values()  # Returns values
user.items()  # Returns (key, value) tuples
user.get('Salary', 'Not specified')  # Get with default value
```

### Tuples
Immutable ordered sequences.

```python
dimensions = (200, 50)  # Cannot be modified after creation
```

### Sets
Unordered collections of unique elements.

```python
unique_ids = {1, 2, 3, 4, 5}
unique_ids.add(6)  # Add element
unique_ids.discard(2)  # Remove element if present
```

## Control Flow

### Conditional Statements
```python
age = 25
if age < 18:
    print("Minor")
elif age < 65:
    print("Adult")
else:
    print("Senior")
```

### Loops

1. **For Loops**
```python
for name in names:
    print(name)

for i in range(1, 11):
    print(i**2)
```

2. **While Loops**
```python
number = 1
while number <= 5:
    print(number)
    number += 1
```

3. **Loop Control**
   - `break`: Exit the loop
   - `continue`: Skip to the next iteration
   - `pass`: Do nothing (placeholder)

## Functions

```python
# Basic function definition
def greet(name):
    """Display a simple greeting."""
    return f"Hello, {name}!"

# Function with default parameter
def describe_pet(name, animal_type='dog'):
    return f"I have a {animal_type} named {name}."

# Multiple parameters
def calculate_area(length, width):
    return length * width
```

### Args and Kwargs
Allow for flexible argument passing:

```python
# Variable number of positional arguments
def mean(*nums):
    return sum(nums) / len(nums)

# Variable number of keyword arguments
def create_profile(**details):
    return details
```

## Modules and Imports

```python
# Importing a module
import math
print(math.sqrt(16))

# Importing specific functions
from math import sqrt, pi

# Renaming imports
import pandas as pd
import numpy as np
```

## File Handling

```python
# Reading from a file
with open('data.txt', 'r') as f:
    data = f.read()

# Writing to a file
with open('output.txt', 'w') as f:
    f.write("Hello, world!")
```

## Object-Oriented Programming

### Classes and Objects

```python
class Dog:
    species = "Canis familiaris"  # Class attribute
    
    def __init__(self, name, age):
        self.name = name  # Instance attributes
        self.age = age
        
    def __str__(self):
        return f"{self.name} is {self.age} years old"
        
    def speak(self, sound):
        return f"{self.name} says {sound}"
```

### Inheritance

```python
class Parent:
    hair_color = "brown"
    
    def walk(self):
        return "Walking"
        
class Child(Parent):
    def run(self):
        return "Running"
```

### OOP Principles
1. **Encapsulation**: Bundling data and methods that work on that data
2. **Abstraction**: Hiding complex implementation details
3. **Inheritance**: Creating a child class from a parent class
4. **Polymorphism**: Different classes can be used with the same interface

## Python for Data Science Applications

### Key Data Science Libraries
- **NumPy**: Numerical computing with arrays and matrices
- **Pandas**: Data manipulation and analysis
- **Matplotlib/Seaborn**: Data visualization
- **Scikit-learn**: Machine learning

### Common Data Science Tasks with Python
- Data collection (APIs, web scraping)
- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Model building and evaluation
- Data visualization

## Best Practices for Python in Data Science
1. Use descriptive variable and function names
2. Document your code with comments and docstrings
3. Follow PEP 8 style guidelines
4. Write modular, reusable code
5. Use version control (Git)
6. Create virtual environments for project dependency management
7. Write tests for your code
