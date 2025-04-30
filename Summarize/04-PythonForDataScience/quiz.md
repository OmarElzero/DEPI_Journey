# Python for Data Science Quiz

## Basic Python Concepts

1. **What will be the output of the following code?**
   ```python
   x = 10
   y = 20
   x, y = y, x
   print(x, y)
   ```
   - A) 10, 20
   - B) 20, 10
   - C) Error
   - D) None of the above

2. **Which of the following is the correct way to create an f-string in Python?**
   - A) f"The value is {x}"
   - B) "The value is {x}".format()
   - C) "The value is %s" % x
   - D) "The value is " + x

3. **What is the output of `print(5 // 2)`?**
   - A) 2.5
   - B) 2
   - C) 3
   - D) 2.0

## Data Structures

4. **Which of the following data structures in Python is mutable?**
   - A) Tuple
   - B) String
   - C) List
   - D) All of the above

5. **What will the following code print?**
   ```python
   names = ['Ahmed', 'Ali', 'Mohamed']
   names.append('Basma')
   print(names[1])
   ```
   - A) Ahmed
   - B) Ali
   - C) Mohamed
   - D) Basma

6. **Given the dictionary below, how would you access the age of the person?**
   ```python
   person = {'name': 'Ahmed', 'age': 25, 'city': 'Cairo'}
   ```
   - A) person.age
   - B) person[age]
   - C) person['age']
   - D) person.get('age')

7. **What is the output of the following code?**
   ```python
   a = [1, 2, 3]
   b = a
   b.append(4)
   print(a)
   ```
   - A) [1, 2, 3]
   - B) [1, 2, 3, 4]
   - C) [4, 1, 2, 3]
   - D) Error

## Functions and Control Flow

8. **What is the difference between `return` and `print` in a function?**
   - A) They are the same
   - B) `return` ends the function execution and returns a value, while `print` displays output
   - C) `print` ends the function execution, while `return` continues execution
   - D) `return` can only be used with numbers, while `print` works with all data types

9. **What will the following code output?**
   ```python
   def my_function(a, b=10):
       return a + b

   print(my_function(5))
   ```
   - A) 5
   - B) 10
   - C) 15
   - D) Error

10. **Which of these is a valid way to define a function with a variable number of arguments?**
    - A) `def func(*args):`
    - B) `def func(...args):`
    - C) `def func(args[]):`
    - D) `def func(args...):`

## Object-Oriented Programming

11. **What is a class attribute in Python?**
    - A) An attribute defined inside a method
    - B) An attribute shared by all instances of a class
    - C) An attribute that can only be accessed inside the class
    - D) An attribute with a default value

12. **What does the `self` parameter represent in a class method?**
    - A) The class itself
    - B) The current instance of the class
    - C) A mandatory Python parameter name
    - D) The parent class in inheritance

13. **Which of the following is used to define a constructor in a Python class?**
    - A) `__new__()`
    - B) `__init__()`
    - C) `__constructor__()`
    - D) `__create__()`

## Data Science with Python

14. **Which Python library is primarily used for data manipulation and analysis?**
    - A) matplotlib
    - B) scikit-learn
    - C) pandas
    - D) TensorFlow

15. **What does the following code accomplish?**
    ```python
    import numpy as np
    arr = np.array([1, 2, 3, 4, 5])
    print(arr.mean())
    ```
    - A) Sorts the array
    - B) Calculates the median of the array
    - C) Calculates the average of the array
    - D) Finds the maximum value in the array

## Practical Tasks

16. **Write a function that takes a list of numbers and returns the sum of all even numbers in the list.**

17. **Create a class named `Rectangle` with attributes `length` and `width`, and methods to calculate area and perimeter.**

18. **Write a Python program that reads a CSV file named "data.csv" and prints the average value of a column named "temperature".**

19. **Create a function that takes a string and returns a dictionary containing the count of each character in the string.**

20. **Using list comprehension, write a single line of code that creates a list containing the squares of all even numbers from 1 to 20.**

## Answer Key

1. B) 20, 10
2. A) f"The value is {x}"
3. B) 2
4. C) List
5. B) Ali
6. C) person['age'] or D) person.get('age')
7. B) [1, 2, 3, 4]
8. B) `return` ends the function execution and returns a value, while `print` displays output
9. C) 15
10. A) `def func(*args):`
11. B) An attribute shared by all instances of a class
12. B) The current instance of the class
13. B) `__init__()`
14. C) pandas
15. C) Calculates the average of the array

16. **Solution:**
```python
def sum_even(numbers):
    return sum(num for num in numbers if num % 2 == 0)
```

17. **Solution:**
```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width
        
    def area(self):
        return self.length * self.width
        
    def perimeter(self):
        return 2 * (self.length + self.width)
```

18. **Solution:**
```python
import pandas as pd

def average_temperature(filename):
    df = pd.read_csv(filename)
    return df['temperature'].mean()
    
# Call with: average_temperature("data.csv")
```

19. **Solution:**
```python
def char_count(string):
    return {char: string.count(char) for char in set(string)}
```

20. **Solution:**
```python
squares_of_even = [x**2 for x in range(1, 21) if x % 2 == 0]
```