# 🌳 Hierarchical Inheritance in Java (Simple Explanation)

In **Hierarchical Inheritance**,  
**one parent class** is inherited by **multiple child classes**.

Structure:
```
        Parent
        /   \
  Child1   Child2
        \   /
       Child3
```

Each child gets properties of the same parent.

---

# ⭐ Syntax

```java
class Parent { }

class Child1 extends Parent { }

class Child2 extends Parent { }

class Child3 extends Parent { }
```

---

# 💻 Example 1 – Simple Hierarchical Inheritance

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

class Cat extends Animal {

    void meow() {
        System.out.println("Cat is meowing...");
    }
}

class Cow extends Animal {

    void moo() {
        System.out.println("Cow is mooing...");
    }
}

public class Main {
    public static void main(String[] args) {

        Dog d = new Dog();
        d.eat();
        d.bark();

        Cat c = new Cat();
        c.eat();
        c.meow();

        Cow cw = new Cow();
        cw.eat();
        cw.moo();
    }
}
```

---

# 💻 Example 2 – Real World: Vehicle → Car, Bike, Bus

```java
class Vehicle {

    void start() {
        System.out.println("Vehicle starting...");
    }
}

class Car extends Vehicle {

    void drive() {
        System.out.println("Car driving...");
    }
}

class Bike extends Vehicle {

    void ride() {
        System.out.println("Bike riding...");
    }
}

class Bus extends Vehicle {

    void carryPassengers() {
        System.out.println("Bus carrying passengers...");
    }
}

public class Main {
    public static void main(String[] args) {

        Car car = new Car();
        car.start();
        car.drive();

        Bike bike = new Bike();
        bike.start();
        bike.ride();

        Bus bus = new Bus();
        bus.start();
        bus.carryPassengers();
    }
}
```

---

# ⭐ Advantages of Hierarchical Inheritance

- One parent → many child classes  
- Code reuse increases  
- Clear separation of child behaviors  
- Good for grouping similar category classes  

---

# ⚠ Important Notes

- Child classes **cannot inherit from each other**  
- Parent constructor executes first  
- Private members of parent NOT inherited  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create class **Shape** with method `area()`.  
Child classes:
- Circle  
- Rectangle  
- Triangle  

Each child prints its own area.

### ✔ Task 2  
Create class **Person** with method `commonSkill()`.  
Child classes:
- Student → study()  
- Teacher → teach()  

Call all functions.

### ✔ Task 3  
Create parent class **Account** with method deposit().  
Child classes:
- SavingsAccount  
- CurrentAccount  

Each child adds its own method.

