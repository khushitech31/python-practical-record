Programming Using Python – Practical Record

A collection of Python programs for the B.Sc. (Hons.) Computer Science practical record. Each practical includes the problem statement, source code, sample output, and space for an output screenshot.

Student Details

Field| Details
Name| Khushi kumari
Course| B.Sc. (Hons.) Computer Science
Semester| I (First Semester)
Roll Number| 26570030
Subject| Programming Using Python
College| Ramanujan college, University of Delhi 

How to Run

1. Install Python 3 on your computer.
2. Save the program in a file with the ".py" extension.
3. Run the program using:

python filename.py

Contents

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

---

Practical 01 – Roots of a Quadratic Equation

Problem Statement: Write a program to find the roots of a quadratic equation (ax^2 + bx + c = 0). Use the discriminant to determine whether the roots are real, equal, or complex.

Program

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
        imag = math.sqrt(-d) / abs(2*a)
        print(f"Complex roots: {real} ± {imag}i")

Sample Output

Enter a: 1
Enter b: -5
Enter c: 6
Two distinct real roots: 3.0 and 2.0

Output Screenshot

Add your program's output screenshot here.

---

Practical 02 – Prime Numbers

Problem Statement: Write a program to check whether a given number is prime.

Program

n = int(input("Enter a number: "))

if n < 2:
    print("Not a prime number")
else:
    prime = True

    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            prime = False
            break

    if prime:
        print(n, "is a prime number")
    else:
        print(n, "is not a prime number")

Sample Output

Enter a number: 17
17 is a prime number

Output Screenshot

Add your program's output screenshot here.

---

Practical 03 – Star Pyramids

Problem Statement: Write a program to print a pyramid pattern using stars.

Program

