## **Module 1 / Section 2 - Data Structures & Operations in Python**  
In this section, we dive deeper into Python's built-in **data structures**, their properties, and operations. Mastering these structures is crucial for efficient programming.

---

## **Concepts Covered**

### **1. Container Objects and Mutability**
Python provides **mutable** and **immutable** container objects.

- **Mutable Objects**: Can be modified after creation. (e.g., `list`, `set`, `dict`)
- **Immutable Objects**: Cannot be changed after creation. (e.g., `tuple`, `str`, `frozenset`)

Example:
```python
# Mutable List
my_list = [1, 2, 3]
my_list[0] = 100  # Allowed

# Immutable Tuple
my_tuple = (1, 2, 3)
# my_tuple[0] = 100  # TypeError
```

---

### **2. Lists: Properties and Operations**
- Lists are **ordered, mutable** collections.
- They support dynamic resizing.

#### **Common List Methods:**
```python
numbers = [10, 20, 30, 40]

numbers.append(50)    # Adds 50 to the list
numbers.insert(2, 25) # Inserts 25 at index 2
numbers.pop()         # Removes last element
numbers.remove(20)    # Removes first occurrence of 20
numbers.reverse()     # Reverses the list
numbers.sort()        # Sorts the list in ascending order
```

---

### **3. Tuples: Properties and Operations**
- Tuples are **ordered, immutable** collections.
- Faster than lists because they are stored in a **single memory block**.

Example:
```python
my_tuple = (1, 2, 3, 4)
print(my_tuple[1])   # Accessing element at index 1
print(len(my_tuple)) # Length of the tuple
```

**Tuple Packing & Unpacking**
```python
a, b, c = (10, 20, 30)
print(a, b, c)  # Output: 10 20 30
```

---

### **4. Sets: Properties and Operations**
- Sets are **unordered, mutable, and store unique elements**.
- Fast **membership checking** (`O(1)` time complexity).

```python
s = {1, 2, 3, 4, 5}
s.add(6)          # Add an element
s.remove(2)       # Remove an element
s.update([7, 8])  # Add multiple elements
print(s)
```

**Set Operations:**
```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

print(A | B)  # Union: {1, 2, 3, 4, 5, 6}
print(A & B)  # Intersection: {3, 4}
print(A - B)  # Difference: {1, 2}
print(A ^ B)  # Symmetric Difference: {1, 2, 5, 6}
```

---

### **5. Dictionaries: Properties and Operations**
- **Key-Value pairs** (`dict`) for fast lookups (`O(1)` complexity).
- **Keys must be unique and immutable** (strings, numbers, tuples).

```python
student = {"name": "Alice", "age": 25, "grade": "A"}
print(student["name"])    # Access value using key
student["age"] = 26       # Modify value
student["subject"] = "Math"  # Add a new key-value pair
del student["grade"]       # Remove key-value pair
```

**Dictionary Methods:**
```python
print(student.keys())    # Get all keys
print(student.values())  # Get all values
print(student.items())   # Get key-value pairs
print(student.get("age")) # Get value safely (avoids KeyError)
```

**Dictionary Comprehension:**
```python
squares = {x: x**2 for x in range(1, 6)}
print(squares)  # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

---

### **6. Operator Precedence & Associativity**
Operator precedence determines the order in which expressions are evaluated.

**Example Order of Operations:**
1. **Parentheses `()`**
2. **Exponents `**`**
3. **Multiplication/Division `* / % //`**
4. **Addition/Subtraction `+ -`**
5. **Comparison Operators `== != > < >= <=`**
6. **Logical Operators `not`, `and`, `or`**

```python
x = 5 + 3 * 2  # Output: 11 (Multiplication before Addition)
y = (5 + 3) * 2  # Output: 16 (Parentheses first)
```

---

## **10 Intermediate Python Practice Questions**
Test your knowledge by solving these challenges!

### **1. List Processing**
Write a function that finds the **largest contiguous subarray sum** in a given list.
```python
arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
# Output: 6  (Subarray: [4, -1, 2, 1])
```

---

### **2. Tuple Operations**
Write a function that **merges two sorted tuples** into a single sorted tuple.
```python
t1 = (1, 4, 6)
t2 = (2, 3, 5)
# Output: (1, 2, 3, 4, 5, 6)
```

---

### **3. Set Operations**
Given two sets, find **elements present in one but not in both**.

```python
A = {1, 3, 5, 7}
B = {3, 7, 9, 11}
# Output: {1, 5, 9, 11}
```

---

### **4. Dictionary Filtering**
Write a function that removes all key-value pairs where the **value is less than 50**.
```python
data = {"a": 45, "b": 60, "c": 30, "d": 75}
# Output: {"b": 60, "d": 75}
```

---

### **5. Dictionary Merging**
Write a function to **merge two dictionaries**, summing values for common keys.

```python
dict1 = {'a': 10, 'b': 20}
dict2 = {'b': 30, 'c': 40}
# Output: {'a': 10, 'b': 50, 'c': 40}
```

---

### **6. Reverse Words in a String**
Write a function to reverse words in a sentence **without reversing individual words**.
```python
s = "Python is fun"
# Output: "fun is Python"
```

---

### **7. Set Intersection Without Using '&'**
Write a function that finds the **intersection of two sets** without using `&` operator.
```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
# Output: {3, 4}
```

---

### **8. Nested Dictionary Sorting**
Given a dictionary where values are dictionaries, **sort by an inner dictionary value**.

```python
students = {
    "Alice": {"age": 25, "grade": 85},
    "Bob": {"age": 22, "grade": 92},
    "Charlie": {"age": 23, "grade": 88}
}
# Sort by 'grade' in descending order
```

---

### **9. Unique Values in a Dictionary**
Write a function that extracts **all unique values** from a dictionary.

```python
d = {"A": [1, 2, 3], "B": [2, 3, 4], "C": [4, 5, 6]}
# Output: {1, 2, 3, 4, 5, 6}
```

---

### **10. Matrix Transposition**
Write a function to **transpose a matrix** (convert rows to columns).

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
# Output: [[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```

---

