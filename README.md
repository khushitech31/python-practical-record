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
