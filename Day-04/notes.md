# Tuple 
## ✅ What is a Tuple?

- A tuple is an ordered, immutable collection of elements in Python.

### 👉 Immutable means: once created, you cannot change its elements.

## 🔹 How to Create a Tuple
```python
  t = (10, 20, 30)
  print(t)
```
### Note:

✔ Parentheses () are commonly used

✔ Comma , is the real identifier of a tuple

## 🔹 Tuple with One Element (Very Important ❗)
- t1 = (10)      # ❌ Not a tuple (int)
- t2 = (10,)     # ✅ Tuple


### 👉 Comma is mandatory for a single-element tuple.

## 🔹 Tuple Without Parentheses
```python
t = 1, 2, 3
print(t)       # (1, 2, 3)
```
## 🔹 Accessing Tuple Elements (Indexing)
```python
t = (10, 20, 30, 40)
print(t[0])    # 10
print(t[-1])   # 40
```

## 🔹 Tuple is Immutable ❌
```python
t = (1, 2, 3)
t[0] = 100     # ❌ Error: TypeError
```

### 👉 This is the key difference between list & tuple.

## 🔹 Tuple Slicing
```python
t = (10, 20, 30, 40, 50)
print(t[1:4])   # (20, 30, 40)
```

## 🔹 Tuple Methods (Only 2)
```python
t = (10, 20, 20, 30)
print(t.count(20))   # 2
print(t.index(30))   # 3
```

### 👉 Because tuple is immutable, methods are very few.

## 🔹 Tuple Packing & Unpacking (Very Important for Interview)
```python
# Packing
t = 10, 20, 30

# Unpacking
a, b, c = t
print(a, b, c)   # 10 20 30
```
## 🔹 Swapping Using Tuple 🔁
```python
a = 5
b = 10

a, b = b, a
print(a, b)   # 10 5
```

## 🔹 Tuple with Different Data Types
```python
t = (1, "hello", 3.5, True)
print(t)
```
## 🔹 Nested Tuple
```python
t = (1, (2, 3), (4, 5))
print(t[1][0])   # 2
```

## 🔹 Why Use Tuple? (Interview Answer)

- ✔ Faster than list
- ✔ Data safety (immutable)
- ✔ Can be used as dictionary keys
- ✔ Used when data should not change

## 🔹 When to Use Tuple?

- Fixed data (days, months, coordinates)

- Return multiple values from a function

- Dictionary keys


# Set 

## 🔹 What is a Set in Python?

- Set unordered collection hota hai
- Duplicate values allowed nahi hoti
- Mutable (change ho sakta hai)
```python
s = {1, 2, 3, 3}
print(s)   # {1, 2, 3}
```
## 🟢 Add Elements
### 1️⃣ add(x)

➡ Single element add karta hai
```python
s = {1, 2}
s.add(3)
print(s)   # {1, 2, 3}
```

📌 Agar element already present hai → koi change nahi

### 2️⃣ update(iterable)

➡ Multiple elements add karta hai (list, tuple, set)
```python
s = {1, 2}
s.update([3, 4, 5])
print(s)   # {1, 2, 3, 4, 5}
```

- 📌 add() = single
= 📌 update() = multiple

🔴 Remove Elements
### 3️⃣ remove(x)

- ➡ Element remove karta hai
- ❌ Agar element nahi mila → KeyError
```python
s = {1, 2, 3}
s.remove(2)
print(s)   # {1, 3}
``` 
### 4️⃣ discard(x)

- ➡ Element remove karta hai
- ✅ Agar element nahi mila → no error
```python
s = {1, 2, 3}
s.discard(5)   # no error
print(s)
```

- 📌 Interview tip:
- remove() error deta hai, discard() safe hota hai

### 5️⃣ pop()

➡ Random element remove karta hai (unordered)
```python
s = {1, 2, 3}
x = s.pop()
print(x)
print(s)
```

📌 Pop ka element fixed nahi hota

### 6️⃣ clear()

➡ Set ko empty bana deta hai
```python
s = {1, 2, 3}
s.clear()
print(s)   # set()
```
## 🔵 Set Operations (New Set Return)
### 7️⃣ union()

➡ Dono sets ke saare unique elements
```python
a = {1, 2, 3}
b = {3, 4}
print(a.union(b))   # {1, 2, 3, 4}
```
### 8️⃣ intersection()

➡ Common elements

print(a.intersection(b))   # {3}

### 9️⃣ difference()

➡ A - B

print(a.difference(b))   # {1, 2}

### 🔟 symmetric_difference()

➡ Common hata ke baaki

print(a.symmetric_difference(b))   # {1, 2, 4}

## 🟡 Update Operations (Original Set Change)
### 1️⃣1️⃣ intersection_update()
```python
a.intersection_update(b)
print(a)   # {3}
```
### 1️⃣2️⃣ difference_update()
```python
a = {1,2,3}
a.difference_update({2})
print(a)   # {1,3}
```
### 1️⃣3️⃣ symmetric_difference_update()
```python
a = {1,2,3}
a.symmetric_difference_update({3,4})
print(a)   # {1,2,4}
```

📌 Difference:

union() → new set

update() → same set modify

## 🟣 Check Relationships
### 1️⃣4️⃣ issubset()
```python
a = {1,2}
b = {1,2,3}
print(a.issubset(b))   # True

# 1️⃣5️⃣ issuperset()
print(b.issuperset(a))   # True

# 1️⃣6️⃣ isdisjoint()

➡ Common element nahi hona chahiye

a = {1,2}
b = {3,4}
print(a.isdisjoint(b))   # True
```
### 🔶 Built-in Functions with Sets
## 🔹 Information / Calculation
```python
s = {1, 2, 3}

- (s)   # 3
- min(s)   # 1
- max(s)   # 3
- sum(s)   # 6
```
## 🔹 Type & Conversion
- set([1,2,2,3])     # {1,2,3}
- list(s)            # [1,2,3]
- tuple(s)           # (1,2,3)
- sorted(s)          # [1,2,3]


📌 sorted() list return karta hai

## 🔹 Checking
- all()

➡ Sab True ho to True

    - all({1,2,3})   # True
    - all({0,1})     # False

- any()

➡ Ek bhi True ho to True

    any({0,0,1})   # True

## Membership
```python
s = {1,2,3}
print(2 in s)       # True
print(5 not in s)   # True
```
