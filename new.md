Sure! Here's a **clear and beginner-friendly explanation** of Python basics with **examples**:

---

### 🧠 **1. Data Types and Variables**

Variables are like containers that store data.

#### Common Data Types:

| Data Type | Description                 | Example                |
|-----------|-----------------------------|------------------------|
| `int`     | Integer (whole number)      | `x = 10`               |
| `float`   | Decimal number              | `pi = 3.14`            |
| `str`     | Text (string)               | `name = "Valli"`       |
| `bool`    | Boolean (True/False)        | `is_active = True`     |
| `list`    | Ordered, changeable items   | `fruits = ["apple", "banana"]` |
| `tuple`   | Ordered, unchangeable items | `point = (4, 5)`       |
| `dict`    | Key-value pairs             | `person = {"name": "Valli", "age": 25}` |
| `set`     | Unordered, unique items     | `colors = {"red", "blue"}` |

---

### ➕ **2. Operators**

#### a) **Arithmetic Operators**
Used for basic math operations:
```python
a = 10
b = 3
print(a + b)  # 13
print(a - b)  # 7
print(a * b)  # 30
print(a / b)  # 3.33...
print(a // b) # 3 (floor division)
print(a % b)  # 1 (modulo)
print(a ** b) # 1000 (exponent)
```

#### b) **Logical Operators**
Used to combine conditional statements:
```python
x = 5
print(x > 3 and x < 10)  # True
print(x < 3 or x > 2)    # True
print(not(x > 3))        # False
```

#### c) **Comparison Operators**
```python
a = 5
b = 7
print(a == b)  # False
print(a != b)  # True
print(a > b)   # False
```

#### d) **Membership Operators**
```python
colors = ["red", "green"]
print("red" in colors)      # True
print("blue" not in colors) # True
```

---

### 🖨️ **3. Basic Input and Output**

#### `print()` – to display output
```python
print("Hello, World!")
```

#### `input()` – to take user input
```python
name = input("Enter your name: ")
print("Hi", name)
```

---

### 📝 **4. Comments and Code Readability**

#### Single-line comment:
```python
# This is a comment
```

#### Multi-line comment:
```python
"""
This is a
multi-line comment
"""
```

💡 **Tip**: Use comments to explain complex logic. It improves readability.

---

### ⬇️ **5. Indentation and Code Structure**

Python uses **indentation (spaces or tabs)** to define code blocks.

Correct:
```python
if True:
    print("Yes")
```

Incorrect (will cause an error):
```python
if True:
print("Yes")  # IndentationError
```

---

### 🔁 **6. Control Flow**

Control flow allows you to control **which code runs and when**.

#### a) **Conditional Statements**
```python
age = 20

if age < 18:
    print("Minor")
elif age < 60:
    print("Adult")
else:
    print("Senior")
```

#### b) **Loops**

**for loop** – used for iterating over a sequence:
```python
for i in range(5):
    print(i)
# Output: 0 1 2 3 4
```

**while loop** – runs as long as condition is True:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

---

### ⏹️ **7. Loop Control**

#### `break` – exit the loop
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

#### `continue` – skip the current iteration
```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

#### `pass` – do nothing (used as placeholder)
```python
for i in range(3):
    pass  # Placeholder for future code
```

---

Let me know if you want practice questions or a mini project using these concepts!

Absolutely! Using **lists** and **dictionaries** together is super powerful in Python. Here are some **common and useful examples** to help you understand:

---

### ✅ **Example 1: List of Dictionaries**

Used to store multiple "objects" (like students, employees, etc.).

```python
students = [
    {"name": "Alice", "age": 20, "marks": 85},
    {"name": "Bob", "age": 22, "marks": 90},
    {"name": "Charlie", "age": 21, "marks": 78}
]

# Print each student's name and marks
for student in students:
    print(f"{student['name']} scored {student['marks']} marks")
```

**Output:**
```
Alice scored 85 marks
Bob scored 90 marks
Charlie scored 78 marks
```

---

### ✅ **Example 2: Dictionary with Lists as Values**

Great for storing grouped data.

```python
class_subjects = {
    "Class A": ["Math", "Science", "English"],
    "Class B": ["History", "Geography", "Civics"]
}

# Print subjects for Class A
for subject in class_subjects["Class A"]:
    print(subject)
```

**Output:**
```
Math
Science
English
```

---

### ✅ **Example 3: Nested Access (List inside Dict inside List)**

```python
data = [
    {"id": 1, "details": {"name": "Ravi", "skills": ["Python", "SQL"]}},
    {"id": 2, "details": {"name": "Priya", "skills": ["Java", "C++"]}},
]

# Print all user skills
for person in data:
    print(f"{person['details']['name']} knows {', '.join(person['details']['skills'])}")
```

**Output:**
```
Ravi knows Python, SQL
Priya knows Java, C++
```

---

### ✅ **Example 4: Counting Items using a Dictionary from a List**

```python
fruits = ["apple", "banana", "apple", "orange", "banana", "apple"]
count = {}

for fruit in fruits:
    if fruit in count:
        count[fruit] += 1
    else:
        count[fruit] = 1

print(count)
```

**Output:**
```python
{'apple': 3, 'banana': 2, 'orange': 1}
```

---

Want me to show how to **add or remove elements** from these combos too?

Great question! Combining **lists** and **dictionaries** is super common in real-world Python programs. Here are some practical, real-world **use cases**:

---

### 🧾 1. **Employee/Student Management Systems**
- **Use Case**: Store and manage records of employees or students.
- **Structure**: List of dictionaries (each dict is a record)

```python
employees = [
    {"id": 1, "name": "Valli", "role": "Developer"},
    {"id": 2, "name": "Ravi", "role": "Designer"},
]

# Find all developers
for emp in employees:
    if emp["role"] == "Developer":
        print(emp["name"])
```

---

### 🛒 2. **E-commerce Product Catalog**
- **Use Case**: Store product details like price, category, stock
- **Structure**: List of product dictionaries

```python
products = [
    {"name": "Laptop", "price": 50000, "in_stock": True},
    {"name": "Phone", "price": 30000, "in_stock": False},
]

# Show only in-stock items
for product in products:
    if product["in_stock"]:
        print(product["name"])
```

---

### 🚌 3. **Transport Schedule / Booking System**
- **Use Case**: Store train/bus schedule info
- **Structure**: List of trips, each as a dictionary

```python
buses = [
    {"route": "Bangalore to Chennai", "departure": "10:00 AM"},
    {"route": "Hyderabad to Bangalore", "departure": "4:00 PM"},
]
```

---

### 📊 4. **Survey/Feedback Data**
- **Use Case**: Store responses from users
- **Structure**: List of dicts (each response)

```python
feedback = [
    {"user": "Asha", "rating": 4, "comment": "Good service"},
    {"user": "Manoj", "rating": 5, "comment": "Excellent"},
]
```

---

### 📚 5. **Library or Bookstore System**
- **Use Case**: Manage book inventory
- **Structure**: List of books (as dictionaries)

```python
books = [
    {"title": "Python Basics", "author": "John", "available": True},
    {"title": "Data Science 101", "author": "Jane", "available": False},
]
```

---

### 🧠 6. **Machine Learning Dataset (like JSON)**  
- **Use Case**: Store dataset rows in memory before training
- **Structure**: Each row is a dictionary, entire dataset is a list

```python
dataset = [
    {"features": [1.2, 3.4], "label": 0},
    {"features": [5.6, 7.8], "label": 1},
]
```

---

### 🗃️ 7. **API Response (JSON Parsing)**  
- **Use Case**: Working with data from web APIs
- **Structure**: JSON responses are just nested dicts/lists!

```python
response = {
    "status": "success",
    "data": [
        {"id": 101, "name": "Alice"},
        {"id": 102, "name": "Bob"},
    ]
}
```

---

Want help building a small **project** with lists + dictionaries? Like a **mini app** for students or products?

Great follow-up! Managing data in `lists` and `dictionaries` can get messy if not done right, especially as your project grows. Here are some **best practices** to keep your code clean, efficient, and bug-free:

---

## ✅ Best Practices for Lists & Dictionaries in Python

---

### 1. **Choose the Right Data Structure**

- Use a **list** when:
  - Order matters (e.g., queue of tasks).
  - You need to iterate over items.
  
- Use a **dictionary** when:
  - You need fast lookup by a key (e.g., student ID, username).
  - Each item has multiple properties (like a record).

🧠 **Tip**: Combine them smartly:  
```python
students = [{"id": 1, "name": "Valli"}, {"id": 2, "name": "Ravi"}]
```

---

### 2. **Use Meaningful Keys and Variable Names**

```python
# Bad
x = [{"n": "Valli", "a": 25}]

# Good
students = [{"name": "Valli", "age": 25}]
```

---

### 3. **Avoid Hardcoding Indexes or Keys**

```python
# ❌ Not safe
print(students[0]["name"])  # Can crash if list is empty

# ✅ Better
if students:
    print(students[0].get("name", "Unknown"))
```

---

### 4. **Use `.get()` for Safe Dictionary Access**

```python
person = {"name": "Asha"}

# ❌ This crashes if 'age' doesn't exist
# print(person["age"])

# ✅ Safer
print(person.get("age", "Not specified"))
```

---

### 5. **Use `enumerate()` for Index in Loops**

```python
for idx, student in enumerate(students):
    print(f"{idx + 1}. {student['name']}")
```

---

### 6. **Use List Comprehensions**

Cleaner and faster way to filter or transform data:
```python
# Get all names
names = [student["name"] for student in students]
```

---

### 7. **Check for Duplicates Before Adding to List or Set**

```python
emails = set()
new_email = "valli@example.com"

if new_email not in emails:
    emails.add(new_email)
```

---

### 8. **Use DefaultDict or Counter (from `collections`) for Counting**

```python
from collections import Counter

fruits = ["apple", "banana", "apple"]
count = Counter(fruits)
print(count["apple"])  # 2
```

---

### 9. **Sort List of Dicts**

```python
# Sort by age
students.sort(key=lambda x: x["age"])
```

---

### 10. **Keep Data Normalized**

Try to keep consistent keys and formats throughout.

```python
# Consistent keys
data = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
]
```

---

### Bonus: 🧪 **Validate Data Before Using It**

Especially when dealing with user input or API data:
```python
if isinstance(person, dict) and "name" in person:
    print(person["name"])
```

---

Would you like a checklist or cheat sheet PDF of these best practices? Or a mini-project where we apply them?

Excellent question! 🙌  
**Exceptions** are runtime errors that can crash your program if not handled properly — especially when dealing with lists and dictionaries where **missing keys**, **out-of-range indexes**, or **wrong data types** are common.

Let’s break down **how to handle exceptions effectively** with practical examples:

---

## ⚠️ Common Exceptions with Lists and Dictionaries

| Error Type                | When It Happens                              |
|---------------------------|----------------------------------------------|
| `KeyError`               | Accessing a missing key in a dictionary      |
| `IndexError`             | Accessing an invalid index in a list         |
| `TypeError`              | Using wrong data type (e.g., indexing a `None`) |
| `ValueError`             | Wrong value passed to a function (like `int("abc")`) |

---

## ✅ Best Practices for Exception Handling

---

### 1. **Use `try-except` Block**

#### Example 1: Handling `KeyError` in a Dictionary
```python
student = {"name": "Valli"}

try:
    print(student["age"])
except KeyError:
    print("Key 'age' not found!")
