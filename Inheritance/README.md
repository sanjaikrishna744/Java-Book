# 🧬 Inheritance in Java (Simple Explanation)

**Inheritance** allows one class to **use properties and methods of another class**.  
It provides *reusability* and reduces duplicate code.

---

# 🔹 Parent Class (Super Class)
The class whose features are inherited.

# 🔹 Child Class (Sub Class)
The class that receives properties from parent.

---

# ⭐ Syntax

```java
class Parent {
    // parent properties & methods
}

class Child extends Parent {
    // child properties & methods
}
```

`extends` keyword → used for inheritance.

---

# 🔥 SINGLE INHERITANCE

Single inheritance means:
- **ONE parent class**
- **ONE child class**

```
Parent
   ↑
 Child
```

---

# 💻 Example 1 – Simple Single Inheritance

```java
class Animal {

    void eat() {
        System.out.println("Animal is eating...");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog is barking...");
    }
}

public class Main {
    public static void main(String[] args) {

        Dog d = new Dog();

        d.eat();   // from parent class
        d.bark();  // from Dog class
    }
}
```

## ✔ Output
```
Animal is eating...
Dog is barking...
```

---

# 💻 Example 2 – Real World: Employee → Programmer

```java
class Employee {

    String name = "Arctic";
    int salary = 30000;

    void work() {
        System.out.println("Employee working...");
    }
}

class Programmer extends Employee {

    int bonus = 15000;

    void code() {
        System.out.println("Programmer coding...");
    }
}

public class Main {
    public static void main(String[] args) {

        Programmer p = new Programmer();

        System.out.println(p.name);
        System.out.println(p.salary);
        System.out.println(p.bonus);

        p.work();  // parent method
        p.code();  // child method
    }
}
```

---

# 💡 What Child Class Gets?

From Parent Class, Child gets:
- variables  
- methods  
- constructors *indirectly*  

(Parent constructor runs automatically.)

---

# ⭐ Why Use Inheritance?

- Code reusability  
- Avoid duplicate code  
- Easy to maintain  
- Builds OOP structure  

---

# ⚠ What Child Cannot Inherit?

Child CANNOT inherit:
- private members  
- constructors directly  
- methods marked final  

---

# 🔥 Example 3 – Using this + super in inheritance (simple)

```java
class Car {
    String brand = "BMW";
}

class SportsCar extends Car {
    int speed = 300;
}

public class Main {
    public static void main(String[] args) {

        SportsCar s = new SportsCar();

        System.out.println(s.brand);  // inherited
        System.out.println(s.speed);  // child property
    }
}
```

---

# 🎯 Practice Tasks

### ✔ Task 1  
Create class **Person** with variables name & age.  
Create class **Student** extends Person with variable department.  
Print all details.

### ✔ Task 2  
Create class **Vehicle** with method start().  
Create class **Bike** extends Vehicle with method ride().  
Call both methods.

### ✔ Task 3  
Create class **Animal** → method sleep().  
Create class **Cat** extends Animal → method meow().  
Call both from main().

