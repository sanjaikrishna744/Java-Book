# 🧱 Classes & Objects in Java (Simple Explanation)

Java is an **Object-Oriented Programming (OOP)** language.  
Everything in Java is built using **classes** and **objects**.

---

# 🔷 What is a Class?

A **class** is a blueprint / design / template.

Example:
- Mobile blueprint → Class  
- Actual mobile → Object  

A class contains:
- Variables (properties)
- Methods (actions)

---

# 🔷 What is an Object?

An **object** is created from a class.  
It has:
- Its own data  
- Its own behavior  

Example:  
If `Car` is a class  
`myCar` is an object created from that class.

---

# 💻 Basic Example – Class & Object

```java
class Car {

    String brand = "BMW";
    int price = 5000000;

    void drive() {
        System.out.println("Car is driving...");
    }
}

public class Main {
    public static void main(String[] args) {

        Car myCar = new Car();  // creating object

        System.out.println(myCar.brand);
        System.out.println(myCar.price);
        myCar.drive();  // calling method
    }
}
```

---

## ✔ Output
```
BMW
5000000
Car is driving...
```

---

# 🧠 Explanation

### ✔ Class  
```
class Car { }
```
Blueprint for creating cars.

### ✔ Object  
```
Car myCar = new Car();
```
myCar = actual car created from blueprint.

### ✔ Access Variables  
```
myCar.brand
myCar.price
```

### ✔ Call Methods  
```
myCar.drive();
```

---

# 💻 Example 2 – Student Class

```java
class Student {

    String name;
    int age;

    void study() {
        System.out.println(name + " is studying.");
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();  // first object
        s1.name = "Arctic";
        s1.age = 20;

        Student s2 = new Student();  // second object
        s2.name = "Kavin";
        s2.age = 21;

        s1.study();
        s2.study();
    }
}
```

---

## ✔ Output
```
Arctic is studying.
Kavin is studying.
```

---

# ⭐ Key Points

- Class = blueprint  
- Object = created from class  
- One class → many objects  
- Objects have **properties** (variables) & **actions** (methods)  
- Access using dot operator `objectName.variable`  

---

# 🔥 Practice Tasks

### Task 1  
Create a `Mobile` class with:
- brand  
- price  
- method: `details()` to print both  

Create 2 objects and print details.

### Task 2  
Create a `BankAccount` class with:
- name  
- balance  
- deposit() method  
- withdraw() method

# 💻 Classes & Objects – Laptop Example

This example shows how to create a class with variables and use an **object** to store real data such as laptop name, processor, and price.

---

## 💻 Code Example

```java
public class Main {

    String name = "";
    String proc = "";
    int price = 0;

    public static void main(String args[]) {

        Main lap1 = new Main();   // creating object

        lap1.name = "Asus Vivobook";
        lap1.proc = "i7";
        lap1.price = 100000;

        System.out.println(lap1.name);
        System.out.println(lap1.proc);
        System.out.println(lap1.price);
    }
}
```

---

## 🧠 Explanation

### ✔ Class
`Main` acts like a **blueprint** for laptop objects.

Inside the class, we define:
- `name` → laptop name  
- `proc` → processor  
- `price` → laptop price  

### ✔ Object Creation
```java
Main lap1 = new Main();
```
`lap1` is an **object**, meaning a real laptop built from the class blueprint.

### ✔ Assigning Values
```java
lap1.name = "Asus Vivobook";
lap1.proc = "i7";
lap1.price = 100000;
```

### ✔ Printing Object Data  
Using dot notation:
```
lap1.name  
lap1.proc  
lap1.price  
```

---

## ✔ Sample Output
```
Asus Vivobook
i7
100000
```

---

# ⭐ Key Takeaways

- Class = template  
- Object = real instance  
- Dot operator used to access data  
- You can create many laptop objects from the same class  

---

# 🔥 Practice Task

Create 2 more objects:

### lap2  
- name: "HP Pavilion"  
- proc: "Ryzen 5"  
- price: 75000  

### lap3  
- name: "MacBook Air"  
- proc: "M1"  
- price: 95000  

Print all their details.

  

Test using 2 accounts.