```

---

#### Example 2: Handling `IndexError` in a List
```python
students = ["Alice", "Bob"]

try:
    print(students[5])
except IndexError:
    print("That student index doesn't exist.")
```

---

### 2. **Use `.get()` for Safe Dictionary Access**

```python
student = {"name": "Valli"}
print(student.get("age", "Age not provided"))
```

---

### 3. **Use `in` to Check Key or Index Exists**

#### Check key in dictionary:
```python
if "age" in student:
    print(student["age"])
```

#### Check index in list:
```python
index = 3
if index < len(students):
    print(students[index])
else:
    print("Index out of range")
```

---

### 4. **Catch Multiple Exceptions**

```python
data = {"scores": [95, 87]}

try:
    print(data["scores"][5])  # May raise IndexError
except KeyError:
    print("Missing 'scores' key")
except IndexError:
    print("Index in 'scores' list is out of range")
```

---

### 5. **Catch All Exceptions (Use with Caution)**

This is a **last resort** – use when you don’t know what could fail.

```python
try:
    # Some risky operation
    print(student["marks"][0])
except Exception as e:
    print("An error occurred:", str(e))
```

---

### 6. **Use `finally` to Clean Up (Optional)**

```python
try:
    print("Trying something...")
except:
    print("Handled error")
finally:
    print("This will always run")
```

---

### 🎯 Summary – Safe Access Checklist

| Goal                           | Recommended Approach         |
|--------------------------------|------------------------------|
| Safe key access in dict        | `dict.get("key", default)`   |
| Check if key exists            | `"key" in dict`              |
| Prevent list out-of-bounds     | `if i < len(list):`          |
| Use try-except                 | For unpredictable data       |
| Catch multiple errors          | `except KeyError`, etc.      |

---

Want me to give you a **real-world mini script** with exception handling? Like a student search, product lookup, or feedback manager?

Great question! 🎯  
**Decorators** are super powerful in Python and are used when you want to **add extra behavior** to a function **without changing its actual code**. Here are some **practical, real-world scenarios** where decorators shine:

---

## ✅ **1. Logging Function Calls**

Track when a function is called – useful for debugging and monitoring.

```python
def log_calls(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args} {kwargs}")
        return func(*args, **kwargs)
    return wrapper

@log_calls
def greet(name):
    print(f"Hello, {name}!")

greet("Valli")
```

🧠 **Use case**: Track how often a function is called, with what arguments.

---

## ✅ **2. Access Control / Authentication**

Control access to sensitive functions.

```python
def requires_login(func):
    def wrapper(user):
        if user.get("logged_in"):
            return func(user)
        else:
            print("Access denied. Please log in.")
    return wrapper

@requires_login
def view_dashboard(user):
    print(f"Welcome {user['name']} to your dashboard!")

user = {"name": "Valli", "logged_in": True}
view_dashboard(user)
```

🧠 **Use case**: Web apps or APIs where you need to check permissions.

---

## ✅ **3. Caching / Memoization**

Store results of expensive function calls to reuse later.

```python
from functools import lru_cache

@lru_cache(maxsize=1000)
def fib(n):
    if n < 2:
        return n
    return fib(n-1) + fib(n-2)

print(fib(35))  # Much faster with caching
```

🧠 **Use case**: Dynamic programming, recursive algorithms, API calls.

---

## ✅ **4. Timing Function Execution**

Measure how long a function takes to run.

```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(2)
    print("Done!")

slow_function()
```

🧠 **Use case**: Performance testing, benchmarking.

---

## ✅ **5. Validation & Sanitization**

Check or modify arguments before the function runs.

```python
def validate_positive(func):
    def wrapper(x):
        if x < 0:
            raise ValueError("Number must be positive!")
        return func(x)
    return wrapper

@validate_positive
def square_root(x):
    return x ** 0.5

print(square_root(25))
```

🧠 **Use case**: Data validation in APIs or form submissions.

---

## ✅ **6. Retry Logic (in case of failure)**

Retry failed functions (like API calls).

```python
import random

def retry(func):
    def wrapper():
        for i in range(3):
            try:
                return func()
            except Exception as e:
                print(f"Attempt {i+1} failed: {e}")
    return wrapper

@retry
def flaky_function():
    if random.choice([True, False]):
        raise Exception("Failed!")
    print("Success!")

flaky_function()
```

🧠 **Use case**: Network requests, flaky operations.

---

## TL;DR – **Use Decorators When You Want To**:

| Purpose             | Example                |
|---------------------|------------------------|
| Logging             | Track usage of a function |
| Access control      | Check login/auth        |
| Performance timing  | Benchmark code          |
| Validation          | Ensure correct input    |
| Retry logic         | Retry on failure        |
| Caching             | Speed up computations   |

---

Want help writing your **own custom decorator** for a specific use case?

Awesome question! 🌟  
**Chaining decorators** means stacking multiple decorators on a single function — each decorator adds its own layer of behavior.

Think of it like **wrapping a gift with multiple layers** — each decorator wraps the function and can modify inputs, outputs, or side effects.

---

## 🧩 Syntax: Stacking Decorators

```python
@decorator1
@decorator2
def my_function():
    pass
```

This is equivalent to:

```python
my_function = decorator1(decorator2(my_function))
```

---

## ✅ Example: Chaining `logging` and `timer` Decorators

### Step 1: Create the decorators

```python
import time

