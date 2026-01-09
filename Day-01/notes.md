# Day 01 – Python Basics

## 1) Python Introduction
- Python is a high-level, interpreted programming language
- Created by Guido van Rossum
- First released in 1991

## Compiler vs Interpreter (Complete but Short)

### Compiler: Poore source code ko ek saath machine code me convert(translate krke .exe file) karta hai, phir execution (by CPU )hota hai.

### Interpreter: Source code ko line by line read, translate aur execute karta hai.(Runtime pr)

### Execution

- Compiler: Translation before execution

- Interpreter: Translation during execution

### Error Handling

- Compiler: Saare errors ek saath batata hai

- Interpreter: Line-wise error, error aate hi execution stop

### Speed

- Compiler: Execution fast (machine code pehle se bana(.exe file) hota hai)

- Interpreter: Execution slow (runtime translation hota hai)

### Memory

- Compiler: Zyada memory use (object/exe file banti hai)

- Interpreter: Kam memory, koi separate .exe  file nahi

### Portability

- Compiler: Platform dependent(Why :👉 Windows ka .exe Linux samajh hi nahi sakta)

- Interpreter: Platform independent (interpreter ho to code chalega)--Hr OS ke liye Python interpreter already available hota hai

### Examples

- Compiler Languages: C, C++

- Interpreter Languages: Python, JavaScript

### Important Note

- 👉 Python fully interpreted nahi hai (bytecode(.pyc compiled internally) + Python Virtual Machine use karta hai)


## Why Learn Python?
- Easy to learn
- Versatile (Web Development, Data Science, AI, Automation)
- Large community:-Extensive libraries
- High demand

## 2) Python Installation
- Download Python from:
  - https://www.python.org/downloads/

### Check if Python is installed
- `python --version`
- `python -V`
- `py --version`

## 3) Python Syntax
- File extension: `.py`
- Indentation:-indicates blocks of code
- Python is case sensitive

## 4) Python Indentation: It is the leading whitespaces before any statement in python
  ### purpose:
    - Improve readability
    - Helps in indicating a block of code
  ### Rules:
    - Minimum one space is neccessary to represent an indented statements.
    - The first line of python code can't have indentaion.
    - Indentation is mandantory to define a block of code.
    - The number of space must be *Uniform*.
                
### 1.Example (Correct ✅)
```python
if 5 > 2:
    print("Hello")
```
### 1.Example (InCorrect ❌ ( There is an Indentation error) )
```python
if 5 > 2:
print("Hello")
```
## 5) Python Comments 
### Non-executable lines in a program
  ### 1. single line commentu
      - Used for a single line
      - Start with `#`
      Example 
      ```python  
      # This is a single-line comment
      print("Hello world")
      ```
     
 ### 2. Multi line commentu
      - Python does not really have a syntax for multi line comments. To add a multiline comment you could insert a # for each line
      - you can add a multiline string (triple quotes) in your code, and place your comment inside it

## 6) Python Variables
### This is a name used to store data values
###  Variable Naming Rules: 
      . variable name only start from * letter *, *_*
      . Do not allow *space* and *Special Characters( @,#,$)* in var name *!*
      . Variable name is case sensitive 
      . A variable name cannot be a *Keyword*
  ### Examples
  - age=20          ✅
  - _total=100      ✅
  - 2namw="hello"   ❌
  - t6 = "Sandhya"  ✅
  - My name="hello" ❌! 
  - My_name="hello" ✅
  - name@ =5        ❌ !

### Multi Value assign:
- Python me multi-value assignment = ek saath 2 ya zyada variables ko values assign karna
- Ye code ko short, readable aur easy to use banata hai
- Swapping, unpacking, function return values, loops me kaafi useful hai
```python
  a, b = 10, 20 # multi value assign
  a, b = b, a   # swap values
```

## 7) Python Memory Management
- Python automatically memory allocate aur deallocate(free) karta hai, programmer ko manually *malloc/free*  nhi likhna pdta hai.
- Python private Heap memory use krta hai.
- All objects(int,list,dict,class) heap me store hote hai.

### Memory management techniques
-  Reference counting
  - Har object k sath reference count hota hai.
  - Reference count = no. of variables pointing object.
  - count = 0 -> memory free.
  *Example*
    ```python
    a=10   
    b=a    #ref= 2
    del a  # ref=1
    del b  # ref=0 -> memory free
    ```
-  Garbage collection
    - Cyclic reference handle krta hai.
    - Background me automatically run hota hai.
  ```python
  import gc
  gc.collect()
  ```
  *Example*
  ```python
  a=[]
  b=[]
  a.append(b)
  b.append(a)
  ```
  - Reference count 0 nhi hota h
  - GC memory free karta hai.
### Memory optimization(caching)
  Small interger cache.
    - -5 to 256 cached hote hai.
  ```python
    a=100
    b=100
    print(a is b)  #true
  ```
  String interning
  ```python
  a="hello"
  b="hello"
  print(a is b) # true
  ```
### *del* keyword
- object ka ref. delete krta hai.
- memory turant free hona guaranteed nhi.

### Memory leak
- It means unused memory is not released after use program.
Avoid ?
- use ke baad var delete kre -> del data
- file & DB connection close kre -> file.close()
- global var km rkhe.
- weak ref. use kre -> import weakref
