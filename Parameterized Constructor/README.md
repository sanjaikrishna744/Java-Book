# 🎯 Parameterized Constructor in Java (Simple Explanation)

A **Parameterized Constructor** is a constructor that accepts **arguments/inputs**.

We use it when:
- We want to initialize object values at the time of creation  
- Each object should have **different values**

---

# 🧩 Syntax

```java
ClassName(type param1, type param2) {
    // assign values
}
```

Example:
```java
Student(String name, int age) {
    this.name = name;
    this.age = age;
}
```

---

# 💻 Example 1 – Simple Parameterized Constructor

```java
class Student {

    String name;
    int age;

    Student(String n, int a) {   // parameterized constructor
        name = n;
        age = a;
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Arctic", 20);
        Student s2 = new Student("Kavin", 21);

        System.out.println(s1.name + " " + s1.age);
        System.out.println(s2.name + " " + s2.age);
    }
}
```

---

# 💻 Example 2 – Laptop Details Using Parameterized Constructor

```java
class Laptop {

    String brand;
    String processor;
    int price;

    Laptop(String b, String p, int pr) {
        brand = b;
        processor = p;
        price = pr;
    }
}

public class Main {
    public static void main(String[] args) {

        Laptop l1 = new Laptop("Asus", "i7", 100000);
        Laptop l2 = new Laptop("HP", "Ryzen 5", 65000);

        System.out.println(l1.brand + " - " + l1.processor + " - " + l1.price);
        System.out.println(l2.brand + " - " + l2.processor + " - " + l2.price);
    }
}
```

---

# 💻 Example 3 – Constructor With Calculations

```java
class Marks {

    int total;

    Marks(int m1, int m2, int m3) {
        total = m1 + m2 + m3;
    }
}

public class Main {
    public static void main(String[] args) {

        Marks m = new Marks(80, 90, 75);
        System.out.println("Total Marks = " + m.total);
    }
}
```

---

# ⭐ Why Use Parameterized Constructors?

- Set different values for each object  
- Avoid using many `setter` methods  
- Cleaner initialization  
- More control over object creation  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create `Mobile` class with constructor:
- brand  
- price  

Create 3 mobiles and print details.

### ✔ Task 2  
Create `Employee` class with constructor:
- name  
- salary  

Print annual salary (salary × 12).

### ✔ Task 3  
Create `Area` class with constructor:
- length  
- breadth  
Print area of rectangle.

