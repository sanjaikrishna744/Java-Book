# 🔼 `super` Keyword in Java (Simple Explanation)

The **super keyword** is used to refer to the **parent class**.  
It is mainly used for:

1️⃣ Accessing parent class **variables**  
2️⃣ Calling parent class **methods**  
3️⃣ Calling parent class **constructor**  

---

# ⭐ Why Use `super`?

Because sometimes child class variables/methods have the **same name** as parent.  
`super` helps to avoid confusion.

---

# 💻 Example 1 – Using super to Access Parent Variable

```java
class Parent {
    int value = 100;
}

class Child extends Parent {
    int value = 200;

    void show() {
        System.out.println("Child value: " + value);
        System.out.println("Parent value: " + super.value);
    }
}

public class Main {
    public static void main(String[] args) {
        Child c = new Child();
        c.show();
    }
}
```

### ✔ Output
```
Child value: 200
Parent value: 100
```

---

# 💻 Example 2 – Using super to Call Parent Method

```java
class Parent {

    void msg() {
        System.out.println("Message from Parent");
    }
}

class Child extends Parent {

    void msg() {
        System.out.println("Message from Child");
    }

    void display() {
        super.msg();  // calling parent method
        msg();        // calling child method
    }
}

public class Main {
    public static void main(String[] args) {

        Child c = new Child();
        c.display();
    }
}
```

### ✔ Output
```
Message from Parent
Message from Child
```

---

# 💻 Example 3 – Calling Parent Constructor Using super()

```java
class Parent {

    Parent() {
        System.out.println("Parent Constructor");
    }
}

class Child extends Parent {

    Child() {
        super();   // calls Parent constructor
        System.out.println("Child Constructor");
    }
}

public class Main {
    public static void main(String[] args) {

        Child c = new Child();
    }
}
```

### ✔ Output
```
Parent Constructor
Child Constructor
```

---

# 💻 Example 4 – Real World: Vehicle → Car

```java
class Vehicle {

    Vehicle(String brand) {
        System.out.println("Vehicle Brand: " + brand);
    }
}

class Car extends Vehicle {

    Car(String brand, int price) {
        super(brand);     // calling parent constructor
        System.out.println("Car Price: " + price);
    }
}

public class Main {
    public static void main(String[] args) {

        Car c = new Car("BMW", 5000000);
    }
}
```

---

# ⭐ What `super` Can Do?

| Use | Meaning |
|------|---------|
| `super.variable` | Access parent variable |
| `super.method()` | Call parent method |
| `super()` | Call parent constructor |

---

# ⚠ Important Notes

- `super()` must be the **first statement** inside a constructor  
- Cannot use `super()` and `this()` in the same constructor  
- super works only in inheritance  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create `Animal` (with method eat())  
Create `Dog` that overrides eat()  
Use super.eat() to call parent‘s eat() too.

### ✔ Task 2  
Create `Person` with constructor → prints name  
Create `Student` extends Person → use super() inside constructor.

### ✔ Task 3  
Create parent & child with same variable name,  
Use super.variable to print both values.

