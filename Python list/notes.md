# Python List

## 1️⃣ What is a List in Python?

- A list is a collection of items in a particular order.

- Items can be of any type: numbers, strings, booleans, other lists, etc.

- Lists are mutable, meaning you can change, add, or remove elements.

- Lists are defined using square brackets [ ].

### Example:

``` pyhton
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "apple", True, 3.14]

Output:

print(fruits)   # ['apple', 'banana', 'cherry']
print(numbers)  # [1, 2, 3, 4, 5]
print(mixed)    # [1, 'apple', True, 3.14]
```
###Real-life analogy:

- Think of a list as a shopping bag. You can put anything inside (fruits, snacks, clothes), remove things, or rearrange them.

## 2️⃣ Why use Lists?

- To store multiple items in a single variable.

- To perform operations like adding, removing, searching, sorting, slicing.

- Efficient for data manipulation.

### Example:
```python
tasks = ["study", "exercise", "cook"]
tasks.append("sleep")  # add new task
print(tasks)

Output:

['study', 'exercise', 'cook', 'sleep']
```

## 3️⃣ List Operations / Logical Concepts

- Here’s what you can do logically with lists:

### Operation	Description	Example
    Access	      Get item by index	      fruits[0] → 'apple'
    Modify	      Change value at index  	fruits[1] = 'mango'
    Add	          Append or insert	      fruits.append('orange')
    Remove	      Remove an element      	fruits.remove('apple')
    Length	      Count items	            len(fruits)
    Slice	        Get sub-list	          fruits[1:3]
    Membership	  Check existence        	'apple' in fruits
    Loop	        Iterate	                for f in fruits: print(f)

## 4️⃣ List Built-in Methods
### A. Add Elements

#### 1. append(x) – Adds an element at the end of the list.
    🔹 What it does
    
    List ke end me ek single element add karta hai.
    
    🔹 Why use
    
    Jab data one by one add karna ho.
    
    🔹 Logic
    
    Existing list change hoti hai
    
    New element last index par jata hai


```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)

Output:

['apple', 'banana', 'cherry']
```
### 💡 Real-life: Adding a new item to your shopping cart.

#### 2. extend(iterable) – Adds multiple elements at the end.
    🔹 What it does
    
    Ek list me multiple elements add karta hai.
    
    🔹 Why use
    
    Jab do lists ko merge karna ho.
    
    🔹 Logic
    
    Iterable ke har element ko alag-alag add karta hai
    
    Nested list nahi banti

```pyhton
fruits.extend(["kiwi", "orange"])
print(fruits)

Output:

['apple', 'banana', 'cherry', 'kiwi', 'orange']
```
### 💡 Real-life: Combining two shopping bags.

#### 3. insert(index, x) – Inserts element at a specific position.

    🔹 What it does
    
    Specific position par element insert karta hai.
    
    🔹 Why use
    
    Jab order maintain karna ho.
    
    🔹 Logic
    
    Existing elements right shift hote hain

```python
fruits.insert(1, "mango")  # insert at 2nd position
print(fruits)

Output:

['apple', 'mango', 'banana', 'cherry', 'kiwi', 'orange']
```
### 💡 Real-life: Placing a book at a specific shelf position.

### B. Remove Elements

#### 1. remove(x) – Removes first occurrence of a value.
    🔹 What it does
    
    Value ke basis par element remove karta hai.
    
    🔹 Why use
    
    Jab exact value pata ho.
    
    🔹 Logic
    
    First occurrence remove hota hai
    
    Value na mile → ValueError

```python
fruits.remove("banana")
print(fruits)

Output:

['apple', 'mango', 'cherry', 'kiwi', 'orange']
```
### 💡 Real-life: Take out a spoiled fruit from your basket.

#### 2. pop(index=-1) – Removes element by index, returns it. Default is last.

    🔹 What it does
    
    Index ke basis par element remove + return karta hai.
    
    🔹 Why use
    
    Jab removed element ka use bhi karna ho.
    
    🔹 Logic
    
    Default → last element
    
    Stack behavior (LIFO)

```python
last_fruit = fruits.pop()
print(last_fruit)
print(fruits)

Output:

orange
['apple', 'mango', 'cherry', 'kiwi']
```
### 💡 Real-life: Picking the last item from a stack of plates.

#### 3. clear() – Removes all elements.
    🔹 What it does
    
    List ko completely empty kar deta hai.
    
    🔹 Why use
    
    Jab list reuse karni ho.

```python
fruits.clear()
print(fruits)

Output:

[]
```
###💡 Real-life: Empty your cart completely.

### C. Search / Count

### 1. index(x, start, end) – Returns index of first occurrence. Optional start/end.

    🔹 What it does
    
    Element ka index return karta hai.
    
    🔹 Logic
    
    First match return
    
    Na mile → ValueError

```python
nums = [10, 20, 30, 20]
print(nums.index(20))  # first 20
print(nums.index(20, 2))  # search from index 2

Output:

1
3
```
### 2. count(x) – Counts how many times x occurs.
```python
print(nums.count(20))

Output:

2
```
### 💡 Real-life: Count how many apples are in your basket.

#### D. Sort / Reverse

#### 1. sort(key=None, reverse=False) – Sorts the list (ascending default).
- sort() modifies the original list.
```python
nums.sort()
print(nums)
nums.sort(reverse=True)
print(nums)

Output:

[10, 20, 20, 30]
[30, 20, 20, 10]
```
### 💡 Real-life: Arrange books by height or alphabetical order.

#### 2. reverse() – Reverses the list order.
```python
nums.reverse()
print(nums)

Output:

[10, 20, 20, 30]
```
### 💡 Real-life: Flip the order of cards.

