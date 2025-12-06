# ⚡ `static` Keyword in Java (Simple Explanation)

`static` keyword is used to create **class-level** members.

✔ Belongs to the **class**, not objects  
✔ Shared by **all objects**  
✔ Memory created only **once**

You can access static members **without creating an object**.

---

# ⭐ When to Use `static`?

- When a variable should be **common** for all objects  
- When a method should run **without object creation**  
- Utility methods (like Math functions)  
- Memory-efficient programs  

---

# 🧩 Types of static members

| Type | Usage |
|------|--------|
| static variable | Shared value for all objects |
| static method | Can be called without object |
| static block | Runs once when class loads |
| static class | Inner classes only |

---

# 💻 Example 1 – Static Variable (Shared by All Objects)

```java
class Student {
    static String college = "ABC College";  // shared variable
    String name;

    Student(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Arctic");
        Student s2 = new Student("Kavin");

        System.out.println(s1.name + " - " + Student.college);
        System.out.println(s2.name + " - " + Student.college);
    }
}
```

### ✔ Output
```
Arctic - ABC College
Kavin - ABC College
```

---

# 💻 Example 2 – Static Method (No Object Needed)

```java
class MathHelper {

    static int square(int x) {
        return x * x;
    }
}

public class Main {
    public static void main(String[] args) {

        System.out.println(MathHelper.square(5));  // call without object
    }
}
```

### ✔ Output
```
25
```

---

# 💻 Example 3 – Static Block (Runs Once Only)

```java
class Demo {

    static {
        System.out.println("Static block executed");
    }
}

public class Main {
    public static void main(String[] args) {

        Demo d = new Demo();  // object creation
    }
}
```

### ✔ Output
```
Static block executed
```

---

# 💻 Example 4 – Static + Normal Members Difference

```java
class Counter {

    static int count = 0;   // shared
    int num = 0;            // object-only

    Counter() {
        count++;
        num++;
        System.out.println("Static count = " + count);
        System.out.println("Normal num = " + num);
    }
}

public class Main {
    public static void main(String[] args) {

        Counter c1 = new Counter();
        Counter c2 = new Counter();
        Counter c3 = new Counter();
    }
}
```

### ✔ Output (important concept)
```
Static count = 1
Normal num = 1

Static count = 2
Normal num = 1

Static count = 3
Normal num = 1
```

---

# ⭐ Key Points to Remember

- `static` members belong to **class**, not objects  
- Access static methods using the class name  
- Cannot use **this** inside static methods  
- Static block runs once when class loads  
- Great for **constants**, **utility methods**, **counters**

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create class `Bank` with static variable `bankName`.  
Create 3 objects and print same bank name.

### ✔ Task 2  
Create static method `add(int a, int b)` returning sum.  
Call it without object.

### ✔ Task 3  
Create class `IDGenerator` with:
- static int nextId = 1  
- Constructor increases id  
Print IDs for 3 objects.


# ✅ `final` Keyword in Java (Simple Explanation)

The **final keyword** is used to say **“this cannot be changed”**.

`final` can be used with:
1. Variables  
2. Methods  
3. Classes  

---

# ⭐ 1. `final` Variable (Constant)

A `final` variable’s value **cannot be changed** once initialized.

```java
class Demo {
    final int speed = 120;

    void show() {
        // speed = 150; // ❌ Error
        System.out.println(speed);
    }
}
```

✅ Value is fixed  
✅ Used for constants  

---

# ⭐ 2. `final` Method (Cannot be Overridden)

When a method is marked `final`,  
**child class cannot override it**.

```java
class Parent {
    final void display() {
        System.out.println("Parent display method");
    }
}

class Child extends Parent {
    // void display() { } ❌ Error
}
```

✅ Ensures method behavior stays same  

---

# ⭐ 3. `final` Class (Cannot be Inherited)

A `final` class **cannot be extended** by any class.

```java
final class Vehicle {
    void run() {
        System.out.println("Vehicle running");
    }
}

// class Car extends Vehicle { } ❌ Error
```

✅ Used for security  
✅ Prevents inheritance  

---

# 💻 Example – All `final` Types Together

```java
final class Bank {

    final double interestRate = 7.5;

    final void showRate() {
        System.out.println("Interest Rate: " + interestRate);
    }
}

public class Main {
    public static void main(String[] args) {

        Bank b = new Bank();
        b.showRate();
    }
}
```

---

# ⭐ Summary Table

| Usage | Meaning |
|------|---------|
| final variable | Value cannot change |
| final method | Cannot override |
| final class | Cannot inherit |

---

# ⚠ Important Notes

- `final` variable must be initialized once  
- Can be initialized in:
  - declaration  
  - constructor  
- Final methods are inherited but NOT overridden  
- Final class methods can be overridden ❌ (since class itself can't be inherited)

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create a final variable `PI = 3.14` and try changing it.

### ✔ Task 2  
Create parent class with final method `rules()`.  
Try overriding in child class and observe error.

### ✔ Task 3  
Create a final class `SecuritySystem`.  
Try extending it and see compiler error.


