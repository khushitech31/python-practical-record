# Programming Using Python - Practical Record

## Student Details

| Field | Details |
|---|---|
| Name | Khushi Kumari |
| Course | B.Sc. (Hons.) Computer Science |
| Semester | I (First Semester) |
| Roll Number | 26570030 |
| Subject | Programming Using Python |
| College | Ramanujan College, University of Delhi |

## How to Run

1. Install Python 3.
2. Save the program with a `.py` extension.
3. Open the terminal in the program's folder.
4. Run the program using:

```bash
python filename.py
```

## **CONTENT**

1. Roots of a Quadratic Equation
2. Prime Numbers
3. Star Pyramids
4. Character Classification
5. String Operations
6. Swap Prefixes of Two Strings
7. Substring Indices
8. Cubes of Even Integers
9. File Handling
10. Dictionary of Cubes
11. Tuple Operations
12. Employee Class and Object Counting
13. Class Point2D
14. Inheritance: Class Point3D
15. Exception Handling for a Name


##  **Practical 01 - Roots of a Quadratic Equation**
Problem: Write a program to find the roots of a quadratic equation.

**Code:**

```python
import math

a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

if a == 0:
    print("Not a quadratic equation")
else:
    d = b**2 - 4*a*c

    if d > 0:
        r1 = (-b + math.sqrt(d)) / (2*a)
        r2 = (-b - math.sqrt(d)) / (2*a)
        print("Two distinct real roots:", r1, "and", r2)
    elif d == 0:
        print("Equal roots:", -b / (2*a))
    else:
        real = -b / (2*a)
        imag = math.sqrt(-d) / (2*a)
        print(f"Complex roots: {real} ± {imag}i")
```
**Output:**

```text
Enter a: 1
Enter b: -5
Enter c: 6
Two distinct real roots: 3.0 and 2.0
```
---

## Practical 02 – Prime Numbers

**Problem Statement:** Write a Python program to check whether a given number is prime or not.

**Code:**

```python
n = int(input("Enter a number: "))

if n <= 1:
    print(n, "is not a prime number")
else:
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            print(n, "is not a prime number")
            break
    else:
        print(n, "is a prime number")
```

**Output:**

```text
Enter a number: 17
17 is a prime number
```

---

## Practical 03 – Star Pyramids

**Problem Statement:** Write a Python program to print a pyramid pattern using stars.

**Code:**

```python
n = int(input("Enter the number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)
```

**Output:**

```text
Enter the number of rows: 5
    *
   * *
  * * *
 * * * *
* * * * *
```

---

## Practical 04 – Character Classification

**Problem Statement:** Write a Python program to classify a character as a vowel, consonant, digit, whitespace, or special character.

**Code:**

```python
ch = input("Enter a character: ")

if len(ch) != 1:
    print("Please enter a single character")
elif ch.isalpha():
    if ch.lower() in "aeiou":
        print("Vowel")
    else:
        print("Consonant")
elif ch.isdigit():
    print("Digit")
elif ch.isspace():
    print("Whitespace")
else:
    print("Special character")
```

**Output:**

```text
Enter a character: A
Vowel
```

---

## Practical 05 – String Operations

**Problem Statement:** Write a Python program to perform basic string operations such as finding the length, converting case, reversing a string, and checking whether it is a palindrome.

**Code:**

```python
s = input("Enter a string: ")

print("Length:", len(s))
print("Uppercase:", s.upper())
print("Lowercase:", s.lower())
print("Reversed:", s[::-1])

if s.lower() == s[::-1].lower():
    print("Palindrome")
else:
    print("Not a palindrome")
```

**Output:**

```text
Enter a string: Madam
Length: 5
Uppercase: MADAM
Lowercase: madam
Reversed: madaM
Palindrome
```

---

## Practical 06 – Swap Prefixes of Two Strings

**Problem Statement:** Write a Python program to swap the first characters of two strings.

**Code:**

```python
s1 = input("Enter the first string: ")
s2 = input("Enter the second string: ")

if len(s1) > 0 and len(s2) > 0:
    s1, s2 = s2[0] + s1[1:], s1[0] + s2[1:]
    print("First string:", s1)
    print("Second string:", s2)
else:
    print("Both strings must be non-empty")
```