### E. Copy

#### 1. copy() – Returns a shallow copy of the list.
    🔹 Logic
    
    New list object
    
    Same values

```python
nums_copy = nums.copy()
print(nums_copy)

Output:

[10, 20, 20, 30]
```
### 💡 Real-life: Take a duplicate shopping list to check while shopping.

## 5️⃣ Built-in Functions That Work with Lists
### A. Information / Calculation
```python
numbers = [10, 20, 30, 40]

print(len(numbers))  # Number of elements
print(min(numbers))  # Minimum
print(max(numbers))  # Maximum
print(sum(numbers))  # Sum

Output:

4
10
40
100
```
### 💡 Real-life: Check how many items, cheapest, or total cost.

### B. Type & Conversion
```python
t = (1, 2, 3)
print(list(t))  # Convert tuple to list

s = "hello"
print(list(s))  # ['h', 'e', 'l', 'l', 'o']

numbers = [3, 1, 2]
print(sorted(numbers))  # Returns sorted list

Output:

[1, 2, 3]
['h', 'e', 'l', 'l', 'o']
[1, 2, 3]
```
### C. Iteration & Checking
```python
nums = [1, 2, 3]

# Enumerate (index + value)
for i, v in enumerate(nums):
    print(i, v)

# all() → True if all elements are True
print(all([True, True, False]))  # False

# any() → True if at least one element is True
print(any([False, False, True]))  # True

# zip → pair elements of two lists
-> pairs elements from multiple iterables index-wise and stops at the shortest iterable.
zip output empty	iterator already consumed
unequal length	shortest list used

a = [1, 2]
b = ["a", "b"]
print(list(zip(a, b)))

Output:

0 1
1 2
2 3
False
True
[(1, 'a'), (2, 'b')]
```
### 💡 Real-life: Enumerate → Serial number items, zip → Pair student names with marks.

###  6️⃣ List-Related Operations (Important)
    Operation    	  Example        	Output
    Indexing	      lst[0]	        first element
    Negative        Indexing	      lst[-1]	last element
    Slicing	        lst[1:3]	      sublist
    Membership	    "apple" in lst	True/False
    Concatenation	  [1,2]+[3,4]	    [1,2,3,4]
    Repetition	    [0]*3	          [0,0,0]
  ###  Real-life Examples / Logical Use Cases

## 🔥List ko list, tuple, dict, set ke andar kaha-kaha use kar sakte hain?

### 1️⃣ List ke andar List ✅ (Nested List)

    ✔ Allowed
    ✔ Very common
    ✔ Matrix / Table structure ke liye use hota hai
    
    data = [
        [1, 2, 3],
        [4, 5, 6]
    ]
    
    print(data[1][2])
    
    Output:
    
    6
    
    👉 Use case:
    Marks table, game board, 2D matrix

### 2️⃣ List ke andar Tuple ✅

    ✔ Allowed
    ✔ Immutable records store karne ke liye useful
    
    students = [
        ("Amit", 85),
        ("Neha", 90)
    ]
    
    print(students[0][1])
    
    Output:
    
    85
    
    👉 Real life:
    Student name + marks as fixed pair

### 3️⃣ List ke andar Dictionary ✅

    ✔ Allowed
    ✔ Very common in real projects
    
    users = [
        {"name": "Amit", "age": 22},
        {"name": "Neha", "age": 21}
    ]
    
    print(users[1]["name"])
    
    Output:
    
    Neha
    
    👉 Real life:
    Database records
    JSON data

### 4️⃣ List ke andar Set ✅

    ✔ Allowed
    ✔ But rare use
    
    data = [
        {1, 2, 3},
        {4, 5, 6}
    ]
    
    print(data[0])
    
    Output:
    
    {1, 2, 3}
### 5️⃣ Tuple ke andar List ✅ (Allowed)

    Tuple immutable hota hai,
    par uske andar list mutable ho sakti hai.
    
    t = ([1, 2, 3], 10)
    
    t[0].append(4)
    
    print(t)
    
    Output:
    
    ([1, 2, 3, 4], 10)
    
    🔥 Important Interview Concept:
    Tuple immutable hai,
    but uske andar ka object mutable ho sakta hai.

### 6️⃣ Dictionary me List as Value ✅

    ✔ Very common
    
    student = {
        "name": "Amit",
        "marks": [80, 90, 85]
    }
    
    print(student["marks"][1])
    
    Output:
    
    90
    7️⃣ Dictionary me List as Key ❌ (NOT Allowed)
    d = {
        [1,2,3]: "data"
    }
    
    ❌ Error aayega:
    
    TypeError: unhashable type: 'list'
    
    👉 Reason:
    Dictionary keys hashable hone chahiye
    List mutable hoti hai → hashable nahi hoti

### 8️⃣ Set ke andar List ❌ (NOT Allowed)
    s = { [1,2,3] }
    
    ❌ Error:
    
    TypeError: unhashable type: 'list'
    
    👉 Reason same:
    Set me elements hashable hone chahiye.

### 🔥 Important Concept: Hashable vs Mutable
    Type        	Mutable?	      Hashable?    	Set/Dict Key me allowed?
    List	        Yes	            ❌ No	        ❌
    Tuple	        No	            ✅ Yes	      ✅
    String	      No	            ✅ Yes	      ✅
    Set	          Yes	            ❌ No	        ❌
### 🎯 Final Interview Summary

    ✔ List ke andar → List, Tuple, Dict, Set sab aa sakte hain
    ✔ List Dict ke value me aa sakti hai
    ❌ List Dict ke key me nahi aa sakti
    ❌ List Set ke andar nahi aa sakti

- "List is mutable and unhashable, so it cannot be used as a dictionary key or set element."

