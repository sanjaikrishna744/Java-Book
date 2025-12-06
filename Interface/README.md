# 🔌 Interface in Java (Simple Explanation)

An **interface** is a blueprint that contains **only method declarations** (no body).

It tells the class **WHAT to do**,  
but the class decides **HOW to do**.

---

# ⭐ Why Use Interface?

✅ To achieve **100% abstraction**  
✅ To support **multiple inheritance**  
✅ To define common rules/standards  

Real life example:
- Charger rule (interface)
- Mobile brand decides implementation

---

# 🧩 Interface Rules

✔ Use `interface` keyword  
✔ Methods are **public & abstract by default**  
✔ Variables are **public static final by default**  
✔ Cannot create object of interface  
✔ Class uses `implements` keyword  

---

# 🧩 Syntax

```java
interface InterfaceName {
    void method1();
    void method2();
}
```

---

# 💻 Example 1 – Simple Interface

```java
interface Animal {
    void sound();   // abstract method
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {

        Dog d = new Dog();
        d.sound();
    }
}
```

### ✔ Output
```
Dog barks
```

---

# 💻 Example 2 – Real World: Payment Interface

```java
interface Payment {
    void pay();
}

class UPI implements Payment {
    public void pay() {
        System.out.println("Payment done using UPI");
    }
}

class Card implements Payment {
    public void pay() {
        System.out.println("Payment done using Card");
    }
}

public class Main {
    public static void main(String[] args) {

        Payment p1 = new UPI();
        Payment p2 = new Card();

        p1.pay();
        p2.pay();
    }
}
```

---

# ⭐ Multiple Inheritance using Interface

Java **does NOT support multiple inheritance using classes**,  
BUT it **supports multiple inheritance using interfaces** ✅

---

# 💻 Example 3 – Multiple Inheritance (Interface)

```java
interface Camera {
    void takePhoto();
}

interface Music {
    void playMusic();
}

class Smartphone implements Camera, Music {

    public void takePhoto() {
        System.out.println("Photo clicked");
    }

    public void playMusic() {
        System.out.println("Music playing");
    }
}

public class Main {
    public static void main(String[] args) {

        Smartphone s = new Smartphone();
        s.takePhoto();
        s.playMusic();
    }
}
```

---

# ⭐ Interface vs Abstract Class

| Feature | Interface | Abstract Class |
|------|----------|---------------|
| Methods | Only abstract (Java 7) | Abstract + normal |
| Variables | public static final | Any type |
| Multiple inheritance | ✅ Yes | ❌ No (classes) |
| Object creation | ❌ No | ❌ No |

---

# 🔥 Example 4 – Interface Variable Example

```java
interface College {
    String NAME = "ABC College";  // public static final
}

class Student implements College {
    void show() {
        System.out.println(NAME);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student();
        s.show();
    }
}
```

---

# ⭐ Key Takeaways

- Interface = rule book  
- Class must implement ALL methods  
- Supports multiple inheritance  
- Best for large applications & frameworks  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create interface `Bank` with method `interestRate()`.  
Implement it in `SBI` and `HDFC`.

### ✔ Task 2  
Create interfaces:
- Camera  
- GPS  
Create class `SmartCar` implementing both.

### ✔ Task 3  
Create interface `Shape` with method `area()`.  
Implement it in Circle, Square.

