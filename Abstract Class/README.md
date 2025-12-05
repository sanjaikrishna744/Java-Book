# 🧩 Abstract Class & Abstract Methods in Java

An **abstract class** is a class that **cannot be instantiated** (cannot create objects directly).  
It is used as a **base** for other classes.

An **abstract method** is a method that **has no body** and must be overridden by child classes.

---

# ⭐ Abstract Class Rules

✔ Use `abstract` keyword  
✔ Cannot create objects of abstract class  
✔ Can have **both abstract and normal methods**  
✔ Child class **must override** abstract methods  

---

# 🧩 Abstract Method Rules

- Declared using `abstract` keyword  
- Does **not** have a body  
- Ends with semicolon `;`  
- Must be overridden in subclass  

---

# 💻 Example 1 – Simple Abstract Class

```java
abstract class Animal {

    abstract void sound();  // abstract method

    void sleep() {          // normal method
        System.out.println("Animal is sleeping");
    }
}

class Dog extends Animal {

    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {

        Dog d = new Dog();   // allowed
        d.sound();           // overridden method
        d.sleep();           // normal method
    }
}
```

### ✔ Output
```
Dog barks
Animal is sleeping
```

---

# 💻 Example 2 – Vehicle Example (Real World)

```java
abstract class Vehicle {

    abstract void start();   // must be implemented by child

    void stop() {
        System.out.println("Vehicle stopped");
    }
}

class Car extends Vehicle {

    void start() {
        System.out.println("Car starting...");
    }
}

public class Main {
    public static void main(String[] args) {

        Car c = new Car();
        c.start();
        c.stop();
    }
}
```

---

# 💻 Example 3 – Multiple Child Classes

```java
abstract class Shape {

    abstract void area();
}

class Circle extends Shape {

    void area() {
        System.out.println("Circle area = πr²");
    }
}

class Square extends Shape {

    void area() {
        System.out.println("Square area = side × side");
    }
}

public class Main {
    public static void main(String[] args) {

        Shape s1 = new Circle();
        s1.area();

        Shape s2 = new Square();
        s2.area();
    }
}
```

---

# ⭐ Why Use Abstract Classes?

- To force child classes to implement specific methods  
- Helps achieve **partial abstraction**  
- Provides a common base class  
- Helps in designing frameworks and templates  

---

# ⚠ Important Notes

- Abstract class **cannot** be instantiated  
- Child class must implement abstract methods  
- Abstract class can have:
  ✔ Variables  
  ✔ Constructors  
  ✔ Normal methods  
  ✔ Abstract methods  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create abstract class **Bank** with abstract method `rateOfInterest()`.  
Create classes `SBI`, `HDFC` that override it.

### ✔ Task 2  
Create abstract class **Animal** with abstract method `move()`.  
Create classes `Dog` and `Fish` implementing move differently.

### ✔ Task 3  
Create abstract class **Phone** with abstract `camera()` and normal `call()`.  
Create child class `SmartPhone` implementing camera().

