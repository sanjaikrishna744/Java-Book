# 🏛️ Multilevel Inheritance in Java (Simple Explanation)

**Multilevel Inheritance** means inheritance happening in multiple levels.

Example:
```
Grandparent → Parent → Child
```

Each class inherits from its super class, forming a **chain**.

---

# ⭐ Structure

```
Class A  (grandparent)
   ↑
Class B  (parent)
   ↑
Class C  (child)
```

Class C gets features from BOTH B and A.

---

# 💻 Example 1 – Simple Multilevel Inheritance

```java
class A {
    void msgA() {
        System.out.println("Message from A");
    }
}

class B extends A {
    void msgB() {
        System.out.println("Message from B");
    }
}

class C extends B {
    void msgC() {
        System.out.println("Message from C");
    }
}

public class Main {
    public static void main(String[] args) {

        C obj = new C();

        obj.msgA();   // from A
        obj.msgB();   // from B
        obj.msgC();   // from C
    }
}
```

### ✔ Output
```
Message from A
Message from B
Message from C
```

---

# 💻 Example 2 – Real World: Person → Employee → Programmer

```java
class Person {

    String name = "Arctic";

    void sleep() {
        System.out.println("Person sleeping...");
    }
}

class Employee extends Person {

    int salary = 30000;

    void work() {
        System.out.println("Employee working...");
    }
}

class Programmer extends Employee {

    int bonus = 15000;

    void code() {
        System.out.println("Programmer coding...");
    }
}

public class Main {
    public static void main(String[] args) {

        Programmer p = new Programmer();

        System.out.println(p.name);
        System.out.println(p.salary);
        System.out.println(p.bonus);

        p.sleep(); 
        p.work();
        p.code();
    }
}
```

---

# 💻 Example 3 – Vehicle → Car → SportsCar

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

class SportsCar extends Car {
    void turbo() {
        System.out.println("Turbo mode activated!");
    }
}

public class Main {
    public static void main(String[] args) {

        SportsCar s = new SportsCar();

        s.start();  
        s.drive();  
        s.turbo();  
    }
}
```

---

# ⭐ Advantages of Multilevel Inheritance

- Code reusability increases  
- Natural hierarchy  
- Child class becomes powerful  
- Allows layered features  

---

# ⚠ Rules / Notes

❌ Java does **not** support multiple inheritance with classes  
✔ But multilevel inheritance *is allowed*  

Private members are **not inherited**.

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create **Animal → Mammal → Dog** and give each a method:
- Animal: eat()  
- Mammal: walk()  
- Dog: bark()  

Call all methods using Dog object.

### ✔ Task 2  
Create **Grandfather → Father → Son**.  
Each prints a family message.

### ✔ Task 3  
Create **Electronics → Laptop → GamingLaptop**.  
Add features in each and test.

