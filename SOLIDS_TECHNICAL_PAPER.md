# SOLID Principles in Python

## Introduction

SOLID is a group of five important design principles used in Object Oriented Programming.
These principles help developers write clean, understandable, and maintainable code.

SOLID principles make programs:
- easier to manage
- easier to update
- easier to test
- reusable

The word SOLID stands for:

S - Single Responsibility Principle  
O - Open Closed Principle  
L - Liskov Substitution Principle  
I - Interface Segregation Principle  
D - Dependency Inversion Principle

# 1. Single Responsibility Principle (SRP)

This principle says that a class should have only one responsibility or one job.

Bad Example:

class Report:

    def create_report(self):

        print("Creating Report")

    def save_report(self):

        print("Saving Report")

Here, the class is doing two jobs:
- creating report
- saving report

Good Example:

class Report:

    def create_report(self):

        print("Creating Report")


class SaveReport:

    def save_report(self):

        print("Saving Report")

Now each class has only one responsibility.

--------------------------------------------------

# 2. Open Closed Principle (OCP)

This principle says software should be open for extension but closed for modification.

It means we should add new features without changing old code.

Example:

class Bird:

    def sound(self):

        pass


class Sparrow(Bird):

    def sound(self):

        print("Chirp")


class Crow(Bird):

    def sound(self):

        print("Caw")

We can add new bird classes without changing existing classes.

--------------------------------------------------

# 3. Liskov Substitution Principle (LSP)

This principle says child classes should be able to replace parent classes without causing problems.

Example:

class Animal:

    def sound(self):

        print("Animal Sound")


class Dog(Animal):

    def sound(self):

        print("Bark")


def make_sound(animal):

    animal.sound()


d1 = Dog()

make_sound(d1)

Here, Dog object works correctly wherever Animal object is expected.

# 4. Interface Segregation Principle (ISP)

This principle says a class should not be forced to use methods it does not need.

Bad Example:

class Worker:

    def work(self):

        pass

    def eat(self):

        pass

A robot does not need eat() method.

Good Example:

class Workable:

    def work(self):

        pass


class Eatable:

    def eat(self):

        pass


class Human(Workable, Eatable):

    pass


class Robot(Workable):

    pass

Now classes use only required methods.

--------------------------------------------------

# 5. Dependency Inversion Principle (DIP)

This principle says high-level classes should not depend directly on low-level classes.
Both should depend on abstraction.

Bad Example:

class Keyboard:

    pass


class Computer:

    def __init__(self):

        self.keyboard = Keyboard()

Computer directly depends on Keyboard.

Good Example:

class Keyboard:

    pass


class Computer:

    def __init__(self, keyboard):

        self.keyboard = keyboard


k1 = Keyboard()

c1 = Computer(k1)


