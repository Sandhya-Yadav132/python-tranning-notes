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