def log_call(func):
    def wrapper(*args, **kwargs):
        print(f"[LOG] Calling: {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"[TIMER] {func.__name__} took {end - start:.4f}s")
        return result
    return wrapper
```

---

### Step 2: Apply both decorators (stack them)

```python
@log_call
@timer
def say_hello():
    time.sleep(1)
    print("Hello!")

say_hello()
```

---

### 🔍 Output:

```
[LOG] Calling: wrapper  <-- from log_call (outermost)
[TIMER] say_hello took 1.0001s  <-- from timer (inner)
Hello!
```

🧠 **Note**: The **outermost decorator runs first** and wraps the inner ones.

---

## 🤹‍♀️ Practical Use Case: Auth + Logging + Timing

```python
def require_login(func):
    def wrapper(user, *args, **kwargs):
        if not user.get("logged_in"):
            return "Unauthorized"
        return func(user, *args, **kwargs)
    return wrapper

@log_call
@timer
@require_login
def view_profile(user):
    time.sleep(0.5)
    return f"Welcome, {user['name']}!"

user = {"name": "Valli", "logged_in": True}
print(view_profile(user))
```

---

## 🔧 Tips for Chaining Decorators

- Use `functools.wraps(func)` to preserve metadata (`__name__`, docstring).
- Stack in **logical order**:
  - Outer layers: Logging, error handling.
  - Inner layers: Access control, transformation.

---

## 🎁 Bonus: A Custom Use Case for You?

Would you like a **realistic mini project** using chained decorators? (e.g. A login-protected dashboard with logging and timing?)  
Just say the word and I’ll code it up for you 😄
Absolutely! 💡  
Chaining decorators can be **clean, powerful**, and **modular** — but to do it **effectively**, you should follow some best practices to keep your code readable, debuggable, and maintainable.

---

## ✅ Best Practices for Chaining Decorators

---

### 1. **Use `functools.wraps()` to Preserve Metadata**

Without it, the original function's name and docstring are lost.

```python
from functools import wraps

def logger(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print(f"[LOG] Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper
```

🔍 Why? This keeps things like `help(func)` and `func.__name__` correct.

---

### 2. **Order Matters – Outer Decorator Wraps Inner**

Stack decorators in **logical order of execution**:

```python
@logger        # Outer
@authenticate  # Inner
def get_data(user):
    ...
```

This means `authenticate` runs **before** `logger`.

📌 **Tip**: Access control usually goes **inner**, logging and timing go **outer**.

---

### 3. **Keep Decorators Small and Focused**

Each decorator should do **one thing well**. Don’t mix logging + timing + access in one.

```python
def timer(func): ...
def logger(func): ...
def authenticate(func): ...
```

🧠 This promotes **reuse and testability**.

---

### 4. **Use Arguments in Decorators with Decorator Factories**

When you need parameters in a decorator (like `@retry(times=3)`), use **nested functions**:

```python
def retry(times):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            for i in range(times):
                try:
                    return func(*args, **kwargs)
                except Exception as e:
                    print(f"Retry {i+1}/{times}: {e}")
        return wrapper
    return decorator
```

✅ Usage:

```python
@retry(times=3)
def flaky_function():
    ...
```

---

### 5. **Log and Handle Exceptions Cleanly**

Use decorators to centralize exception handling.

```python
def catch_errors(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        try:
            return func(*args, **kwargs)
        except Exception as e:
            print(f"[ERROR] {func.__name__}: {e}")
    return wrapper
```

---

### 6. **Chain Decorators in a Clear, Consistent Order**

Recommended logical order:

1. **Input validation / authentication**
2. **Caching / memoization**
3. **Timing / logging**
4. **Error handling**

```python
@catch_errors
@logger
@timer
@authenticate
def process_payment(user):
    ...
```

---

### 7. **Use Decorators to Avoid Repetitive Code**

Example: You don’t need to wrap every function with logging or error handling manually — just decorate them.

---

## 🎯 Example: Full Best-Practices Decorator Chain

```python
from functools import wraps
import time

def authenticate(func):
    @wraps(func)
    def wrapper(user, *args, **kwargs):
        if not user.get("logged_in"):
            print("Unauthorized access")
            return None
        return func(user, *args, **kwargs)
    return wrapper

def logger(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print(f"[LOG] Function: {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

def timer(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"[TIMER] {func.__name__} ran in {end - start:.4f}s")
        return result
    return wrapper

@logger
@timer
@authenticate
def show_profile(user):
    print(f"Welcome {user['name']}!")

user = {"name": "Valli", "logged_in": True}
show_profile(user)
```

---

## 👌 Summary of Best Practices

| Best Practice                     | Why It Matters                                |
|----------------------------------|------------------------------------------------|
| Use `@wraps`                     | Preserves metadata                             |
| Order decorators logically       | Controls flow of logic                         |
| Keep each decorator single-purpose | Easier to reuse and debug                    |
| Use decorator factories          | Enables passing arguments                      |
| Centralize error handling        | Cleaner and more consistent code              |
| Chain for clarity                | Encourages DRY and modular code                |

---

Would you like a **reusable decorator library template** you can plug into your projects?

Absolutely! ✅  
**Testing decorators** is super important — especially when you want to ensure they work independently, don’t interfere with the function logic, and behave well when chained.

Let’s walk through this with practical, clean examples 🚀

---

## 🎯 **1. Test a Simple Decorator in Isolation**

Let’s test a logging decorator:

### 🔧 Decorator Code
```python
from functools import wraps

def logger(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print(f"[LOG] Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper
```

### ✅ Function with Decorator
```python
@logger
def greet(name):
    return f"Hello, {name}!"
```

### 🧪 Unit Test (with `unittest`)
```python
import unittest
from io import StringIO
import sys

class TestLoggerDecorator(unittest.TestCase):
    def test_logger_output(self):
        captured_output = StringIO()
        sys.stdout = captured_output  # Redirect stdout

        result = greet("Valli")

        sys.stdout = sys.__stdout__  # Reset redirect

        self.assertIn("[LOG] Calling greet", captured_output.getvalue())
        self.assertEqual(result, "Hello, Valli")

if __name__ == '__main__':
    unittest.main()
```

---

## 🎯 **2. Test a Decorator with Side Effects (e.g., access control)**

### 🔧 Decorator
```python
def require_login(func):
    @wraps(func)
    def wrapper(user, *args, **kwargs):
        if not user.get("logged_in"):
            return "Unauthorized"
        return func(user, *args, **kwargs)
    return wrapper
```

### ✅ Function
```python
@require_login
def dashboard(user):
    return f"Welcome {user['name']}!"
```

### 🧪 Test
```python
class TestRequireLogin(unittest.TestCase):
    def test_access_granted(self):
        user = {"name": "Valli", "logged_in": True}
        self.assertEqual(dashboard(user), "Welcome Valli!")

    def test_access_denied(self):
        user = {"name": "Valli", "logged_in": False}
        self.assertEqual(dashboard(user), "Unauthorized")
```

---

## 🎯 **3. Test Chained Decorators**

Suppose we chain `@logger` + `@require_login`:

```python
@logger
@require_login
def view_profile(user):
    return f"{user['name']}'s Profile"
```

You can test both behaviors together or mock one.

---

## ✅ Best Practices for Testing Decorators

| Tip | Why it Helps |
|-----|--------------|
| Use `unittest` or `pytest` | Standard testing frameworks make assertions easy |
| Test the function **with and without** the decorator | Ensure decorator behavior is isolated |
| Mock dependencies if needed | Like time, I/O, or DB |
| Test both **expected behavior** and **edge cases** | e.g., unauthorized user, error in wrapped function |
| Always preserve function metadata with `@wraps` | Makes your decorator test-friendly |

---

## 🧪 Bonus: Testing a Decorator Factory (e.g., `@retry(times=3)`)

```python
def retry(times):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            for _ in range(times):
                try:
                    return func(*args, **kwargs)
                except Exception:
                    continue
            return "Failed after retries"
        return wrapper
    return decorator
```

### ✅ Test
```python
@retry(times=3)
def fail_once():
    if not hasattr(fail_once, 'called'):
        fail_once.called = True
        raise ValueError("First try fails")
    return "Success"

class TestRetry(unittest.TestCase):
    def test_retry_success(self):
        result = fail_once()
        self.assertEqual(result, "Success")
```

---

Would you like a `pytest` version or a GitHub-ready test suite example? Happy to share! 😄

Absolutely! Let's break this down **clearly** with **simple examples** so you can understand and use each concept confidently. 💡

---

## 📦 **Data Structures**

---

### 🔹 **1. Lists** – *Ordered, Mutable Collections*

```python
# Creating a list
fruits = ["apple", "banana", "cherry"]

# Accessing elements
print(fruits[0])         # 'apple'
print(fruits[-1])        # 'cherry'

# Modifying a list
fruits.append("orange")
fruits[1] = "blueberry"
print(fruits)            # ['apple', 'blueberry', 'cherry', 'orange']
```

✅ Use when order matters and you may change elements.

---

### 🔹 **2. Tuples** – *Ordered, Immutable Collections*

```python
# Creating a tuple
dimensions = (1920, 1080)

# Accessing elements
print(dimensions[0])     # 1920

# Tuples cannot be modified
# dimensions[0] = 1280  ❌ will raise TypeError
```

✅ Use when data shouldn't change (e.g., coordinates, config).

---

### 🔹 **3. Dictionaries** – *Key-Value Pairs*

```python
# Creating a dictionary
student = {
    "name": "Valli",
    "age": 22,
    "grade": "A"
}

# Accessing values
print(student["name"])       # Valli
print(student.get("age"))    # 22

# Modifying
student["age"] = 23
student["gender"] = "Female"
print(student)
```

✅ Use when you need to label data.

---

### 🔹 **4. Sets** – *Unordered, Unique Items*

```python
# Creating a set
languages = {"Python", "Java", "Python", "C++"}

print(languages)             # {'Python', 'Java', 'C++'}

# Adding and removing
languages.add("Go")
languages.discard("Java")
print(languages)
```

✅ Use to remove duplicates or test membership quickly.

---

## ⚡ **Data Comprehensions** – *Efficient Data Handling*

### 🔸 List Comprehension
```python
# Squares of numbers from 1 to 5
squares = [x**2 for x in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]
```

### 🔸 Dict Comprehension
```python
# Mapping numbers to their squares
squares_dict = {x: x**2 for x in range(1, 4)}
print(squares_dict)  # {1: 1, 2: 4, 3: 9}
```

### 🔸 Set Comprehension
```python
nums = [1, 2, 2, 3, 4, 4]
unique_squares = {x**2 for x in nums}
print(unique_squares)  # {16, 1, 4, 9}
```

---

## 📚 **Modules and Packages**

---

### 🔹 **Standard Library Modules**

✅ Python comes with batteries included!

#### `math` module
```python
import math

print(math.sqrt(16))      # 4.0
print(math.pi)            # 3.14159...
```

#### `os` module
```python
import os

print(os.getcwd())        # Current working directory
```

#### `sys` module
```python
import sys

print(sys.version)        # Python version info
```

#### `datetime` module
```python
from datetime import datetime

now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

---

### 🔹 **Using Packages and Dependencies**

You can install external packages using `pip`.

```bash
pip install requests
```

```python
import requests

response = requests.get("https://api.github.com")
print(response.status_code)
```

---

### 🔹 **Creating Custom Modules**

1. Create a file called `math_utils.py`:

```python
# math_utils.py
def add(a, b):
    return a + b
```

2. Use it in another file:

```python
from math_utils import add

print(add(3, 5))  # 8
```

---

### 🔹 **Using Virtual Environments**

Helps manage project-specific dependencies.

```bash
# Create virtual environment
python -m venv myenv

# Activate it
# On Windows
myenv\Scripts\activate
# On Mac/Linux
source myenv/bin/activate

# Install packages inside it
pip install pandas
```

✅ Keeps your projects isolated and clean.

---

## ✅ Summary Table

| Feature           | Description                         | Example                     |
|-------------------|-------------------------------------|-----------------------------|
| List              | Ordered, mutable collection         | `fruits = ['a', 'b']`       |
| Tuple             | Ordered, immutable collection       | `t = (1, 2)`                |
| Dictionary        | Key-value mapping                   | `d = {'a': 1}`              |
| Set               | Unordered, unique values            | `s = {1, 2}`                |
| Comprehension     | Efficient collection creation       | `[x*x for x in range(5)]`   |
| Standard Library  | Built-in modules                    | `import math, datetime`     |
| Virtual Env       | Isolated Python envs                | `python -m venv myenv`      |

---

Would you like a **mini project** that uses all of these concepts together? I’d love to put one together for you! 🚀

Absolutely! 🚀 Let's build a **simple Student Gradebook app** that uses:

- ✅ **Lists** (to store multiple students)  
- ✅ **Dictionaries** (to store each student's details)  
- ✅ **Functions** (to organize and reuse logic)

---

## 🎯 Goal: A mini app that can:
- Add a student
- Update grades
- Display all students and their grades

---

### 🧠 Step 1: App Structure

```python
# Global list to store student dictionaries
students = []

def add_student(name, grade):
    student = {"name": name, "grade": grade}
    students.append(student)
    print(f"✅ Added: {name} with grade {grade}")

def update_grade(name, new_grade):
    for student in students:
        if student["name"].lower() == name.lower():
            student["grade"] = new_grade
            print(f"✏️ Updated {name}'s grade to {new_grade}")
            return
    print("❌ Student not found.")

def display_all():
    print("\n📋 Student Gradebook:")
    for student in students:
        print(f"{student['name']} - Grade: {student['grade']}")
    print()
```

---

### 🎮 Step 2: Use It Like an App

```python
# Simulate user interaction
add_student("Alice", "A")
add_student("Bob", "B")
add_student("Charlie", "C")

update_grade("Bob", "A+")

display_all()
```

---

### 🖥 Output:
```
✅ Added: Alice with grade A
✅ Added: Bob with grade B
✅ Added: Charlie with grade C
✏️ Updated Bob's grade to A+

📋 Student Gradebook:
Alice - Grade: A
Bob - Grade: A+
Charlie - Grade: C
```

---

## 🔍 Concepts Used

| Feature         | Usage                                     |
|----------------|--------------------------------------------|
| **List**        | `students = []` – Holds all student records |
| **Dict**        | Each student = `{"name": ..., "grade": ...}` |
| **Function**    | Modular logic – add, update, display         |
| **Loop**        | Iterating to find and update student info   |

---

## 🌟 Want to Extend It?

Let me know if you want to add:
- GPA calculation 🎓
- Search by name 🔍
- Save/load from a file 📁
- Menu-based CLI interface 🖱️

I can help you scale it up!

Absolutely! Let’s clearly walk through **Python File Handling** with real-life examples 🚀  
We'll cover everything from **reading & writing files** to **handling errors**, using **paths**, and even **compressing files**!

---

## 📁 1. File Operations — Opening, Reading, Writing

### 🔹 Open & Write to a File

```python
# 'w' mode = write (creates file if it doesn't exist)
with open("notes.txt", "w") as f:
    f.write("Hello, file!\nThis is a new line.")
```

### 🔹 Read a File

```python
with open("notes.txt", "r") as f:
    content = f.read()
    print(content)
```

📌 `with` automatically closes the file. Safer and cleaner!

---

## 📄 2. File Methods: `read()`, `readline()`, `write()`

```python
# Example file: myfile.txt
# Line 1
# Line 2
# Line 3

with open("myfile.txt", "r") as file:
    print(file.readline())     # Reads one line
    print(file.readline())     # Reads next line

with open("myfile.txt", "r") as file:
    lines = file.readlines()   # Returns a list of all lines
    print(lines)
```

---

## 🛣️ 3. Working with Paths — `pathlib` Module

### ✅ Best way to handle cross-platform paths!

```python
from pathlib import Path

# Define a path
file_path = Path("data") / "info.txt"

# Create folder if it doesn't exist
file_path.parent.mkdir(parents=True, exist_ok=True)

# Write to the file
file_path.write_text("Pathlib is easy!")

# Read the file
print(file_path.read_text())
```

---

## 📦 4. File Compression — Using `zipfile`

```python
import zipfile

# Compress files
with zipfile.ZipFile("archive.zip", "w") as zipf:
    zipf.write("notes.txt")
    zipf.write("myfile.txt")

# Extract
with zipfile.ZipFile("archive.zip", "r") as zipf:
    zipf.extractall("extracted_files")
```

---

## ⚠️ 5. Exception Handling

### 🔸 Understanding Exceptions

Examples of errors:

```python
# FileNotFoundError
open("nonexistent.txt", "r")

# ZeroDivisionError
x = 5 / 0
```

---

### 🔹 `try` / `except`

```python
try:
    with open("not_here.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found!")
```

You can catch multiple exceptions:

```python
try:
    num = int(input("Enter number: "))
    print(10 / num)
except ZeroDivisionError:
    print("Can't divide by zero!")
except ValueError:
    print("Invalid number!")
```

---

### 🧑‍💻 Custom Exceptions

```python
class NegativeNumberError(Exception):
    pass

def square_root(x):
    if x < 0:
        raise NegativeNumberError("Cannot take square root of negative number")
    return x ** 0.5

try:
    print(square_root(-9))
except NegativeNumberError as e:
    print(e)
```

---

### 📋 Error Logging — Using `logging` module

```python
import logging

logging.basicConfig(filename="app.log", level=logging.ERROR)

try:
    x = 1 / 0
except ZeroDivisionError as e:
    logging.error("Error occurred: %s", e)
```

📝 This logs the error to `app.log`.

---

## ✅ Summary Table

| Task                   | Module/Function         | Example                             |
|------------------------|-------------------------|-------------------------------------|
| Read/Write Files       | `open()`, `read()`, `write()` | `with open("file.txt") as f` |
| File Paths             | `pathlib.Path`          | `Path("folder") / "file.txt"`       |
| Compression            | `zipfile`               | `ZipFile("archive.zip", "w")`       |
| Error Handling         | `try/except`            | Catch and handle exceptions         |
| Custom Exceptions      | `class MyError(Exception)` | Raise your own errors          |
| Logging Errors         | `logging`               | `logging.error()`                   |

---

Would you like to build a **mini file organizer app** with this knowledge? 📂 I can show you how!

Awesome! Let’s build a **Simple File Organizer App** that:

📦 **Organizes files by type** (e.g., Images, Documents, Videos)  
📁 Uses:
- **File operations** (move, create folders)
- **Pathlib** for clean, cross-platform paths
- **Exception handling**
- Optional: File logging

---

## 🛠️ Goal:
Take messy files in a folder like this:

```
Downloads/
  - pic.jpg
  - doc.pdf
  - video.mp4
  - script.py
```

📂 And organize them into subfolders:

```
Downloads/
  Images/
    - pic.jpg
  Documents/
    - doc.pdf
  Videos/
    - video.mp4
  Scripts/
    - script.py
```

---

## ✅ Code: File Organizer App

```python
from pathlib import Path
import shutil
import os

# Define file type mapping
FILE_TYPES = {
    "Images": [".jpg", ".jpeg", ".png", ".gif"],
    "Documents": [".pdf", ".docx", ".txt"],
    "Videos": [".mp4", ".mov", ".avi"],
    "Scripts": [".py", ".js", ".java"],
    "Others": []
}

def get_category(extension):
    for category, extensions in FILE_TYPES.items():
        if extension in extensions:
            return category
    return "Others"

def organize_folder(target_folder):
    try:
        folder_path = Path(target_folder)

        if not folder_path.exists():
            print("❌ The specified folder does not exist.")
            return

        for item in folder_path.iterdir():
            if item.is_file():
                ext = item.suffix.lower()
                category = get_category(ext)
                destination_folder = folder_path / category
                destination_folder.mkdir(exist_ok=True)
                shutil.move(str(item), destination_folder / item.name)
                print(f"✅ Moved: {item.name} → {category}/")

        print("\n🎉 Organization complete!")
    
    except Exception as e:
        print(f"⚠️ Error: {e}")

# 🔸 Run the organizer
if __name__ == "__main__":
    folder_to_organize = input("Enter the folder path to organize: ")
    organize_folder(folder_to_organize.strip())
```

---

## 🔍 What This Uses:

| Feature | Use |
|--------|------|
| `pathlib` | Navigating & creating paths |
| `shutil.move()` | Moves files |
| `try/except` | Handles errors safely |
| `.suffix` | Gets file extension |
| `.mkdir(exist_ok=True)` | Makes folders only if not present |

---

## 🧪 Example Run:

```bash
Enter the folder path to organize: Downloads
✅ Moved: pic.jpg → Images/
✅ Moved: doc.pdf → Documents/
✅ Moved: script.py → Scripts/
✅ Moved: video.mp4 → Videos/

🎉 Organization complete!
```

---

## 🚀 Want to Improve It?

Let me know if you want to:
- Add **logging to a file**
- Run it automatically with **schedule**
- Support **nested folders**
- Include a **GUI**

Ready to level it up?


Perfect! Let's enhance the **File Organizer App** by adding **error logging** using Python’s `logging` module. This will keep a record of any issues (like permission errors or failed moves) in a log file.

---

## ✅ Step-by-Step Updates:

### 🔧 1. Import and Set Up Logging
```python
import logging

# Configure logging
logging.basicConfig(
    filename="organizer_errors.log",   # Log file name
    level=logging.ERROR,               # Only log errors and above
    format="%(asctime)s - %(levelname)s - %(message)s"
)
```

---

### 🧠 2. Modify `organize_folder()` to Log Errors

We'll wrap the **file move operation** and **folder creation** in try-except blocks and log any exceptions.

---

## 🧩 Final Code with Logging:

```python
from pathlib import Path
import shutil
import os
import logging

# 📝 Set up logging to a file
logging.basicConfig(
    filename="organizer_errors.log",
    level=logging.ERROR,
    format="%(asctime)s - %(levelname)s - %(message)s"
)

# 📁 File categories
FILE_TYPES = {
    "Images": [".jpg", ".jpeg", ".png", ".gif"],
    "Documents": [".pdf", ".docx", ".txt"],
    "Videos": [".mp4", ".mov", ".avi"],
    "Scripts": [".py", ".js", ".java"],
    "Others": []
}

# 🔍 Determine category based on file extension
def get_category(extension):
    for category, extensions in FILE_TYPES.items():
        if extension in extensions:
            return category
    return "Others"

# 🛠️ Main function to organize files
def organize_folder(target_folder):
    try:
        folder_path = Path(target_folder)

        if not folder_path.exists():
            print("❌ The specified folder does not exist.")
            logging.error(f"Folder not found: {target_folder}")
            return

        for item in folder_path.iterdir():
            if item.is_file():
                try:
                    ext = item.suffix.lower()
                    category = get_category(ext)
                    destination_folder = folder_path / category

                    # Ensure destination folder exists
                    destination_folder.mkdir(exist_ok=True)

                    # Move the file
                    shutil.move(str(item), destination_folder / item.name)
                    print(f"✅ Moved: {item.name} → {category}/")
                
                except Exception as e:
                    print(f"⚠️ Error moving {item.name}")
                    logging.error(f"Failed to move {item.name}: {e}")

        print("\n🎉 Organization complete!")
    
    except Exception as e:
        print("❌ Unexpected error occurred.")
        logging.error(f"Unexpected error: {e}")

# ▶️ Run the app
if __name__ == "__main__":
    folder_to_organize = input("Enter the folder path to organize: ")
    organize_folder(folder_to_organize.strip())
```

---

## 🧪 What Happens Now?

- If an error occurs during **file movement**, it shows a warning and logs the error in `organizer_errors.log`.
- The app continues running even after encountering individual file errors.
- You get better **debugging insight** later!

---

## 🔍 Example Log Entry in `organizer_errors.log`:

```
2025-04-04 16:22:35,002 - ERROR - Failed to move secret.docx: [Errno 13] Permission denied: 'secret.docx'
```

---

Ready to try it out? Let me know if you'd like:
- Timestamped folders
- Deleting empty folders
- Auto-run using Task Scheduler or cron!

Absolutely! Let's break down **Object-Oriented Programming (OOP)** in Python step-by-step with **clear examples**.

---

## 🧱 1. Class Basics (Defining Classes)

A **class** is a blueprint for creating objects (instances).

```python
class Animal:
    def speak(self):
        print("Animal speaks")

# Creating an object
a = Animal()
a.speak()
```

---

## 📦 2. Instance Variables and Methods

Instance variables are tied to a particular object.

```python
class Dog:
    def __init__(self, name):
        self.name = name  # Instance variable

    def bark(self):
        print(f"{self.name} says Woof!")

d = Dog("Buddy")
d.bark()  # Output: Buddy says Woof!
```

---

## 🔧 3. Constructors and Destructors (`__init__`, `__del__`)

### Constructor: Runs when an object is created  
### Destructor: Runs when an object is deleted (or goes out of scope)

```python
class Person:
    def __init__(self, name):
        self.name = name
        print(f"{self.name} has entered.")

    def __del__(self):
        print(f"{self.name} has left.")

p = Person("Alice")
# Output:
# Alice has entered.
# (On object deletion: Alice has left.)
```

---

## 👨‍👧 4. Inheritance and Polymorphism

### 🔹 Inheritance: One class (child) can inherit from another (parent)

```python
class Vehicle:
    def move(self):
        print("Moving...")

class Car(Vehicle):
    def move(self):
        print("Car is driving.")  # Overriding (Polymorphism)

v = Vehicle()
v.move()

c = Car()
c.move()
```

🔁 **Polymorphism** allows the same method name to behave differently based on the object.

---

## 🔐 5. Encapsulation and Abstraction

### ✅ Encapsulation: Hides internal state using private variables  
### ✅ Abstraction: Hides complexity and shows only essential features

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

acc = BankAccount(1000)
acc.deposit(500)
print(acc.get_balance())  # Output: 1500
```

---

## 🧙‍♂️ 6. Magic Methods (Dunder Methods)

Used to define how objects behave with built-in functions.

```python
class Book:
    def __init__(self, title):
        self.title = title

    def __str__(self):
        return f"Book: {self.title}"

    def __len__(self):
        return len(self.title)

b = Book("Python 101")
print(b)        # Book: Python 101
print(len(b))   # 11
```

---

## 🔧 7. Abstract Base Classes (ABC)

Force subclasses to implement certain methods.

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side ** 2

s = Square(4)
print(s.area())  # Output: 16
```

You **cannot instantiate** `Shape` directly because it's abstract.

---

## 🏷️ 8. Property Decorators (`@property`, `@setter`)

Used to make methods behave like attributes.

```python
class Circle:
    def __init__(self, radius):
        self._radius = radius

    @property
    def area(self):
        return 3.14 * self._radius ** 2

    @property
    def radius(self):
        return self._radius

    @radius.setter
    def radius(self, value):
        self._radius = value

c = Circle(5)
print(c.area)         # Output: 78.5
c.radius = 10
print(c.area)         # Output: 314.0
```

---

## 🧠 Summary Table

| Concept               | Keyword / Method      | Purpose                             |
|----------------------|-----------------------|-------------------------------------|
| Class                | `class`               | Blueprint for objects               |
| Constructor          | `__init__`            | Initializes new object              |
| Destructor           | `__del__`             | Clean up on deletion                |
| Inheritance          | `class B(A)`          | Reuse base class features           |
| Polymorphism         | Method Overriding     | Same method, different class        |
| Encapsulation        | `__var`, getter/setter| Protect data access                 |
| Abstraction          | `@abstractmethod`     | Hide complexity                     |
| Magic Methods        | `__str__`, `__len__`  | Customize built-in behavior         |
| Properties           | `@property`, `@setter`| Get/set like attributes             |

---

Would you like to build a **real-world OOP app** like a Student Management System or a Shopping Cart using these principles?

Great choice! Let's build a **Student Management System** using **OOP principles**. This example will cover:

---

## ✅ OOP Concepts Used

| Concept | Used For |
|--------|----------|
| **Classes & Objects** | Students, Courses, and the System |
| **Instance Variables & Methods** | Storing data and behaviors |
| **Encapsulation** | Protect student/course data |
| **Inheritance** | Optional future extension (e.g., GraduateStudent) |
| **Magic Methods** | Nicely formatted output |
| **@property** | Controlled access to attributes |

---

## 🏫 1. Basic Structure:

We’ll create:
- `Student` class
- `Course` class
- `StudentManagementSystem` class to manage both

---

## 📄 Full Code:

```python
# student_management.py

class Student:
    def __init__(self, student_id, name):
        self.student_id = student_id
        self.name = name
        self.courses = []

    def enroll(self, course):
        if course not in self.courses:
            self.courses.append(course)
            course.add_student(self)

    def __str__(self):
        return f"Student {self.student_id}: {self.name}"

class Course:
    def __init__(self, course_code, title):
        self.course_code = course_code
        self.title = title
        self.students = []

    def add_student(self, student):
        if student not in self.students:
            self.students.append(student)

    def __str__(self):
        return f"{self.course_code}: {self.title}"

class StudentManagementSystem:
    def __init__(self):
        self.students = {}
        self.courses = {}

    def add_student(self, student_id, name):
        if student_id not in self.students:
            self.students[student_id] = Student(student_id, name)
            print(f"✅ Added {name}")
        else:
            print("⚠️ Student already exists.")

    def add_course(self, course_code, title):
        if course_code not in self.courses:
            self.courses[course_code] = Course(course_code, title)
            print(f"📘 Course '{title}' added.")
        else:
            print("⚠️ Course already exists.")

    def enroll_student(self, student_id, course_code):
        student = self.students.get(student_id)
        course = self.courses.get(course_code)
        if student and course:
            student.enroll(course)
            print(f"📚 Enrolled {student.name} in {course.title}")
        else:
            print("❌ Student or course not found.")

    def display_students(self):
        print("\n🎓 All Students:")
        for student in self.students.values():
            print(f"{student} → {[c.course_code for c in student.courses]}")

    def display_courses(self):
        print("\n📘 All Courses:")
        for course in self.courses.values():
            print(f"{course} → {[s.name for s in course.students]}")
```

---

## ▶️ 2. Example Usage

```python
if __name__ == "__main__":
    system = StudentManagementSystem()

    # Add students
    system.add_student(1, "Alice")
    system.add_student(2, "Bob")

    # Add courses
    system.add_course("CS101", "Intro to Computer Science")
    system.add_course("MATH101", "Calculus I")

    # Enrollments
    system.enroll_student(1, "CS101")
    system.enroll_student(2, "MATH101")
    system.enroll_student(1, "MATH101")

    # Display data
    system.display_students()
    system.display_courses()
```

---

## 🧪 Output

```
✅ Added Alice
✅ Added Bob
📘 Course 'Intro to Computer Science' added.
📘 Course 'Calculus I' added.
📚 Enrolled Alice in Intro to Computer Science
📚 Enrolled Bob in Calculus I
📚 Enrolled Alice in Calculus I

🎓 All Students:
Student 1: Alice → ['CS101', 'MATH101']
Student 2: Bob → ['MATH101']

📘 All Courses:
CS101: Intro to Computer Science → ['Alice']
MATH101: Calculus I → ['Bob', 'Alice']
```

---

## 🚀 What Next?

Want to:
- Save/load to files?
- Add grading?
- Use a GUI with Tkinter or web frontend?
- Integrate SQLite?

Let me know what you'd like to add!

Great idea! Let’s extend your **Student Management System** with **file-saving and loading** features using **JSON** for simplicity.

---

## ✅ Goals:
- 📝 **Save student and course data to a file** (e.g., `data.json`)
- 📂 **Load the data back into the system**
- 🔐 Preserve relationships between students and their courses

We'll use:
- `json` module for file I/O
- Custom methods to **serialize** and **deserialize** objects

---

## 🧩 Updated Classes with Save/Load

```python
import json
from pathlib import Path

class Student:
    def __init__(self, student_id, name):
        self.student_id = student_id
        self.name = name
        self.courses = []  # Will hold course codes for saving

    def enroll(self, course):
        if course.course_code not in self.courses:
            self.courses.append(course.course_code)
            course.add_student(self)

    def __str__(self):
        return f"Student {self.student_id}: {self.name}"

    def to_dict(self):
        return {
            "student_id": self.student_id,
            "name": self.name,
            "courses": self.courses
        }

    @classmethod
    def from_dict(cls, data):
        student = cls(data["student_id"], data["name"])
        student.courses = data["courses"]
        return student


class Course:
    def __init__(self, course_code, title):
        self.course_code = course_code
        self.title = title
        self.students = []  # Will hold student IDs

    def add_student(self, student):
        if student.student_id not in self.students:
            self.students.append(student.student_id)

    def __str__(self):
        return f"{self.course_code}: {self.title}"

    def to_dict(self):
        return {
            "course_code": self.course_code,
            "title": self.title,
            "students": self.students
        }

    @classmethod
    def from_dict(cls, data):
        course = cls(data["course_code"], data["title"])
        course.students = data["students"]
        return course
```

---

## 🗂️ StudentManagementSystem with Save/Load

```python
class StudentManagementSystem:
    def __init__(self):
        self.students = {}
        self.courses = {}

    def add_student(self, student_id, name):
        if student_id not in self.students:
            self.students[student_id] = Student(student_id, name)
            print(f"✅ Added {name}")

    def add_course(self, course_code, title):
        if course_code not in self.courses:
            self.courses[course_code] = Course(course_code, title)
            print(f"📘 Course '{title}' added.")

    def enroll_student(self, student_id, course_code):
        student = self.students.get(student_id)
        course = self.courses.get(course_code)
        if student and course:
            student.enroll(course)
            print(f"📚 Enrolled {student.name} in {course.title}")

    def display_students(self):
        print("\n🎓 Students:")
        for student in self.students.values():
            print(f"{student} → {student.courses}")

    def display_courses(self):
        print("\n📘 Courses:")
        for course in self.courses.values():
            print(f"{course} → {course.students}")

    def save_data(self, filename="data.json"):
        data = {
            "students": [s.to_dict() for s in self.students.values()],
            "courses": [c.to_dict() for c in self.courses.values()]
        }
        with open(filename, "w") as f:
            json.dump(data, f, indent=4)
        print("💾 Data saved to", filename)

    def load_data(self, filename="data.json"):
        file_path = Path(filename)
        if not file_path.exists():
            print("⚠️ File not found. Starting fresh.")
            return

        with open(filename, "r") as f:
            data = json.load(f)

        # Load students
        self.students = {
            s["student_id"]: Student.from_dict(s) for s in data["students"]
        }

        # Load courses
        self.courses = {
            c["course_code"]: Course.from_dict(c) for c in data["courses"]
        }

        # Re-link student-course relationships
        for student in self.students.values():
            for course_code in student.courses:
                course = self.courses.get(course_code)
                if course:
                    course.add_student(student)

        print("📂 Data loaded from", filename)
```

---

## ▶️ Example Usage

```python
if __name__ == "__main__":
    system = StudentManagementSystem()
    system.load_data()

    system.add_student(1, "Alice")
    system.add_course("CS101", "Intro to CS")
    system.enroll_student(1, "CS101")

    system.display_students()
    system.display_courses()

    system.save_data()
```

---

## 💾 Example `data.json` Output

```json
{
  "students": [
    {
      "student_id": 1,
      "name": "Alice",
      "courses": ["CS101"]
    }
  ],
  "courses": [
    {
      "course_code": "CS101",
      "title": "Intro to CS",
      "students": [1]
    }
  ]
}
```

---

## ✅ Summary

| Feature | Implemented |
|--------|-------------|
| Save students/courses to file | ✅ |
| Load and restore relationships | ✅ |
| JSON format | ✅ |
| Error-safe loading | ✅ |

Want to add features like search, remove, or GUI next?

Sure! Let’s break down **Iterators**, **Generators**, **Lazy Evaluation**, **Decorators**, and **Context Managers** with **clear explanations and examples**.

---

## 🔁 **Iterators**

An **iterator** is an object that can be iterated (looped) over using `next()`.

### ✅ Creating an Iterator

```python
# Custom iterator that returns numbers up to a limit
class CountUpTo:
    def __init__(self, max):
        self.max = max
        self.current = 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.current > self.max:
            raise StopIteration
        val = self.current
        self.current += 1
        return val

counter = CountUpTo(3)
for number in counter:
    print(number)
```

**Output:**
```
1
2
3
```

---

## ⚙️ **Generators** and `yield`

Generators **generate values on the fly** using `yield`, which remembers the function’s state between calls.

### ✅ Example Generator Function

```python
def count_up_to(max):
    current = 1
    while current <= max:
        yield current
        current += 1

for num in count_up_to(3):
    print(num)
```

Same output as above, but much more memory-efficient.

---

## 🐢 **Lazy Evaluation**

Generators are a great example of **lazy evaluation**—values are computed only **when needed**.

### ✅ Example: Generating Even Numbers

```python
def even_numbers(n):
    for i in range(n):
        if i % 2 == 0:
            yield i

evens = even_numbers(10)
print(next(evens))  # 0
print(next(evens))  # 2
```

No entire list is stored in memory—only one value at a time!

---

## 🎁 **Function Decorators**

Decorators let you **wrap another function** to extend its behavior.

### ✅ Basic Function Decorator

```python
def log_decorator(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}")
        return func(*args, **kwargs)
    return wrapper

@log_decorator
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))
```

**Output:**
```
Calling greet
Hello, Alice!
```

---

## 📦 **Context Managers** (`with` statement)

Context managers help manage **resources** like files or database connections.

### ✅ Using `with` to open files

```python
with open("example.txt", "w") as file:
    file.write("Hello!")

# file is automatically closed after the block
```

---

## 🛠️ Creating Custom Context Manager

You can create one using a class with `__enter__` and `__exit__` methods.

```python
class ManagedFile:
    def __init__(self, filename):
        self.filename = filename

    def __enter__(self):
        self.file = open(self.filename, "w")
        return self.file

    def __exit__(self, exc_type, exc_val, exc_tb):
        self.file.close()
        print("File closed.")

with ManagedFile("log.txt") as f:
    f.write("Logging info...")
```

---

## ✅ Summary

| Concept        | Key Feature |
|----------------|-------------|
| **Iterator**   | Implements `__iter__()` and `__next__()` |
| **Generator**  | Uses `yield` to produce lazy values |
| **Lazy Eval**  | Saves memory by computing on demand |
| **Decorator**  | Wraps a function to modify/enhance it |
| **Context Manager** | Manages resources automatically (`with`) |

Would you like a mini-project using these ideas together (like logging file access or streaming large data)?


Creating **custom decorators** in Python is a powerful way to **extend the behavior of functions or methods**—like logging, authentication, performance timing, etc.—without modifying their original code.

Let’s break this down step-by-step with clear examples!

---

## ✅ 1. What is a Decorator?

A **decorator** is a function that takes another function as input, adds some functionality, and returns a new function.

---

## 🧱 2. Basic Structure of a Custom Decorator

```python
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Something before the function runs.")
        result = func(*args, **kwargs)
        print("Something after the function runs.")
        return result
    return wrapper
```

### 👇 Applying the decorator:
```python
@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

**Output:**
```
Something before the function runs.
Hello!
Something after the function runs.
```

---

## 📌 3. Decorator with Arguments

If your function takes arguments, your decorator must accept `*args` and `**kwargs`.

```python
def debug(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args} and {kwargs}")
        result = func(*args, **kwargs)
        print(f"{func.__name__} returned {result}")
        return result
    return wrapper

@debug
def add(a, b):
    return a + b

add(2, 3)
```

---

## 🕐 4. Timing Decorator Example

```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} ran in {end - start:.4f}s")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(1)

slow_function()
```

---

## 🎁 5. Decorator That Accepts Its Own Arguments

To make a decorator **accept its own arguments**, wrap it **one level deeper**.

```python
def repeat(n):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(3)
def greet():
    print("Hello!")

greet()
```

---

## 🧠 6. Use `functools.wraps` to Preserve Metadata

Without `wraps`, the decorated function loses its name and docstring.

```python
from functools import wraps

def safe_run(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        try:
            return func(*args, **kwargs)
        except Exception as e:
            print(f"Error: {e}")
    return wrapper

@safe_run
def risky():
    return 1 / 0

risky()
```

---

## 🔚 Summary

| Type                        | Use Case                            |
|-----------------------------|-------------------------------------|
| Basic Decorator             | Add pre/post functionality          |
| With `*args, **kwargs`      | Support flexible function arguments |
| With decorator arguments    | Pass config to decorators           |
| With `functools.wraps`      | Preserve metadata                   |

---

Would you like to:
- Chain multiple custom decorators?
- Apply decorators to **classes or methods**?
- Turn this into a **logging or authorization system**?

Let me know how deep you'd like to go!

Great! Let’s implement **decorators for class methods** and see how they work with both **instance methods** and **class methods**.

---

## ✅ Example Use Case

Let’s create a class `Account` and add a **decorator** that:
- Logs the method name and arguments.
- Works for both instance and class methods.

---

## 🔧 Step 1: Define the Decorator

Use `functools.wraps` to preserve metadata.

```python
from functools import wraps

def method_logger(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        print(f"[LOG] Calling: {func.__name__}")
        print(f"       args: {args}")
        print(f"       kwargs: {kwargs}")
        result = func(*args, **kwargs)
        print(f"[LOG] {func.__name__} returned: {result}")
        return result
    return wrapper
```

---

## 🧱 Step 2: Create a Class and Apply the Decorator

```python
class Account:
    def __init__(self, name, balance):
        self.name = name
        self.balance = balance

    @method_logger
    def deposit(self, amount):
        self.balance += amount
        return self.balance

    @method_logger
    def withdraw(self, amount):
        if self.balance >= amount:
            self.balance -= amount
            return self.balance
        else:
            return "Insufficient funds"

    @classmethod
    @method_logger
    def bank_name(cls):
        return "Python National Bank"
```

---

## 🚀 Step 3: Use the Decorated Methods

```python
acc = Account("Valli", 1000)

acc.deposit(500)
acc.withdraw(200)
Account.bank_name()
```

---

## 🖨️ Output

```
[LOG] Calling: deposit
       args: (<__main__.Account object at 0x...>, 500)
       kwargs: {}
[LOG] deposit returned: 1500

[LOG] Calling: withdraw
       args: (<__main__.Account object at 0x...>, 200)
       kwargs: {}
[LOG] withdraw returned: 1300

[LOG] Calling: bank_name
       args: (<class '__main__.Account'>,)
       kwargs: {}
[LOG] bank_name returned: Python National Bank
```

---

## 🧠 Bonus Tips

- You can also apply decorators to `@staticmethod`s.
- Decorators can be stacked for additional functionality (e.g., `@logger`, `@auth_required`, etc.).

---

Would you like to:
- Add **authentication** or **access control** via decorators?
- Use **class-based decorators**?
- Log to a **file instead of console**?

Let me know and I’ll guide you through!

Absolutely! Class-based decorators are great for implementing **more complex or stateful logic**. Unlike function-based decorators, they use a class with a `__call__()` method to wrap the target function or method.

---

## 🧠 Why Use Class-Based Decorators?

- Maintain **state/data** across function calls.
- More readable for complex logic.
- Easier to extend or reuse.

---

## ✅ 1. Basic Class-Based Decorator Example

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.count = 0

    def __call__(self, *args, **kwargs):
        self.count += 1
        print(f"[INFO] {self.func.__name__} has been called {self.count} times.")
        return self.func(*args, **kwargs)
```

### Apply it to a Function:
```python
@CallCounter
def greet(name):
    print(f"Hello, {name}!")

greet("Valli")
greet("Sree")
```

---

## ✅ 2. Using Class-Based Decorator on Class Methods

Let's use a decorator that:
- Logs method name
- Logs which instance called it

---

### Step 1: Define the Decorator

```python
from functools import wraps

class MethodLogger:
    def __init__(self, func):
        self.func = func
        wraps(func)(self)  # Preserve metadata

    def __get__(self, instance, owner):
        # Bind the method to the instance using __get__
        def wrapper(*args, **kwargs):
            print(f"[LOG] {self.func.__name__} called on {instance} with args={args}, kwargs={kwargs}")
            result = self.func(instance, *args, **kwargs)
            print(f"[LOG] Returned: {result}")
            return result
        return wrapper
```

---

### Step 2: Apply to a Class

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    @MethodLogger
    def deposit(self, amount):
        self.balance += amount
        return self.balance

    @MethodLogger
    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            return self.balance
        return "Insufficient funds"
```

---

### Step 3: Run It

```python
acc = BankAccount("Valli", 1000)
acc.deposit(200)
acc.withdraw(500)
```

---

## 🖨 Output

```
[LOG] deposit called on <__main__.BankAccount object at 0x...> with args=(200,), kwargs={}
[LOG] Returned: 1200
[LOG] withdraw called on <__main__.BankAccount object at 0x...> with args=(500,), kwargs={}
[LOG] Returned: 700
```

---

## 🔁 3. Stateful Class-Based Decorator Example

Let’s create a **rate limiter**—you can call a method only `n` times.

```python
class LimitCalls:
    def __init__(self, max_calls=3):
        self.max_calls = max_calls
        self.calls = 0

    def __call__(self, func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            if self.calls >= self.max_calls:
                print(f"[ERROR] {func.__name__} limit reached!")
                return None
            self.calls += 1
            return func(*args, **kwargs)
        return wrapper
```

### Apply it:

```python
class Greeter:
    @LimitCalls(2)
    def greet(self, name):
        print(f"Hi, {name}!")

g = Greeter()
g.greet("Alice")
g.greet("Bob")
g.greet("Charlie")  # This call will be blocked
```

---

## ✅ Summary

| Use Case                  | Decorator Type        |
|---------------------------|-----------------------|
| Simple enhancements       | Function-based        |
| Stateful or complex logic | Class-based decorators |
| Works on methods too      | Yes, with `__get__()` |

---

Want to take it further?
- Create **parameterized class-based decorators**
- Combine with **context managers**
- Turn into a reusable **decorator library**

Let me know what you'd like next!

Sure! Let's break it down into two major sections:

---

# ✅ **1. Regular Expressions (RegEx) in Python**

## 🔹 What is RegEx?

Regular Expressions are patterns used to match character combinations in strings.

In Python, it's supported through the `re` module.

---

### 🔹 Import the Module
```python
import re
```

---

## ✅ **Regular Expression Basics**

### Example: Check if string starts with "Hello"
```python
text = "Hello World"
match = re.match(r"Hello", text)

if match:
    print("Match found!")
```

---

## ✅ **Pattern Matching (Assertions and Grouping)**

### Example: Extract name and age
```python
data = "Name: Valli, Age: 25"
pattern = r"Name: (\w+), Age: (\d+)"

match = re.search(pattern, data)
if match:
    print(match.group(1))  # Valli
    print(match.group(2))  # 25
```

- `(\w+)` → Group for name
- `(\d+)` → Group for digits

---

## ✅ **Common `re` Functions**

### `re.findall()`: Returns all matches
```python
emails = "Send to valli@gmail.com and sree@yahoo.com"
found = re.findall(r"[\w.-]+@[\w.-]+", emails)
print(found)  # ['valli@gmail.com', 'sree@yahoo.com']
```

### `re.search()`: Finds first match
```python
result = re.search(r"\d{3}", "House number 456 is ready.")
print(result.group())  # 456
```

### `re.split()`: Split string by pattern
```python
text = "apple, banana; orange|grapes"
parts = re.split(r"[;,|]\s*", text)
print(parts)  # ['apple', 'banana', 'orange', 'grapes']
```

---

# ✅ **2. Working with Databases (SQL + Python)**

We'll use **SQLite** (built-in), but the concept applies to MySQL too.

---

## ✅ **SQL Basics – CRUD**

| Operation | SQL Command   |
|----------|---------------|
| Create   | `CREATE TABLE`|
| Read     | `SELECT`      |
| Update   | `UPDATE`      |
| Delete   | `DELETE`      |

---

## ✅ **Connect to SQLite Database**

```python
import sqlite3

# Connect or create DB
conn = sqlite3.connect("students.db")
cursor = conn.cursor()
```

---

## ✅ **Create Table**

```python
cursor.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER
)
""")
conn.commit()
```

---

## ✅ **Insert Data**

```python
cursor.execute("INSERT INTO students (name, age) VALUES (?, ?)", ("Valli", 25))
conn.commit()
```

---

## ✅ **Read Data**

```python
cursor.execute("SELECT * FROM students")
for row in cursor.fetchall():
    print(row)
```

---

## ✅ **Update Data**

```python
cursor.execute("UPDATE students SET age = ? WHERE name = ?", (26, "Valli"))
conn.commit()
```

---

## ✅ **Delete Data**

```python
cursor.execute("DELETE FROM students WHERE name = ?", ("Valli",))
conn.commit()
```

---

## ✅ **Close the Connection**

```python
conn.close()
```

---

# ✅ Bonus: Combine RegEx + SQL

### Extract emails and insert into DB
```python
import sqlite3
import re

emails = "Contact valli@gmail.com or sree@yahoo.com"

matches = re.findall(r"[\w.-]+@[\w.-]+", emails)

conn = sqlite3.connect("emails.db")
cursor = conn.cursor()

cursor.execute("CREATE TABLE IF NOT EXISTS contacts (email TEXT)")

for email in matches:
    cursor.execute("INSERT INTO contacts (email) VALUES (?)", (email,))
conn.commit()
conn.close()
```

---

Would you like help connecting to a **MySQL** database next or building a **mini CLI database app** using this knowledge?

Absolutely! Let’s go step-by-step through **advanced SQL queries** using **JOINs** with clear examples. We'll use **SQLite with Python**, but the SQL syntax applies to MySQL, PostgreSQL, etc.

---

## 🧠 What is a JOIN?

A **JOIN** combines rows from two or more tables based on a related column between them.

---

## 🎓 Example Scenario: `students` and `courses`

We’ll create two tables:

- **students**: stores student info  
- **courses**: stores what courses each student is enrolled in

---

### ✅ Step 1: Set Up Tables

```python
import sqlite3

conn = sqlite3.connect("school.db")
cur = conn.cursor()

# Create students table
cur.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY,
    name TEXT
)
""")

# Create courses table
cur.execute("""
CREATE TABLE IF NOT EXISTS courses (
    course_id INTEGER PRIMARY KEY,
    student_id INTEGER,
    course_name TEXT,
    FOREIGN KEY (student_id) REFERENCES students(id)
)
""")
conn.commit()
```

---

### ✅ Step 2: Insert Sample Data

```python
# Insert students
cur.execute("INSERT INTO students (id, name) VALUES (1, 'Valli')")
cur.execute("INSERT INTO students (id, name) VALUES (2, 'Sree')")

# Insert courses
cur.execute("INSERT INTO courses (student_id, course_name) VALUES (1, 'Math')")
cur.execute("INSERT INTO courses (student_id, course_name) VALUES (1, 'Physics')")
cur.execute("INSERT INTO courses (student_id, course_name) VALUES (2, 'Chemistry')")
conn.commit()
```

---

## 🔍 JOIN Examples

---

### ✅ 1. INNER JOIN — Match only where student has courses

```python
cur.execute("""
SELECT students.name, courses.course_name
FROM students
INNER JOIN courses ON students.id = courses.student_id
""")

for row in cur.fetchall():
    print(row)
```

🧾 **Output:**
```
('Valli', 'Math')
('Valli', 'Physics')
('Sree', 'Chemistry')
```

---

### ✅ 2. LEFT JOIN — Show all students (even if no courses)

```python
cur.execute("""
SELECT students.name, courses.course_name
FROM students
LEFT JOIN courses ON students.id = courses.student_id
""")

for row in cur.fetchall():
    print(row)
```

🧾 **Output:**  
(If someone has no course, course_name will be `None`)

---

### ✅ 3. RIGHT JOIN (SQLite doesn’t support it natively)

But in databases like MySQL:

```sql
SELECT students.name, courses.course_name
FROM courses
RIGHT JOIN students ON students.id = courses.student_id
```

> SQLite workaround = swap tables + LEFT JOIN.

---

### ✅ 4. JOIN with WHERE clause

```python
cur.execute("""
SELECT students.name, courses.course_name
FROM students
INNER JOIN courses ON students.id = courses.student_id
WHERE courses.course_name = 'Math'
""")

print(cur.fetchall())
```

🧾 **Output:**
```
[('Valli', 'Math')]
```

---

## 🧠 Summary

| Type        | Description                              |
|-------------|------------------------------------------|
| `INNER JOIN` | Matches only where keys exist in both   |
| `LEFT JOIN`  | All from left + matched from right      |
| `RIGHT JOIN` | All from right + matched from left (not in SQLite) |
| `FULL JOIN`  | All records when there is a match (PostgreSQL) |

---

Want to see **aggregates (COUNT, GROUP BY)** or **JOIN across 3+ tables** next?

Absolutely! Let’s implement **aggregate functions** like `COUNT()` and use `GROUP BY` in SQL with Python using **SQLite**. These are powerful tools to summarize and group data from tables.

---

## 🎓 Scenario: `students` and `courses`

Assume we already have two tables:

- `students(id, name)`
- `courses(course_id, student_id, course_name)`

We’ll count how many courses each student is enrolled in.

---

### ✅ Step 1: Create Tables and Insert Data

If you haven’t already:

```python
import sqlite3

conn = sqlite3.connect("school.db")
cur = conn.cursor()

# Create students table
cur.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY,
    name TEXT
)
""")

# Create courses table
cur.execute("""
CREATE TABLE IF NOT EXISTS courses (
    course_id INTEGER PRIMARY KEY AUTOINCREMENT,
    student_id INTEGER,
    course_name TEXT,
    FOREIGN KEY (student_id) REFERENCES students(id)
)
""")

# Insert sample data
cur.execute("DELETE FROM students")
cur.execute("DELETE FROM courses")

students_data = [(1, 'Valli'), (2, 'Sree'), (3, 'Avi')]
courses_data = [
    (1, 'Math'),
    (1, 'Physics'),
    (2, 'Chemistry'),
    (1, 'English'),
    (3, 'Biology'),
    (3, 'Math')
]

cur.executemany("INSERT INTO students (id, name) VALUES (?, ?)", students_data)
cur.executemany("INSERT INTO courses (student_id, course_name) VALUES (?, ?)", courses_data)
conn.commit()
```

---

### ✅ Step 2: COUNT Courses Per Student with GROUP BY

```python
cur.execute("""
SELECT students.name, COUNT(courses.course_name) AS total_courses
FROM students
LEFT JOIN courses ON students.id = courses.student_id
GROUP BY students.id
""")

results = cur.fetchall()
for name, count in results:
    print(f"{name} is enrolled in {count} course(s).")
```

🧾 **Output:**
```
Valli is enrolled in 3 course(s).
Sree is enrolled in 1 course(s).
Avi is enrolled in 2 course(s).
```

---

### ✅ Step 3: Using Other Aggregates (SUM, AVG – for example purposes)

Let’s say we track `course_credits`.

```python
# Add credits column for demo
cur.execute("ALTER TABLE courses ADD COLUMN credits INTEGER")

# Update with some credits
cur.execute("UPDATE courses SET credits = 3 WHERE course_name = 'Math'")
cur.execute("UPDATE courses SET credits = 4 WHERE course_name = 'Physics'")
cur.execute("UPDATE courses SET credits = 2 WHERE course_name = 'English'")
cur.execute("UPDATE courses SET credits = 3 WHERE course_name = 'Biology'")
cur.execute("UPDATE courses SET credits = 3 WHERE course_name = 'Chemistry'")
conn.commit()
```

### Total credits per student:

```python
cur.execute("""
SELECT students.name, SUM(courses.credits) as total_credits
FROM students
LEFT JOIN courses ON students.id = courses.student_id
GROUP BY students.id
""")

for row in cur.fetchall():
    print(row)
```

🧾 **Sample Output:**
```
('Valli', 9)
('Sree', 3)
('Avi', 6)
```

---

## ✅ Common Aggregate Functions

| Function | Description                         |
|----------|-------------------------------------|
| `COUNT()` | Number of rows                     |
| `SUM()`   | Total sum of a column              |
| `AVG()`   | Average of numeric values          |
| `MIN()`   | Minimum value                      |
| `MAX()`   | Maximum value                      |

---

Would you like to also:
- Add `HAVING` clause to filter groups?
- Visualize this data (e.g., with a bar chart)?
- Store this summary in a new table?

Let me know what’s next!

Absolutely! Let's break this down into **practical, clear sections** with **examples** to help you understand **Web Scraping** and **APIs** using Python.

---

# 🕸️ WEB SCRAPING IN PYTHON

---

## ✅ 1. HTML Parsing with `BeautifulSoup`

**Install the required libraries:**

```bash
pip install requests beautifulsoup4
```

### ▶️ Example: Scrape Titles from a Webpage

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"
response = requests.get(url)

soup = BeautifulSoup(response.text, 'html.parser')

# Extract all h1 tags
for heading in soup.find_all("h1"):
    print(heading.text)
```

✅ You can use `.find()`, `.find_all()`, `.select()` to target HTML elements.

---

## ✅ 2. Requests and Responses (`requests` module)

```python
import requests

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")

print("Status Code:", response.status_code)
print("Headers:", response.headers)
print("Body:", response.text)
```

---

## ✅ 3. Web Scraping with **Scrapy**

**Scrapy** is a more powerful and scalable scraping framework.

### Install:

```bash
pip install scrapy
```

### Create a Scrapy project:
```bash
scrapy startproject myproject
cd myproject
scrapy genspider quotes quotes.toscrape.com
```

### Sample Spider (`quotes.py`):

```python
import scrapy

class QuotesSpider(scrapy.Spider):
    name = "quotes"
    start_urls = ["http://quotes.toscrape.com/"]

    def parse(self, response):
        for quote in response.css("div.quote"):
            yield {
                'text': quote.css("span.text::text").get(),
                'author': quote.css("span small::text").get(),
            }
```

Run with:
```bash
scrapy crawl quotes -o quotes.json
```

---

## ✅ 4. Data Storage Options

- Save to JSON: `json.dump()`
- Save to CSV: `csv.writer()`
- Save to SQLite/MySQL: Use `sqlite3` or `sqlalchemy`

---

# 🔗 WORKING WITH APIs

---

## ✅ 5. APIs Basics (REST API Overview)

REST APIs allow communication over HTTP using:
- **GET** – Retrieve data
- **POST** – Create data
- **PUT/PATCH** – Update data
- **DELETE** – Delete data

---

## ✅ 6. Working with REST APIs

### ▶️ Example: GET Request to Fake API

```python
import requests

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
data = response.json()

print(data['title'])
```

### ▶️ Example: POST Request

```python
response = requests.post("https://jsonplaceholder.typicode.com/posts", json={
    "title": "New Post",
    "body": "This is the content",
    "userId": 1
})

print(response.json())
```

---

## ✅ 7. Handling JSON Data

```python
import json

# Convert dict to JSON
data = {'name': 'Valli', 'age': 25}
json_str = json.dumps(data)

# Convert JSON to dict
parsed = json.loads(json_str)
print(parsed['name'])
```

---

## ✅ 8. Creating REST APIs with Flask

Install Flask:

```bash
pip install flask
```

### ▶️ Example: Simple Flask API

```python
from flask import Flask, jsonify, request

app = Flask(__name__)

students = []

@app.route('/students', methods=['GET'])
def get_students():
    return jsonify(students)

@app.route('/students', methods=['POST'])
def add_student():
    student = request.get_json()
    students.append(student)
    return jsonify(student), 201

if __name__ == '__main__':
    app.run(debug=True)
```

Test it with:
```bash
curl http://127.0.0.1:5000/students
curl -X POST -H "Content-Type: application/json" -d '{"name":"Valli"}' http://127.0.0.1:5000/students
```

---

## 🧠 Summary

| Tool        | Purpose                        |
|-------------|-------------------------------|
| BeautifulSoup | Parse HTML content             |
| Requests      | Send HTTP requests             |
| Scrapy        | Scalable web scraping          |
| JSON          | Work with API responses        |
| Flask         | Create REST APIs in Python     |

---

Would you like to build a small project that uses both **scraping** and **APIs**, like a **news aggregator** or **job listing fetcher**?

Sure! Working with **dates and times** is very common in Python — whether it's for logging, timestamps, scheduling, or formatting user data.

Python provides a powerful module called `datetime` to handle this.

---

# 🕓 Working with Dates and Times in Python

We'll cover:

1. `datetime` Module Basics  
2. Parsing Dates and Times  
3. Formatting Date/Time Strings  

---

## ✅ 1. `datetime` Module Basics

You can use the `datetime` module to work with **dates**, **times**, or both.

### ▶️ Getting the current date and time

```python
from datetime import datetime

now = datetime.now()
print("Current Date and Time:", now)
```

📌 Output:
```
Current Date and Time: 2025-04-04 12:34:56.789123
```

### ▶️ Extract parts of the date

```python
print("Year:", now.year)
print("Month:", now.month)
print("Day:", now.day)
print("Hour:", now.hour)
print("Minute:", now.minute)
```

---

## ✅ 2. Parsing Dates and Times

Sometimes, you get a **string** like `"04-04-2025"` and want to turn it into a Python `datetime` object.

### ▶️ Using `strptime()` to parse date strings

```python
from datetime import datetime

date_str = "04-04-2025"
parsed_date = datetime.strptime(date_str, "%d-%m-%Y")

print("Parsed Date:", parsed_date)
```

📌 `%d` = day, `%m` = month, `%Y` = 4-digit year

---

## ✅ 3. Formatting Date/Time Strings

Convert a `datetime` object back to a string in a specific format using `strftime()`.

```python
from datetime import datetime

now = datetime.now()

formatted = now.strftime("%A, %d %B %Y %I:%M %p")
print("Formatted:", formatted)
```

📌 Output:
```
Formatted: Friday, 04 April 2025 12:34 PM
```

### ⏱️ Common Format Codes:

| Code | Meaning           | Example       |
|------|-------------------|---------------|
| `%Y` | Year (4 digits)   | 2025          |
| `%y` | Year (2 digits)   | 25            |
| `%m` | Month (01–12)     | 04            |
| `%B` | Month name        | April         |
| `%d` | Day (01–31)       | 04            |
| `%A` | Weekday name      | Friday        |
| `%H` | Hour (24h)        | 13            |
| `%I` | Hour (12h)        | 01            |
| `%p` | AM or PM          | PM            |
| `%M` | Minute            | 34            |

---

### 🗓 Bonus: Working with `date` and `time` objects

```python
from datetime import date, time

today = date.today()
print("Date only:", today)

t = time(14, 30)
print("Time only:", t)
```

---

### 🧮 Doing Math with Dates (Timedelta)

```python
from datetime import timedelta

future = now + timedelta(days=7)
print("7 days from now:", future)
```

---

Would you like to see **how to calculate age from birthdate** or build a **countdown timer** next?

Great question! In Python, calculating the **difference between two dates** is straightforward using the `datetime` module. The result is a `timedelta` object, which represents the **duration** between the two dates.

---

## ✅ Example: Calculate Date Difference

```python
from datetime import datetime

# Define two dates
date1 = datetime(2025, 4, 4)
date2 = datetime(2025, 1, 1)

# Calculate difference
difference = date1 - date2

print("Difference:", difference)
print("Days:", difference.days)
print("Seconds:", difference.total_seconds())
```

### 🧾 Output:
```
Difference: 93 days, 0:00:00
Days: 93
Seconds: 8035200.0
```

---

## ✅ Real-World Example: Calculate Age

```python
from datetime import datetime

birthdate_str = "2000-08-15"
birthdate = datetime.strptime(birthdate_str, "%Y-%m-%d")

today = datetime.now()
age_days = (today - birthdate).days
age_years = age_days // 365

print(f"You are approximately {age_years} years old.")
```

---

## ✅ Bonus: Difference in Hours/Minutes

You can also get hours and minutes by converting `.total_seconds()`:

```python
from datetime import datetime

start = datetime(2025, 4, 4, 9, 0)
end = datetime(2025, 4, 4, 17, 30)

diff = end - start
minutes = diff.total_seconds() / 60
hours = diff.total_seconds() / 3600

print(f"Worked for {hours:.2f} hours ({minutes:.0f} minutes)")
```

🧾 Output:
```
Worked for 8.5 hours (510 minutes)
```

---

Would you like a small utility function to calculate the difference between *any* two date strings?

Absolutely! Let’s break down **Concurrency** and **Parallelism** in Python with clear explanations and practical code examples.

---

# 🧠 Concurrency vs Parallelism

| Concept        | Description |
|----------------|-------------|
| **Concurrency** | Multiple tasks progress at **overlapping times** (interleaved execution). |
| **Parallelism** | Multiple tasks run **at the same time** using multiple cores. |

---

## 🧵 1. Threading (Concurrency with Threads)

Python’s `threading` module allows running multiple threads **concurrently** — useful for I/O-bound tasks (e.g., downloading files, API calls).

### ▶️ Example: Using `threading`

```python
import threading
import time

def print_numbers():
    for i in range(5):
        print(f"Number: {i}")
        time.sleep(1)

def print_letters():
    for ch in "ABCDE":
        print(f"Letter: {ch}")
        time.sleep(1)

# Create threads
t1 = threading.Thread(target=print_numbers)
t2 = threading.Thread(target=print_letters)

t1.start()
t2.start()

t1.join()
t2.join()

print("Done!")
```

🧠 Threads share the same memory space and are lightweight.

---

## 🧠 2. Multiprocessing (Parallel Processing)

For **CPU-bound tasks** (like calculations), use the `multiprocessing` module — it uses separate **processes** that run in **parallel**.

### ▶️ Example: Using `multiprocessing`

```python
import multiprocessing
import time

def square(n):
    print(f"Square of {n} = {n * n}")
    time.sleep(1)

if __name__ == '__main__':
    numbers = [1, 2, 3, 4]
    processes = []

    for num in numbers:
        p = multiprocessing.Process(target=square, args=(num,))
        processes.append(p)
        p.start()

    for p in processes:
        p.join()

    print("All done.")
```

✅ Processes run on **different CPU cores** (true parallelism).

---

## ⚡ 3. Asyncio (Asynchronous I/O Operations)

`asyncio` is used for **non-blocking** I/O operations like network requests or file handling, especially where you wait for a lot of responses (e.g., many APIs).

### ▶️ Example: Basic `asyncio` Usage

```python
import asyncio

async def greet(name):
    print(f"Hello, {name}!")
    await asyncio.sleep(1)
    print(f"Goodbye, {name}!")

async def main():
    await asyncio.gather(
        greet("Alice"),
        greet("Bob")
    )

asyncio.run(main())
```

⏱️ While one task is "sleeping", the other can proceed — great for high-performance web apps or real-time dashboards.

---

## 🔄 Summary: When to Use What?

| Use Case              | Module           |
|-----------------------|------------------|
| Downloading files     | `threading` or `asyncio` |
| Processing images     | `multiprocessing` |
| High-performance APIs | `asyncio`         |
| CPU-heavy tasks       | `multiprocessing` |
| Simple multitasking   | `threading`       |

---

Would you like a real-world example like **multi-threaded web scraper** or **async API fetcher** next?

Awesome! Let's build a simple **multi-threaded web scraper** using Python's `threading` module and `requests` + `BeautifulSoup` to scrape titles from multiple web pages concurrently.

---

## ✅ Objective:
We’ll scrape the `<title>` tag from multiple URLs **simultaneously** using **threads**.

---

## 🔧 Requirements

```bash
pip install requests beautifulsoup4
```

---

## 🧵 Multi-threaded Web Scraper (Example)

```python
import threading
import requests
from bs4 import BeautifulSoup

# List of websites to scrape
urls = [
    'https://www.python.org',
    'https://www.wikipedia.org',
    'https://www.github.com',
    'https://www.stackoverflow.com',
    'https://www.djangoproject.com',
]

def fetch_title(url):
    try:
        print(f"Fetching: {url}")
        response = requests.get(url, timeout=5)
        soup = BeautifulSoup(response.text, 'html.parser')
        title = soup.title.string if soup.title else 'No Title Found'
        print(f"[{url}] ➜ Title: {title}")
    except Exception as e:
        print(f"[{url}] ➜ Error: {e}")

# Create threads for each URL
threads = []

for url in urls:
    t = threading.Thread(target=fetch_title, args=(url,))
    threads.append(t)
    t.start()

# Wait for all threads to complete
for t in threads:
    t.join()

print("\n✅ All scraping tasks completed.")
```

---

### 🧠 What’s Happening:
- We're spinning up one thread per URL.
- Each thread fetches and parses the `<title>` tag from the HTML content.
- Threads run concurrently, improving speed for I/O-bound operations like HTTP requests.

---

### 🧪 Sample Output:
```
Fetching: https://www.python.org
Fetching: https://www.wikipedia.org
Fetching: https://www.github.com
Fetching: https://www.stackoverflow.com
Fetching: https://www.djangoproject.com
[https://www.github.com] ➜ Title: GitHub: Let’s build from here
[https://www.stackoverflow.com] ➜ Title: Stack Overflow - Where Developers Learn, Share, & Build Careers
...
✅ All scraping tasks completed.
```

---

Would you like to:
- 🔁 Extend it to **scrape multiple pages per domain**?
- 📄 Save results to a **CSV or JSON file**?
- ⚙ Add a **thread pool (via `concurrent.futures`)** for better control?

Let me know what direction you want to go next!

Absolutely! Let's use **`asyncio`** and **`aiohttp`** to fetch data from multiple APIs **asynchronously**, which is perfect for I/O-bound tasks like calling many APIs at once.

---

## 🔧 Requirements

You'll need the `aiohttp` library:

```bash
pip install aiohttp
```

---

## 🚀 Objective

We'll call several APIs **concurrently** and print their JSON responses using `asyncio`.

---

### ✅ Example: Async API Fetcher

```python
import asyncio
import aiohttp

# List of APIs to call
urls = [
    'https://jsonplaceholder.typicode.com/posts/1',
    'https://jsonplaceholder.typicode.com/posts/2',
    'https://jsonplaceholder.typicode.com/users/1',
    'https://jsonplaceholder.typicode.com/todos/1',
]

# Async function to fetch a single URL
async def fetch(session, url):
    try:
        async with session.get(url) as response:
            data = await response.json()
            print(f"✅ Fetched from {url}: {data['id'] if 'id' in data else 'No ID'}")
            return data
    except Exception as e:
        print(f"❌ Error fetching {url}: {e}")

# Main async function
async def main():
    async with aiohttp.ClientSession() as session:
        tasks = [fetch(session, url) for url in urls]
        results = await asyncio.gather(*tasks)

# Run the async event loop
asyncio.run(main())
```

---

## 🧠 How it works:

- **`aiohttp.ClientSession()`** is used to create an efficient HTTP session.
- **`async with session.get()`** handles the API call non-blockingly.
- **`await asyncio.gather(*tasks)`** runs all tasks concurrently.

---

## 🔁 Sample Output:

```
✅ Fetched from https://jsonplaceholder.typicode.com/posts/1: 1
✅ Fetched from https://jsonplaceholder.typicode.com/posts/2: 2
✅ Fetched from https://jsonplaceholder.typicode.com/users/1: 1
✅ Fetched from https://jsonplaceholder.typicode.com/todos/1: 1
```

---

Would you like to:
- ⏳ Add **timeout or retry logic**?
- 📝 Save the fetched data to a **file**?
- 🔒 Use **authentication tokens** for secure APIs?

Let me know how you'd like to extend this!

Perfect! Let's build a simple **multiprocessing image processor** using Python's `multiprocessing` module and the `Pillow` library.

We’ll apply a basic transformation (like converting images to grayscale or resizing them) using **parallel processing** — ideal for CPU-bound operations like image editing.

---

## 🧰 Requirements

Install Pillow (Python Imaging Library):

```bash
pip install pillow
```

---

## ✅ Objective

- Load multiple images from a folder
- Process them (e.g., convert to grayscale)
- Save the processed images to an output folder
- Use **multiprocessing** to speed it up

---

## 🖼️ Folder Structure

```
image_processor/
├── input/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
├── output/
└── script.py
```

---

## 🧠 Code: `script.py`

```python
import os
from PIL import Image
from multiprocessing import Pool, cpu_count

# Paths
INPUT_DIR = 'input'
OUTPUT_DIR = 'output'

# Ensure output folder exists
os.makedirs(OUTPUT_DIR, exist_ok=True)

# Process a single image
def process_image(filename):
    input_path = os.path.join(INPUT_DIR, filename)
    output_path = os.path.join(OUTPUT_DIR, filename)

    try:
        with Image.open(input_path) as img:
            gray_img = img.convert('L')  # Convert to grayscale
            gray_img.save(output_path)
            print(f"✅ Processed: {filename}")
    except Exception as e:
        print(f"❌ Error with {filename}: {e}")

# Main function using multiprocessing
def main():
    image_files = [f for f in os.listdir(INPUT_DIR) if f.endswith(('.png', '.jpg', '.jpeg'))]

    with Pool(cpu_count()) as pool:
        pool.map(process_image, image_files)

    print("\n🎉 All images processed.")

if __name__ == '__main__':
    main()
```

---

## ⚡ How it Works:

- Uses `Pool` to assign image files to available CPU cores.
- Each image is opened, converted to grayscale, and saved.
- Parallel execution dramatically improves performance with many images.

---

## 🧪 Output

Processed grayscale images are saved in the `output/` folder.

---

## 🛠️ Extension Ideas

- 📏 Resize or crop images.
- 🧠 Apply custom filters.
- 🗂️ Process images by categories (e.g., by file type).
- 🧵 Combine this with threading for downloading + processing.

---

Would you like to:
- ➕ Add watermarking?
- 🧼 Clean corrupted images?
- 🧾 Log the processing time per image?

Let me know how you'd like to expand this!