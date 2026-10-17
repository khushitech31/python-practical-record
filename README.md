Programming Using Python - Practical Record

Student Details

Field| Details
Name| Khushi Kumari
Course| B.Sc. (Hons.) Computer Science
Semester| I (First Semester)
Roll Number| 26570030
Subject| Programming Using Python
College| Ramanujan College, University of Delhi

Practical 01 - Roots of a Quadratic Equation

Code

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

Output

Enter a: 1
Enter b: -5
Enter c: 6
Two distinct real roots: 3.0 and 2.0

Practical 02 - Prime Numbers

Code

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

Output

Enter a number: 17
17 is a prime number

Practical 03 - Star Pyramids

Code

n = int(input("Enter the number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)

Output

Enter the number of rows: 5
    *
   * *
  * * *
 * * * *
* * * * *

Practical 04 - Character Classification

Code

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

Output

Enter a character: A
Vowel

Practical 05 - String Operations

Code

s = input("Enter a string: ")

print("Length:", len(s))
print("Uppercase:", s.upper())
print("Lowercase:", s.lower())
print("Reversed:", s[::-1])

if s.lower() == s[::-1].lower():
    print("Palindrome")
else:
    print("Not a palindrome")

Output

Enter a string: Madam
Length: 5
Uppercase: MADAM
Lowercase: madam
Reversed: madaM
Palindrome

Practical 06 - Swap Prefixes of Two Strings

Code

s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if not s1 or not s2:
    print("Both strings must be non-empty")
else:
    result1 = s2[0] + s1[1:]
    result2 = s1[0] + s2[1:]

    print("First string:", result1)
    print("Second string:", result2)

Output

Enter first string: abc
Enter second string: xyz
First string: xbc
Second string: ayz

Practical 07 - Substring Indices

Code

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

Output

Enter the main string: banana
Enter the substring: ana
Found at index: 1
Found at index: 3

Practical 08 - Cubes of Even Integers

Code

n = int(input("Enter the upper limit: "))

for i in range(2, n + 1, 2):
    print("Cube of", i, "=", i**3)

Output

Enter the upper limit: 10
Cube of 2 = 8
Cube of 4 = 64
Cube of 6 = 216
Cube of 8 = 512
Cube of 10 = 1000

Practical 09 - File Handling

Code

filename = "sample.txt"

with open(filename, "w") as file:
    file.write("Hello, Python!\n")
    file.write("File handling practical.")

with open(filename, "r") as file:
    content = file.read()

print("File contents:")
print(content)

Output

File contents:
Hello, Python!
File handling practical.

Practical 10 - Dictionary of Cubes

Code

n = int(input("Enter the number of elements: "))

cubes = {i: i**3 for i in range(1, n + 1)}

print("Dictionary of cubes:")
print(cubes)

Output

Enter the number of elements: 5
Dictionary of cubes:
{1: 1, 2: 8, 3: 27, 4: 64, 5: 125}

Practical 11 - Tuple Operations

Code

t = (10, 20, 30, 40, 50)

print("Tuple:", t)
print("First element:", t[0])
print("Last element:", t[-1])
print("Length:", len(t))
print("Sliced tuple:", t[1:4])
print("Maximum:", max(t))
print("Minimum:", min(t))
print("Sum:", sum(t))

Output

Tuple: (10, 20, 30, 40, 50)
First element: 10
Last element: 50
Length: 5
Sliced tuple: (20, 30, 40)
Maximum: 50
Minimum: 10
Sum: 150

Practical 12 - Employee Class and Object Counting

Code

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

Output

Name: Aman
Salary: 25000
Name: Riya
Salary: 30000
Total employees: 2

Practical 13 - Class Point2D

Code

class Point2D:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def display(self):
        print(f"Point: ({self.x}, {self.y})")


p = Point2D(3, 4)
p.display()

Output

Point: (3, 4)

Practical 14 - Inheritance: Class Point3D

Code

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

Output

Point: (3, 4, 5)

Practical 15 - Exception Handling for a Name

Code

try:
    name = input("Enter your name: ").strip()

    if not name:
        raise ValueError("Name cannot be empty")

    if not name.replace(" ", "").isalpha():
        raise ValueError("Name must contain only letters and spaces")

    print("Hello,", name)

except ValueError as e:
    print("Invalid input:", e)

Output

Enter your name: Khushi Kumari
Hello, Khushi Kumari
