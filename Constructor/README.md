# 🏗️ Constructor in Java (Simple Explanation)

A **constructor** is a special method that is called **automatically** when an object is created.

It is mainly used to:
- Initialize variables  
- Set default values  
- Allocate resources  

---

# 🧩 Rules of Constructor

✔ Constructor name = class name  
✔ No return type (not even void)  
✔ Called automatically when object is created  

---

# 💻 Example 1 – Simple Constructor

```java
class Laptop {

    Laptop() {     // constructor
        System.out.println("Laptop object created");
    }
}

public class Main {
    public static void main(String[] args) {

        Laptop l1 = new Laptop();   // calls constructor
        Laptop l2 = new Laptop();   // calls again
    }
}
```

### ✔ Output
```
Laptop object created
Laptop object created
```

---

# 💻 Example 2 – Constructor Initializing Variables

```java
class Student {

    String name;
    int age;

    Student() {        // constructor
        name = "Arctic";
        age = 20;
    }
}

public class Main {
    public static void main(String[] args) {

        Student s = new Student();

        System.out.println(s.name);
        System.out.println(s.age);
    }
}
```

---

# 💻 Example 3 – Real-World Example

```java
class Car {

    String brand;
    int price;

    Car() {      // constructor
        brand = "BMW";
        price = 5000000;
    }
}

public class Main {
    public static void main(String[] args) {

        Car c = new Car();

        System.out.println(c.brand);
        System.out.println(c.price);
    }
}
```

---

# ⭐ Summary

- Constructor runs **automatically**  
- Used to initialize values  
- No return type  
- Same name as the class  
- Gets called every time an object is created  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create a class `Mobile` with a constructor that sets:
- brand  
- model  
- price  

Print the values.

### ✔ Task 2  
Create a class `Employee` with constructor setting:
- name  
- salary  
Print a message using the values.

### ✔ Task 3  
Create 3 objects using the same constructor and print their values.

