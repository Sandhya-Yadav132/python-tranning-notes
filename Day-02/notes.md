# Day 02 - Python Basics
## 8) Data Types:Data types define the type of data a variable can store in Python.
  Python has the following data types built-in by default, in these categories:

  - Text Type:	str
  - Numeric Types:	int, float, complex
  - Sequence Types:	list, tuple, range
  - Mapping Type:	dict
  - Set Types:	set, frozenset
  - Boolean Type:	bool
  - Binary Types:	bytes, bytearray, memoryview
  - None Type:	NoneType

## Python mein data types do categories mein divided hote hain:
 1. Mutable Data Types
 2. Immutable Data Types

### Mutable Data Types
  Mutable data types wo hote hain jinhe hum modify kar sakte hain bina unka memory address change kiye.
### Examples of Mutable Data Types:
     1. Lists
     2. Dictionaries   
     3. Sets

### Example of Mutable Data Type - List
```python
  my_list = [1, 2, 3]
  print("Original List:", my_list)
  my_list[0] = 10  # Modifying the first element
  print("Modified List:", my_list)
  print("Memory Address of List:", id(my_list))
```

### Immutable Data Types
  Immutable data types wo hote hain jinhe hum modify nahi kar sakte bina unka memory address change kiye.
### Examples of Immutable Data Types:
     1. Strings
     2. Tuples
     3. Numbers (int, float, complex)

### Example of Immutable Data Type - String
```python
  my_string = "Hello"
  print("Original String:", my_string)
  # Attempting to modify the first character (this will create a new string)
  new_string = 'h' + my_string[1:]
  print("Modified String:", new_string)
  print("Memory Address of Original String:", id(my_string))
  print("Memory Address of Modified String:", id(new_string))
```

### Example of Immutable Data Type - Tuple
```python
  my_tuple = (1, 2, 3)
  print("Original Tuple:", my_tuple)
  # Attempting to modify the first element (this will create a new tuple)
  new_tuple = (10,) + my_tuple[1:]
  print("Modified Tuple:", new_tuple)
  print("Memory Address of Original Tuple:", id(my_tuple))
  print("Memory Address of Modified Tuple:", id(new_tuple))
```

### Example of Immutable Data Type - Number
```python
  my_number = 100
  print("Original Number:", my_number)
  # Modifying the number (this will create a new number)
  my_number += 50
  print("Modified Number:", my_number)
  print("Memory Address of Modified Number:", id(my_number))
```

### Summary
 Mutable data types can be changed without changing their memory address,
 while immutable data types create new objects in memory when modified.

### Setting the Data Type
  In Python, the data type is set when you assign a value to a variable:

    x = "Hello World"  # str
    x = 20            # int
    x = 20.5          # float
    x = 1j            # complex
    x = ["apple", "banana", "cherry"]  # list
    x = ("apple", "banana", "cherry")  # tuple
    x = range(6)      # range
    x = {"name" : "John", "age" : 36}  # dict
    x = {"apple", "banana", "cherry"}  # set
    x = True          # bool