**Output:**

```text
Enter the first string: abc
Enter the second string: xyz
First string: xbc
Second string: ayz
```

---

## Practical 07 – Substring Indices

**Problem Statement:** Write a Python program to find all starting indices of a substring in a given string.

**Code:**

```python
s = input("Enter the main string: ")
sub = input("Enter the substring: ")

indices = []

if sub:
    start = 0
    while True:
        index = s.find(sub, start)
        if index == -1:
            break
        indices.append(index)
        start = index + 1

print("Indices:", indices)
```

**Output:**

```text
Enter the main string: banana
Enter the substring: ana
Indices: [1, 3]
```

---

## Practical 08 – Cubes of Even Integers

**Problem Statement:** Write a Python program to display the cubes of even integers up to a given number.

**Code:**

```python
n = int(input("Enter the limit: "))

for i in range(2, n + 1, 2):
    print("Cube of", i, "=", i**3)
```

**Output:**

```text
Enter the limit: 10
Cube of 2 = 8
Cube of 4 = 64
Cube of 6 = 216
Cube of 8 = 512
Cube of 10 = 1000
```

---

## Practical 09 – File Handling

**Problem Statement:** Write a Python program to write data into a file and then read its contents.

**Code:**

```python
with open("sample.txt", "w") as file:
    file.write("Hello, Python!\n")
    file.write("File handling example.")

with open("sample.txt", "r") as file:
    content = file.read()

print("File contents:")
print(content)
```

**Output:**

```text
File contents:
Hello, Python!
File handling example.
```

---

## Practical 10 – Dictionary of Cubes

**Problem Statement:** Write a Python program to create a dictionary containing integers and their cubes.

**Code:**

```python
n = int(input("Enter the limit: "))

cubes = {i: i**3 for i in range(1, n + 1)}

print("Dictionary of cubes:", cubes)
```

**Output:**

```text
Enter the limit: 5
Dictionary of cubes: {1: 1, 2: 8, 3: 27, 4: 64, 5: 125}
```

---

## Practical 11 – Tuple Operations

**Problem Statement:** Write a Python program to perform basic tuple operations such as concatenation, repetition, indexing, and slicing.

**Code:**

```python
t1 = (1, 2, 3)
t2 = (4, 5, 6)

print("First tuple:", t1)
print("Second tuple:", t2)
print("Concatenation:", t1 + t2)
print("Repetition:", t1 * 2)
print("First element:", t1[0])
print("Slicing:", t1[1:])
print("Length:", len(t1))
```

**Output:**

```text
First tuple: (1, 2, 3)
Second tuple: (4, 5, 6)
Concatenation: (1, 2, 3, 4, 5, 6)
Repetition: (1, 2, 3, 1, 2, 3)
First element: 1
Slicing: (2, 3)
Length: 3
```

---

## Practical 12 – Employee Class and Object Counting

**Problem Statement:** Write a Python program to create an Employee class and count the number of objects created.

**Code:**

```python
class Employee:
    count = 0

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
        Employee.count += 1

    def display(self):
        print("Name:", self.name)
        print("Salary:", self.salary)


e1 = Employee("Aman", 25000)
e2 = Employee("Riya", 30000)

e1.display()
e2.display()

print("Total employees:", Employee.count)
```

**Output:**

```text
Name: Aman
Salary: 25000
Name: Riya
Salary: 30000
Total employees: 2
```

---

## Practical 13 – Class Point2D

**Problem Statement:** Write a Python program to define a Point2D class and display the coordinates of a point.

**Code:**

```python
class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print("Point:", (self.x, self.y))


p = Point2D(3, 4)
p.display()
```

**Output:**

```text
Point: (3, 4)
```

---

## Practical 14 – Inheritance: Class Point3D

**Problem Statement:** Write a Python program to demonstrate inheritance by creating a Point3D class derived from Point2D.

**Code:**

```python
class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print("2D Coordinates:", (self.x, self.y))


class Point3D(Point2D):
    def __init__(self, x, y, z):
        super().__init__(x, y)
        self.z = z

    def display(self):
        print("3D Coordinates:", (self.x, self.y, self.z))


p = Point3D(2, 3, 4)
p.display()
```

**Output:**

```text
3
