## **Control Flow: Conditional Statements, Loops, Break, and Continue in Python**
Control flow statements dictate the execution order of a program. They determine which code runs and how many times it should execute.

---

## **1. Conditional Statements**
Conditional statements execute different blocks of code based on conditions.

### **If-Else Statement**
```python
x = 10
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```
#### **Nested If-Else**
```python
num = 15
if num % 2 == 0:
    if num % 4 == 0:
        print("Divisible by 4")
    else:
        print("Even but not divisible by 4")
else:
    print("Odd")
```
---
## **2. Loops**
Loops help execute a block of code multiple times.

### **For Loop**
Used for iterating over sequences (lists, tuples, dictionaries, strings, etc.).
```python
for i in range(1, 6):  # Iterates from 1 to 5
    print(i)
```

### **Iterating Over a List**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### **While Loop**
Executes as long as a condition is `True`.
```python
count = 5
while count > 0:
    print(count)
    count -= 1  # Decrement counter
```

---
## **3. Break and Continue Statements**
### **Break Statement**
`break` exits the loop completely.

```python
for num in range(1, 10):
    if num == 5:
        break  # Loop stops when num is 5
    print(num)
```
**Output:**
```
1
2
3
4
```

### **Continue Statement**
`continue` skips the current iteration and proceeds with the next.

```python
for num in range(1, 10):
    if num == 5:
        continue  # Skips printing 5
    print(num)
```
**Output:**
```
1
2
3
4
6
7
8
9
```

---
## **10 Intermediate Python Problems on Control Flow**
Try these to master conditionals, loops, `break`, and `continue`!

### **1. FizzBuzz Problem**
Write a function that prints numbers from `1 to N`, but:
- Print **"Fizz"** for multiples of 3.
- Print **"Buzz"** for multiples of 5.
- Print **"FizzBuzz"** for multiples of both.

```python
fizzbuzz(15)
# Output: 1, 2, Fizz, 4, Buzz, ..., 14, FizzBuzz
```

---

### **2. Find the First Non-Repeating Character**
Write a function that finds the **first non-repeating character** in a string.

```python
first_unique("swiss")
# Output: "w"
```

---

### **3. Reverse a Number Without Converting to a String**
Write a function that reverses an integer **without converting it into a string**.

```python
reverse_number(1234)
# Output: 4321
```

---

### **4. Find Prime Numbers in a Range**
Write a function that prints **all prime numbers** between `1 to N`.

```python
prime_numbers(10)
# Output: [2, 3, 5, 7]
```

---

### **5. Find the Factorial of a Number Using Loops**
Write a function that calculates factorial **without recursion**.

```python
factorial(5)
# Output: 120
```

---

### **6. Check if a Number is Palindrome**
Write a function to check if a number is **palindromic** (reads the same forward and backward).

```python
is_palindrome(121)  # True
is_palindrome(123)  # False
```

---

### **7. Count the Frequency of Elements in a List**
Given a list, return a dictionary with **element frequencies**.

```python
arr = [1, 2, 2, 3, 3, 3]
# Output: {1: 1, 2: 2, 3: 3}
```

---

### **8. Print a Pyramid Pattern**
Write a program to print this pattern:
```
    *    
   ***   
  *****  
 *******
*********
```

---

### **9. Sum of Digits Using While Loop**
Write a function that takes a number and returns the **sum of its digits**.

```python
sum_digits(1234)
# Output: 10 (1+2+3+4)
```

---

### **10. Implement a Simple Calculator Using If-Else**
Write a function that takes `num1`, `num2`, and an **operator** (`+`, `-`, `*`, `/`) and returns the result.

```python

calculator(10, 5, '+')  # Output: 15
calculator(10, 5, '*')  # Output: 50
```
