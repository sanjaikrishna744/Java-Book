# 🔄 Constructor Overloading in Java (Simple Explanation)

**Constructor Overloading** means a class can have **multiple constructors**  
with the **same name** but **different parameters**.

Just like method overloading, but here it applies to constructors.

---

# 🧩 Why Constructor Overloading?

- To create objects in **different ways**  
- To allow **default values + custom values**  
- To make object creation flexible  

Example:
```
Student()
Student(String name)
Student(String name, int age)
```

---

# 💻 Example 1 – Basic Constructor Overloading

```java
class Student {

    String name;
    int age;

    Student() {    // default constructor
        name = "Unknown";
        age = 0;
    }

    Student(String n) {   // constructor with one parameter
        name = n;
        age = 18;
    }

    Student(String n, int a) {   // constructor with two parameters
        name = n;
        age = a;
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();
        Student s2 = new Student("Arctic");
        Student s3 = new Student("Kavin", 21);

        System.out.println(s1.name + " " + s1.age);
        System.out.println(s2.name + " " + s2.age);
        System.out.println(s3.name + " " + s3.age);
    }
}
```

---

# 💻 Example 2 – Laptop Constructor Overloading

```java
class Laptop {

    String brand;
    String processor;
    int price;

    Laptop() {
        brand = "Unknown";
        processor = "Not specified";
        price = 0;
    }

    Laptop(String b) {
        brand = b;
        processor = "i5";
        price = 50000;
    }

    Laptop(String b, String p, int pr) {
        brand = b;
        processor = p;
        price = pr;
    }
}

public class Main {
    public static void main(String[] args) {

        Laptop l1 = new Laptop();
        Laptop l2 = new Laptop("Asus");
        Laptop l3 = new Laptop("HP", "Ryzen 5", 65000);

        System.out.println(l1.brand + " - " + l1.processor + " - " + l1.price);
        System.out.println(l2.brand + " - " + l2.processor + " - " + l2.price);
        System.out.println(l3.brand + " - " + l3.processor + " - " + l3.price);
    }
}
```

---

# 💻 Example 3 – Real World (Rectangle Area)

```java
class Rectangle {

    int length;
    int breadth;

    Rectangle() {
        length = 1;
        breadth = 1;
    }

    Rectangle(int side) {
        length = side;
        breadth = side;
    }

    Rectangle(int l, int b) {
        length = l;
        breadth = b;
    }
}

public class Main {
    public static void main(String[] args) {

        Rectangle r1 = new Rectangle();
        Rectangle r2 = new Rectangle(5);
        Rectangle r3 = new Rectangle(4, 6);

        System.out.println(r1.length + " x " + r1.breadth);
        System.out.println(r2.length + " x " + r2.breadth);
        System.out.println(r3.length + " x " + r3.breadth);
    }
}
```

---

# ⭐ Key Points

- Constructor name = class name  
- Parameter list must be different  
- Overloading gives flexibility  
- Helps initialize objects in multiple ways  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create class `Mobile` with overloaded constructors:
- No parameters  
- brand  
- brand + price  

### ✔ Task 2  
Create class `Car` with:
- Default constructor  
- constructor with `brand`  
- constructor with `brand`, `model`, `price`

### ✔ Task 3  
Create class `BankAccount` with:
- name  
- balance  
- Overloaded constructors to set values in different ways  

