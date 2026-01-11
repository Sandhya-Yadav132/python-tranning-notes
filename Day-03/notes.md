# Day 03 - Python Basics
## String Data Types
- A string in Python is an immutable sequence of Unicode characters enclosed in quotes(' ', " ", ''' ''').
  - Unicode ek international standard hai jo har language ke characters ko unique number (code) deta hai. Python 3 strings are Unicode by default.
  👉 Matlab:

        English letters (A, a)
        Hindi letters (अ, आ)
        Numbers (1, २)
        Emojis (😊 😂)
        Symbols (₹, €, @)
        sab Unicode characters hote hain.
- Example:
 ```python
s1 = "Hello"
s2 = 'Python'
s3 = """This is
multi-line string"""
```
### Note : *"All string methods return a new string because strings are immutable."*
### # Important Properties
  1. Immutable
```python
s = "Hello"
s[0] = "h"   # ❌ Error
```
👉 String change nahi hoti, naya string banta hai
  2. Indexing
```python
s = "Python"
print(s[0])   # P
print(s[-1])  # n
```
 3. Slicing
```python
s = "Python"
print(s[1:4])   # yth
print(s[::-1])  # nohtyP
```
### # String Operators(Concatenation(+),Repetition(*),Membership(in))
```python
print("Data"+" "+"Structure")  #Data Structure
print("Py" in "Python")   # True
print("Hi" * 3)           # HiHiHi
```
### # Important String Functions
  1. Case Conversion
```python
s = "python"
print(s.upper())      # PYTHON
print(s.lower())      # python
print(s.title())      # Python
print(s.capitalize()) # Python
```
  2. Check Functions (Boolean return)
```python
print("abc".isalpha())     # True
print("123".isdigit())     # True
print("abc123".isalnum())  # True
print(" ".isspace())       # True
```
  3.Searching and checking
```python
s = "hello world"
print(s.find("o"))     # 4
print(s.index("o"))    # 4
print(s.count("l"))    #
```
- 👉 Difference:

      find() → -1 return if not found
      index() → error if not found
      count() → count occurence (0 if not found)
  4 . Replace and modify
```python
s = "hello"
print(s.replace("l", "L"))   # heLLo
```
  5. split and join
```python
s = "a,b,c"
print(s.split(","))    # ['a','b','c']

print("-".join(["a","b","c"]))  # a-b-c
```
  6. Strip (remove spaces)
      

