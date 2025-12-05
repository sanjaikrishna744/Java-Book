# 🔗 Hybrid Inheritance in Java (Simple Explanation)

**Hybrid Inheritance** = Combination of two or more types of inheritance.

Example:
- Single Inheritance  
- Multilevel Inheritance  
- Hierarchical Inheritance  

All mixed together → **Hybrid Inheritance**

---

# ⚠ Important Note  
Java **does NOT support Hybrid Inheritance using classes**,  
because it leads to **multiple inheritance issues** (Diamond Problem).

👉 But with **interfaces**, hybrid inheritance is possible.

---

# ⭐ Example Structure

```
      Interface A
         |
      Class B
     /      \
Class C    Class D
```

This mixes:
- Hierarchical Inheritance  
- Single Inheritance  
- Interface-based multiple inheritance  

---

# 💻 Example 1 – Hybrid Using Interfaces + Classes

```java
interface A {
    void show();
}

class B implements A {
    public void show() {
        System.out.println("Inside A - implemented in B");
    }
}

class C extends B {
    void msgC() {
        System.out.println("Class C message");
    }
}

class D extends B {
    void msgD() {
        System.out.println("Class D message");
    }
}

public class Main {
    public static void main(String[] args) {

        C obj1 = new C();
        D obj2 = new D();

        obj1.show();   // from interface A through B
        obj1.msgC();   // own method

        obj2.show();   // from interface A through B
        obj2.msgD();   // own method
    }
}
```

---

# ✔ Output
```
Inside A - implemented in B
Class C message
Inside A - implemented in B
Class D message
```

---

# 💻 Example 2 – Real World Hybrid:  
**Device → Laptop → Gaming Laptop**  
**Device → Mobile**

→ This mixes *hierarchical + multilevel* inheritance.

```java
class Device {
    void powerOn() {
        System.out.println("Device Power On");
    }
}

class Laptop extends Device {
    void features() {
        System.out.println("Laptop Features");
    }
}

class GamingLaptop extends Laptop {
    void rgb() {
        System.out.println("RGB Lights ON");
    }
}

class Mobile extends Device {
    void call() {
        System.out.println("Calling...");
    }
}

public class Main {
    public static void main(String[] args) {

        GamingLaptop g = new GamingLaptop();
        g.powerOn();
        g.features();
        g.rgb();

        Mobile m = new Mobile();
        m.powerOn();
        m.call();
    }
}
```

---

# ⭐ Why Use Hybrid Inheritance?

- Mix different inheritance styles  
- Avoid duplicate code  
- Build large systems with structured class hierarchy  
- Achieve multiple inheritance safely using **interfaces**

---

# ⚠ Java Restrictions

- Java **does not allow multiple inheritance** using classes.  
- But using **interfaces**, hybrid inheritance is allowed.  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create interface `Shape` with method draw().  
Create class `Circle` and `Square` implementing Shape.  
Create new class `ColoredCircle` extending Circle.

### ✔ Task 2  
Create hierarchy:  
```
Animal (super)
   |
 Pet (extends Animal)
  /    \
Dog    Cat
```
Add methods and print output.

### ✔ Task 3  
Use interface + class mix:
- Interface `Vehicle`  
- Class `Car` implements it  
- Class `ElectricCar` extends Car  

