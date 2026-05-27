# Python Self Review

## Array Methods

Python lists are used like arrays.
Common methods:
- append()
- pop()
- insert()
- remove()
- sort()

Example: arr = [1, 2, 3]
               arr.append(4)
               print(arr)

## String Methods

Strings store text data.
Common methods:
- upper()
- lower()
- split()
- replace()
- strip()

Example:
text = "python"
print(text.upper())

## Objects and Object Oriented Programming

OOP means Object Oriented Programming.
Main concepts:
- Class
- Object
- Method
- Constructor

Example:
class Person:

    def __init__(self, name):
        self.name = name

p1 = Person("Hari")

print(p1.name)

## Decorators
Decorators are used to add extra functionality to functions.

Example:

def greet():
    print("Hello")

## virtualenv
virtualenv is used to create separate Python environments.

Create virtual environment:
python -m venv venv

Activate virtual environment:
source venv/bin/activate

## pip Package Manager

pip is used to install Python packages.

Install package:
pip install pygame
Check installed packages:
pip list

## PEP-8 Standards Summary

PEP-8 is the Python coding style guide.

Rules:
- Use proper indentation
- Use meaningful variable names
- Write readable code
- Add spaces properly
- Keep code clean

Example:
name = "Hari"
instead of:
name="Hari"