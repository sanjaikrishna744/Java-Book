# 🔗 Multiple Inheritance Using Interface in Java (Simple Explanation)

Java **does NOT support multiple inheritance using classes**  
(One child cannot extend multiple classes).

BUT ✅  
Java **supports multiple inheritance using interfaces**.

👉 A class can implement **multiple interfaces**.

---

# ❌ Multiple Inheritance Using Classes (Not Allowed)

```java
class A { }
class B { }

// class C extends A, B { }  ❌ ERROR
```

This causes **Diamond Problem**, so Java blocks it.

---

# ✅ Multiple Inheritance Using Interfaces (Allowed)

```java
interface A {
    void methodA();
}

interface B {
    void methodB();
}

class C implements A, B {

    public void methodA() {
        System.out.println("Method A implemented");
    }

    public void methodB() {
        System.out.println("Method B implemented");
    }
}

public class Main {
    public static void main(String[] args) {

        C obj = new C();
        obj.methodA();
        obj.methodB();
    }
}
```

---

## ✔ Output
```
Method A implemented
Method B implemented
```

---

# 🧠 How This Works?

- Interfaces only define **rules (no implementation)**  
- No confusion in method execution  
- Class `C` chooses HOW to implement methods  

✅ Diamond problem avoided

---

# 💻 Example 2 – Real World: Smartphone

```java
interface Camera {
    void takePhoto();
}

interface Music {
    void playMusic();
}

interface GPS {
    void navigate();
}

class Smartphone implements Camera, Music, GPS {

    public void takePhoto() {
        System.out.println("Photo captured");
    }

    public void playMusic() {
        System.out.println("Music playing");
    }

    public void navigate() {
        System.out.println("Navigation started");
    }
}

public class Main {
    public static void main(String[] args) {

        Smartphone s = new Smartphone();
        s.takePhoto();
        s.playMusic();
        s.navigate();
    }
}
```

---

# ⭐ Interface + Class Inheritance Combined

A class can:
- Extend **one class**
- Implement **multiple interfaces**

✅ This is very powerful.

```java
class Vehicle {
    void start() {
        System.out.println("Vehicle started");
    }
}

interface Electric {
    void charge();
}

interface Autonomous {
    void autoDrive();
}

class Tesla extends Vehicle implements Electric, Autonomous {

    public void charge() {
        System.out.println("Charging battery");
    }

    public void autoDrive() {
        System.out.println("Self driving mode ON");
    }
}

public class Main {
    public static void main(String[] args) {

        Tesla t = new Tesla();
        t.start();
        t.charge();
        t.autoDrive();
    }
}
```

---

# ⭐ Rules to Remember

✔ A class can `implements` multiple interfaces  
✔ Interface methods must be implemented  
✔ Use comma `,` between interfaces  
✔ Use `implements`, not `extends`  

---

# 🧠 Interface vs Class (Quick)

| Feature | Class | Interface |
|-------|------|-----------|
| Multiple inheritance | ❌ No | ✅ Yes |
| Method body | ✅ Yes | ❌ (Java 7) |
| Object creation | ✅ Yes | ❌ No |

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create interfaces `Printer` and `Scanner`.  
Create class `AllInOneMachine` implementing both.

### ✔ Task 2  
Create interfaces `Flyable` and `Swimmable`.  
Create class `Duck` implementing both.

### ✔ Task 3  
Create interface `Payment`.  
Implement it in:
- UPI  
- Card  
Create a common reference and call `pay()`.

