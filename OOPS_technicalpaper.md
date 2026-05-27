# OOPs in Python

## Introduction

* OOP stands for Object Oriented Programming.
* It is a way of writing programs using classes and objects.
* OOP helps us write clean, reusable, and organized code.
* Python supports OOP concepts and they are used in many real-world applications.

# Class and Object

* A class is like a blueprint.
* An object is created from the class.

Example:

class Student:
    def __init__(self, name, age):

        self.name = name
        self.age = age

s1 = Student("Hari", 25)
print(s1.name)
print(s1.age)

Output:
Hari
25

# Constructor

A constructor is a special method that runs automatically when an object is created.
In Python, constructor is written as:

Example:

class Car:
    def __init__(self, brand):
         
         self.brand = brand


c1 = Car("BMW")
print(c1.brand)

# Encapsulation
 
Encapsulation means keeping data and methods inside one class.
It also helps protect data.

Example:

class Bank:
    def __init__(self):
        
        self.__balance = 1000

# Inheritance

Inheritance allows one class to use features of another class.

Example:

class Animal:
    def sound(self):
        
        print("Animal sound")
class Dog(Animal):
    
    pass


d1 = Dog()
d1.sound()

Output:
Animal sound

Dog class uses method from Animal class.

# Polymorphism

Polymorphism means one method name can work in different ways.

Example:

class Dog:
    def sound(self):
        
        print("Bark")


class Cat:
    def sound(self):
        
        print("Meow")

animals = [Dog(), Cat()]

for animal in animals:
    
    animal.sound()

Output:

Bark
Meow

# Abstraction

Abstraction means hiding internal details and showing only important features.

Example:

from abc import ABC, abstractmethod

class Vehicle(ABC):
    
    @abstractmethod
    def start(self):
        
        pass

class Car(Vehicle):
    def start(self):
        
        print("Car Started")

c1 = Car()
c1.start()

# Advantages of OOP

- Code can be reused
- Easy to understand
- Easy to maintain
- Reduces repeated code