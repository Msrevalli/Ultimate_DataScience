### **Module 1 / Section 1 - Python Foundations**  
#### **Concepts Covered:**
This section introduces Python and its fundamental concepts. Below is a breakdown of the core topics:

---

### **1. Introduction to Python**
Python is a high-level, interpreted programming language known for its readability and versatility. It supports multiple programming paradigms, including:
- Procedural
- Object-Oriented
- Functional

**Comparison with other languages:**
- **Python vs. C++:** Python is dynamically typed, whereas C++ is statically typed.
- **Python vs. Java:** Python uses indentation for code blocks, while Java uses braces `{}`.
- **Python vs. JavaScript:** Python is used for backend, whereas JavaScript is mostly for web development.

---

### **2. Python Objects: Numbers, Booleans, and Strings**
Python treats everything as an object. Here are fundamental object types:

1. **Numbers:**  
   - Integers (`int`): `x = 10`
   - Floating Point (`float`): `y = 3.14`
   - Complex Numbers (`complex`): `z = 3 + 4j`

2. **Booleans:**  
   - Represents `True` or `False`
   - Example: `x = (5 > 3) → True`

3. **Strings:**  
   - Strings are immutable sequences of Unicode characters.
   - Example: `s = "Hello, World!"`
   - Access characters using indexing: `s[0]` → `'H'`
   - Slicing: `s[0:5]` → `'Hello'`

---

### **3. Data Structures & Operations**
Python provides built-in data structures:

1. **Lists (`list`)**: Ordered, mutable collections.  
   ```python
   my_list = [1, 2, 3, "apple", 3.14]
   my_list.append("banana")   # Add element
   my_list.pop(2)             # Remove element at index 2
   ```

2. **Tuples (`tuple`)**: Ordered, immutable collections.  
   ```python
   my_tuple = (10, 20, 30)
   ```

3. **Sets (`set`)**: Unordered, unique elements.  
   ```python
   my_set = {1, 2, 3, 4, 5}
   my_set.add(6)
   ```

4. **Dictionaries (`dict`)**: Key-value pairs.  
   ```python
   my_dict = {"name": "John", "age": 25}
   print(my_dict["name"])  # Output: John
   ```

---

### **4. Operators & Operator Precedence**
Python supports various operators:

1. **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`, `//`, `**`
2. **Comparison Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
3. **Logical Operators**: `and`, `or`, `not`
4. **Bitwise Operators**: `&`, `|`, `^`, `<<`, `>>`
5. **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `//=`
6. **Membership Operators**: `in`, `not in`
7. **Identity Operators**: `is`, `is not`

**Example:**
```python
x = 10
y = 3
print(x ** y)  # Output: 1000 (10^3)
print(10 // 3) # Output: 3 (integer division)
```

---

### **5. Control Flow: Conditionals & Loops**
Python allows controlling the flow of execution using conditionals and loops.

#### **Conditional Statements**
```python
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is exactly 5")
else:
    print("x is less than 5")
```

#### **Loops**
1. **For Loop**
   ```python
   for i in range(1, 6):
       print(i)
   ```
2. **While Loop**
   ```python
   x = 5
   while x > 0:
       print(x)
       x -= 1
   ```
3. **Break & Continue**
   ```python
   for num in range(1, 10):
       if num == 5:
           break  # Exits the loop
       print(num)
   ```

---

### **6. String Manipulation**
Strings in Python support multiple built-in methods.

**String Methods:**
```python
s = "Python Programming"
print(s.upper())  # 'PYTHON PROGRAMMING'
print(s.lower())  # 'python programming'
print(s.split())  # ['Python', 'Programming']
print(" ".join(["Hello", "World"]))  # 'Hello World'
```

---

### **7. Lists, Collections & Comprehensions**
List comprehensions provide a concise way to create lists.

```python
squares = [x**2 for x in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]
```

---

## **10 Intermediate Python Practice Questions**


### **1. Number Operations**
Write a function to determine whether a given number is **prime**.
```python
def isprime(n):
    for i in range(2,(n//2)+1):
        if n%i==0:
            return False
    return True

isprime(10)
```

### **2. String Manipulation**
Write a function that takes a string as input and returns the string in **reverse order**, preserving spaces.

### **3. List Processing**
Write a function to find **the second largest** number in a given list.

### **4. Dictionary Operations**
Create a Python function that takes a dictionary and returns a new dictionary with **keys and values swapped**.

### **5. Set Operations**
Write a function that returns the intersection, union, and difference between two sets.

### **6. Tuple Manipulation**
Given a list of tuples where each tuple contains a student's name and score, sort the list in **descending order** by score.

```python
students = [("Alice", 85), ("Bob", 78), ("Charlie", 92)]
```

### **7. List Comprehension**
Generate a list of **all numbers from 1 to 100** that are divisible by both 3 and 5.

### **8. Control Flow Challenge**
Write a program to generate the **Fibonacci series up to `n`** using a while loop.

### **9. File Handling**
Write a Python script that reads a file and counts the **occurrences of each word**.

### **10. Nested Loops**
Write a program to print the following pattern:
```
1  
1 2  
1 2 3  
1 2 3 4  
1 2 3 4 5  
```