n = int(input("Enter the number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)

Sample Output

Enter the number of rows: 5
    *
   * *
  * * *
 * * * *
* * * * *

Output Screenshot

Add your program's output screenshot here.

---

Practical 04 – Character Classification

Problem Statement: Write a program to classify a character as a vowel, consonant, digit, whitespace, or special character.

Program

ch = input("Enter a character: ")

if len(ch) != 1:
    print("Please enter exactly one character")
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

Sample Output

Enter a character: A
Vowel

Output Screenshot

Add your program's output screenshot here.

---

Practical 05 – String Operations

Problem Statement: Write a program to perform common string operations such as finding length, converting case, reversing a string, and checking a palindrome.

Program

s = input("Enter a string: ")

print("Length:", len(s))
print("Uppercase:", s.upper())
print("Lowercase:", s.lower())
print("Reversed:", s[::-1])

if s.lower() == s[::-1].lower():
    print("Palindrome")
else:
    print("Not a palindrome")

Sample Output

Enter a string: Madam
Length: 5
Uppercase: MADAM
Lowercase: madam
Reversed: madaM
Palindrome

Output Screenshot

Add your program's output screenshot here.

---

Practical 06 – Swap Prefixes of Two Strings

Problem Statement: Write a program to swap the first characters of two strings.

Program

s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if not s1 or not s2:
    print("Both strings must be non-empty")
else:
    result1 = s2[0] + s1[1:]
    result2 = s1[0] + s2[1:]

    print("First string:", result1)
    print("Second string:", result2)

Sample Output

Enter first string: abc
Enter second string: xyz
First string: xbc
Second string: ayz

Output Screenshot

Add your program's output screenshot here.

---

Practical 07 – Substring Indices

Problem Statement: Write a program to find the starting indices of a substring in a string.

Program

s = input("Enter the main string: ")
sub = input("Enter the substring: ")

if not sub:
    print("Substring cannot be empty")
else:
    start = 0
    found = False

    while True:
        index = s.find(sub, start)

        if index == -1:
            break

        print("Found at index:", index)
        found = True
        start = index + 1

    if not found:
        print("Substring not found")

Sample Output

Enter the main string: banana
Enter the substring: ana
Found at index: 1
Found at index: 3

Output Screenshot

Add your program's output screenshot here.

---

Practical 08 – Cubes of Even Integers

Problem Statement: Write a program to print the cubes of even integers within a given range.

Program

n = int(input("Enter the upper limit: "))

for i in range(2, n + 1, 2):
    print("Cube of", i, "=", i**3)

Sample Output

Enter the upper limit: 10
Cube of 2 = 8
Cube of 4 = 64
Cube of 6 = 216
Cube of 8 = 512
Cube of 10 = 1000

Output Screenshot

Add your program's output screenshot here.

---

Practical 09 – File Handling

Problem Statement: Write a program to create a text file, write data into it, and read the contents.

Program

filename = "sample.txt"

with open(filename, "w") as file:
    file.write("Hello, Python!\n")
    file.write("File handling practical.")

with open(filename, "r") as file:
    content = file.read()

print("File contents:")
print(content)

Sample Output

File contents:
Hello, Python!
File handling practical.

Output Screenshot

Add your program's output screenshot here.

---

Practical 10 – Dictionary of Cubes

Problem Statement: Write a program to create a dictionary containing numbers and their cubes.

Program

n = int(input("Enter the number of elements: "))

cubes = {i: i**3 for i in range(1, n + 1)}

print("Dictionary of cubes:")
print(cubes)

Sample Output

Enter the number of elements: 5
Dictionary of cubes:
{1: 1, 2: 8, 3: 27, 4: 64, 5: 125}

Output Screenshot

Add your program's output screenshot here.

---

Practical 11 – Tuple Operations

Problem Statement: Write a program to perform basic tuple operations.

Program

t = (10, 20, 30, 40, 50)

print("Tuple:", t)
print("First element:", t[0])
print("Last element:", t[-1])
print("Length:", len(t))
print("Sliced tuple:", t[1:4])
print("Maximum:", max(t))
print("Minimum:", min(t))
print("Sum:", sum(t))

Sample Output

Tuple: (10, 20, 30, 40, 50)
First element: 10
Last element: 50
Length: 5
Sliced tuple: (20, 30, 40)
Maximum: 50
Minimum: 10
Sum: 150

Output Screenshot

Add your program's output screenshot here.

---

Practical 12 – Employee Class and Object Counting

Problem Statement: Create an Employee class and count the number of objects created.

Program

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

Sample Output

Name: Aman
Salary: 25000
Name: Riya
Salary: 30000
Total employees: 2

Output Screenshot

Add your program's output screenshot here.

---

Practical 13 – Class Point2D

Problem Statement: Create a Point2D class to represent a point in two-dimensional space and display its coordinates.

Program

class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print(f"Point: ({self.x}, {self.y})")


p = Point2D(3, 4)
p.display()

Sample Output

Point: (3, 4)

Output Screenshot

Add your program's output screenshot here.

---

Practical 14 – Inheritance: Class Point3D

Problem Statement: Create a Point3D class that inherits from Point2D and adds a third coordinate, z.

Program

class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print(f"Point: ({self.x}, {self.y})")


class Point3D(Point2D):
    def __init__(self, x, y, z):
        super().__init__(x, y)
        self.z = z

    def display(self):
        print(f"Point: ({self.x}, {self.y}, {self.z})")


p = Point3D(3, 4, 5)
p.display()

Sample Output

Point: (3, 4, 5)

Output Screenshot

Add your program's output screenshot here.

---

Practical 15 – Exception Handling for a Name

Problem Statement: Write a program to accept a name and handle invalid input using exception handling.

Program

try:
    name = input("Enter your name: ").strip()

    if not name:
        raise ValueError("Name cannot be empty")

    if not name.replace(" ", "").isalpha():
        raise ValueError("Name must contain only letters and spaces")

    print("Hello,", name)

except ValueError as e:
    print("Invalid input:", e)

Sample Output

Enter your name: Sanskriti
Hello, Sanskriti

Output Screenshot

Add your program's output screenshot here.

---

Conclusion

This practical record covers fundamental Python concepts, including conditional statements, loops, strings, tuples, dictionaries, file handling, classes, inheritance, and exception handling.

Each program can be executed independently using Python 3. Sample outputs are included for reference.

Note: Verify the programs and sample outputs against your college's practical syllabus before submission.
