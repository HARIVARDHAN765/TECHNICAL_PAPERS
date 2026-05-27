# SOLID Principles in Python

## Introduction

SOLID is a group of five important design principles used in Object-Oriented Programming (OOP).

These principles help developers write clean, understandable, reusable, and maintainable code.

SOLID principles make programs:

- Easier to manage
- Easier to update
- Easier to test
- More reusable

The word SOLID stands for:

- S - Single Responsibility Principle
- O - Open Closed Principle
- L - Liskov Substitution Principle
- I - Interface Segregation Principle
- D - Dependency Inversion Principle

---

# 1. Single Responsibility Principle (SRP)

This principle says that a class should have only one responsibility or one job.

## Bad Example

```python
class Report:

    def create_report(self):
        print("Creating Report")

    def save_report(self):
        print("Saving Report")
```

Here, the class is doing two jobs:

- Creating the report
- Saving the report

## Good Example

```python
class Report:

    def create_report(self):
        print("Creating Report")


class SaveReport:

    def save_report(self):
        print("Saving Report")
```

Now each class has only one responsibility.

---

# 2. Open Closed Principle (OCP)

This principle says software should be open for extension but closed for modification.

It means we should add new features without changing old code.

## Example

```python
class Bird:

    def sound(self):
        pass


class Sparrow(Bird):

    def sound(self):
        print("Chirp")


class Crow(Bird):

    def sound(self):
        print("Caw")
```

We can add new bird classes without changing existing classes.

---

# 3. Liskov Substitution Principle (LSP)

This principle says child classes should replace parent classes without causing problems.

## Example

```python
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
```

Here, the `Dog` object works correctly wherever an `Animal` object is expected.

---

# 4. Interface Segregation Principle (ISP)

This principle says a class should not be forced to use methods it does not need.

## Bad Example

```python
class Worker:

    def work(self):
        pass

    def eat(self):
        pass
```

A robot does not need the `eat()` method.

## Good Example

```python
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
```

Now classes use only the required methods.

---

# 5. Dependency Inversion Principle (DIP)

This principle says high-level classes should not depend directly on low-level classes.

Both should depend on abstraction.

## Bad Example

```python
class Keyboard:
    pass


class Computer:

    def __init__(self):
        self.keyboard = Keyboard()
```

Here, `Computer` directly depends on `Keyboard`.

## Good Example

```python
class Keyboard:
    pass


class Computer:

    def __init__(self, keyboard):
        self.keyboard = keyboard


k1 = Keyboard()

c1 = Computer(k1)
```

Now the dependency is passed from outside, making the code more flexible and reusable.

---

# Advantages of SOLID Principles

- Cleaner code
- Better readability
- Easier maintenance
- Better scalability
- Easier testing
- Reusable components

---

# Conclusion

SOLID principles are very important in software development. They help developers write flexible, maintainable, and reusable code.

Using SOLID principles improves software quality and makes applications easier to manage in large projects.

---

# References

1. Python Documentation  
2. Clean Code by Robert C. Martin  
3. Real Python Articles  
4. GeeksforGeeks OOP Articles  
5. W3Schools Python Tutorial