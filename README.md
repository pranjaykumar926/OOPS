# Object-Oriented Programming (OOP) in Python

## 🚀 Four Pillars of OOP
Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes. Python supports OOP with four key principles:

---

## 1️⃣ Encapsulation (🔒 Data Hiding)
Encapsulation is the concept of **restricting direct access to variables** and **allowing controlled access** via methods.

### **Example:**
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable (Encapsulation)

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance  # Controlled access

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # ✅ Output: 1500
print(account.__balance)  # ❌ Error (Encapsulation prevents direct access)
```
---

## 2️⃣ Inheritance (🔄 Code Reusability)
Inheritance allows a class (child) to **inherit attributes and methods** from another class (parent), promoting **code reuse**.

### **Example:**
```python
class Animal:
    def speak(self):
        return "I make a sound"

class Dog(Animal):  # 🐶 Dog inherits from Animal
    def speak(self):
        return "Bark! Bark!"

d = Dog()
print(d.speak())  # ✅ Output: "Bark! Bark!"
```
---

## 3️⃣ Polymorphism (🔁 Multiple Forms)
Polymorphism allows **methods to have the same name but different behavior** in different classes.

### **Example:**
```python
class Bird:
    def fly(self):
        return "Some birds can fly"

class Sparrow(Bird):
    def fly(self):
        return "Sparrow can fly"

class Ostrich(Bird):
    def fly(self):
        return "Ostrich cannot fly"  # Different behavior

birds = [Sparrow(), Ostrich()]
for bird in birds:
    print(bird.fly())  
# ✅ Output:
# "Sparrow can fly"
# "Ostrich cannot fly"
```
---

## 4️⃣ Abstraction (🎭 Hiding Implementation Details)
Abstraction **hides unnecessary details** and shows only the essential features.

### **Example:**
```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass  # Abstract method (must be implemented in subclass)

class Car(Vehicle):
    def start(self):
        return "Car engine started 🚗"

c = Car()
print(c.start())  # ✅ Output: "Car engine started 🚗"
```
🔹 **Key Point:** You **cannot** create an object of an **abstract class** (`Vehicle` in this case).

---

## 🎯 **Summary Table**
| **Pillar**        | **Description**                                  | **Example** |
|-------------------|----------------------------------------------|------------|
| **Encapsulation** | Hiding data, using private variables         | `self.__balance` |
| **Inheritance**   | Reusing code, child class inherits parent    | `class Dog(Animal)` |
| **Polymorphism**  | Same method, different behavior              | `def fly(self):` |
| **Abstraction**   | Hiding details, showing only necessary parts | `@abstractmethod` |

---

## 🔥 **Conclusion**
Object-Oriented Programming (OOP) in Python makes code **more reusable, scalable, and maintainable**. Mastering these four pillars will help you design **efficient and structured** programs!

📌 **Happy Coding! 🚀**

