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

## Python mein data types 2 categories mein divided hote hain:
 1. Mutable Data Types
 2. Immutable Data Types

### * Mutable Data Types
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

### * Immutable Data Types
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

## Numeric Data Type
Numeric data types numbers ko represent aur store karne ke liye use hote hain, jinke upar mathematical operations perform kiye ja sakte hain.

### Types of Numeric Data Types in Python
Python me 3 numeric data types hote hain:
  - 1️⃣ int
  - 2️⃣ float
  - 3️⃣ complex
### Note:-
- Type Promotion Rule (Common for all numeric types)

      int → float → complex
      (lower precision → higher precision)
  
      Matlab:
      int + complex → complex
      float + complex → complex
  
1️⃣ *int (Integer)* :
  int whole numbers ko represent karta hai, bina decimal ke.
  
🔹 Example

      a = 10
      b = -25
      c = 0

🔹 Key Points
   - Decimal allowed nahi hota
 ```python
print(int(3.9)  # 3 (Reason : truncate , not round)
```
   - Python me integer size unlimited hota hai (memory ke hisaab se)
```python
x = 999999999999999999999
print(type(x))   # int
```
- Small integer cache(-5 to 256)
```python
a= 256
b= 256
print(a is b) # True
```
- ==(double eqaul) : value comparison
- is : memory location comparison
- bool is the subset of integer
    - bool(0) : False (for zero)
    - bool(1) : True  (for every non zero val.)
- String to int (base 10 by default)
```python
print(int("10")   # 10
print(int("-25")  #-25
```
- String with base: syntax -> int(string,base)
  - base 2(binary)

        int("101",2)  # 5 (binary)
        - "101" -> binary number
        - base -> 2
        Digit         place value
        1              2^2
        0              2^1
        1              2^0
        calculation:  1*2^2+0*2^1+1*2^0
                      4+0+1=5
  - base 16(Hexadecimal)

         1> int("A",16)  # 10 
          - "A" -> hexadecimal digit
          - base -> 16
          Hex digit mapping
            0-9 -> 0-9
            A -> 10
            B -> 11
            ...
            F -> 15
          2> int("1A",16)  # 26 
            hex number =1A
            Digit    value    power of 16
            1          1      16^1
            A          10     16^0
            calculation:  (1*16^1)+(10*16^0)
                          = 1*16+10*1
                          = 16+10=26
            
         
          
2️⃣ *float (Floating Point)*:
    float decimal numbers ko represent karta hai.
    
🔹 Example

    x = 3.14
    y = -0.5
    z = 1.0

    float(10)  # 10.0
    float("10.5")  # 10.5
    float("-3.2")  #-3.2
    float("ab")   #error

🔹 Scientific Notation

    a = 1e3     # 1000.0
    b = 2e-2    # 0.02

🔹 Key Points
     - Range : Approx 1.7e-308 to 1.8e+308 (IEEE 754)   
     - 0.1+0.2 = 0.3 ❌ ❔🤔
  ```python
  print(0.1 + 0.2)  
  # 0.30000000000000004
  ```
  - Reason : - Float binary format me store hota hai, kuch decimal value exactly represent nhi hoti h
  - solution :
```python
        #1) round()
         print(round(0.1+0.2,1)  # 3.0

        # 2) decimal module
        from decimal import Decimal
        a=Decimal.('0.1')
        b=Decimal.('0.2')
        print(a+b)    # 0.3

        # 3) math.isclose() -> float comparison
        import math
        print(math.isclose(0.1+0.2,0.3)  # True
        #==
        print(0.1+0.2==0.3)  # False
```
### Note: *Never compare float using ==(double equal)❌ , use math.isclose()✅*
### *round()*: Python ka built-in function hai jo number ko nearest value tak round karta hai.
      Call	          Return
      round(x)	      int
      round(x, n)	    float            
  - round(number, n)
    - number → int / float
    - n = number of decimal places(optional)
    - n positive, zero ya negative ho sakta hai
  - Rule:
    - decimal < 0.5 → down
    - decimal > 0.5 → up
    - decimal = 0.5 → ⚠️ special rule (bankers rounding -> Even(Nearest))
  - Exmple:

        # when n positive
        round(12.4) → 12
        round(12.6) → 13
        round(12.5) → 12   ❗(12 is Even)
        round(13.5) → 14   ❗(14 is Even)

        # when n=0  (Nearest integer, but float return hota hai)
        round(12.6, 0) → 13.0
        round(12.5, 0) → 12.0
        round(13.5, 0) → 14.0

        when n negetive : Left side rounding (tens, hundreds, thousands)
        round(1234, -2) → 1200
        round(1299, -2) → 1300
        round(1500, -3) → 2000
    
### Note: *“Python round() uses bankers rounding (round half to even). Normal rounding behavior appears only when the value is not exactly halfway.”✅*

### *Special floating point value*, jo invalid mathematical result ko represent krta hai.
    - float('inf') -> +∞
    - float('-inf') -> -∞
    - float('nan')  -> NaN
### Note: - *NaN kisi se equal nhi hota h,even itself.*
- Example:
```python
    #NaN
    x= float('nan')
    print(x==x)   # False

    #inf
    x=float('inf')-float('inf')
    print(x)      #nan
``` 
      
3️⃣ *complex (Complex Number)* :
   complex numbers real + imaginary part se milkar bante hain.

🔹 Format

    # z = a + bj   # (j=√-1)
     where a = real part 
           b = img part 
    # z = complex(2,3)
     print(z)      # (2+3j)
  
🔹 Example
```python
c = 5 + 4j
print(type(c))  # complex
print(c.real)   # 5.0
print(c.imag)   # 4.0
```

🔹 Key Points
  - j imaginary part ko represent karta hai
  - Mostly scientific, ML, signal processing me use hota hai
  - No fixed range(real + img part follow float range)

         -> (2+3j)>(1+2j)  # TypeError
            complex number ka ordering define nhi hota h.
         -> (2+3j)==(2+3j)  # True
         -> z= 3+4j
            print(abs(z)) # 5.0
            Formula : √(r²+i²)
         -> print(5+(2+3j))      # (7+3j)
         -> print(2.5+(1+2j))    # (3.5+2j)
            int/float automatically complex me convert ho jata h.
         -> int(2+3j)      # ❌ TypeError
         -> float(2+3j)    # ❌ TypeError
            complex ko int/float me convert nhi kr skte h

📌 Type Conversion (Numeric)

     int(3.7)      # 3
     float(5)      # 5.0
     complex(2,3)  # 2+3j

📌 Interview One-Liner ⭐

      “Numeric data types in Python are int, float, and complex, used to store numerical values.”
