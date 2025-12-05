# 🔹 `this` Keyword in Java (Simple Explanation)

`this` keyword refers to **the current object**.  
It is used when **local variable name** and **instance variable name** are the same.

---

# ⭐ Why Use `this`?

To avoid confusion between:
- Class variable (instance variable)  
- Method/constructor parameter  

Example:

```
this.name → refers to object variable  
name      → refers to method parameter
```

---

# 💻 Example 1 – Using `this` to Assign Values

```java
class Student {

    String name;
    int age;

    Student(String name, int age) {
        this.name = name;  
        this.age = age;    
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Arctic", 20);

        System.out.println(s1.name);
        System.out.println(s1.age);
    }
}
```

### ✔ Output
```
Arctic
20
```

---

# 🧠 Why `this` Is Needed?

Inside constructor:

```
name = name;
```

❌ Both refer to the parameter → object variable never gets value.

But:

```
this.name = name;
```

✔ Left side = object variable  
✔ Right side = parameter value  

---

# 💻 Example 2 – this used to call another method

```java
class Demo {

    void show() {
        System.out.println("Show method called");
    }

    void display() {
        this.show();   // calling method using this
    }
}

public class Main {
    public static void main(String[] args) {

        Demo d = new Demo();
        d.display();
    }
}
```

---

# 💻 Example 3 – this() calling another constructor

```java
class Car {

    String brand;
    int price;

    Car() {
        this("BMW", 5000000);   // calls parameterized constructor
    }

    Car(String brand, int price) {
        this.brand = brand;
        this.price = price;
    }
}

public class Main {
    public static void main(String[] args) {

        Car c = new Car();
        System.out.println(c.brand + " - " + c.price);
    }
}
```

---

# ⭐ What `this` Can Do?

| Usage | Purpose |
|--------|----------|
| `this.variable` | Access object variable |
| `this.method()` | Call a method inside same class |
| `this()` | Call another constructor |
| `return this` | Return current object |

---

# 🔥 Example 4 – Returning Current Object

```java
class Person {

    String name;

    Person setName(String name) {
        this.name = name;
        return this;      // returning current object
    }
}

public class Main {
    public static void main(String[] args) {

        Person p = new Person();
        p.setName("Arctic");

        System.out.println(p.name);
    }
}
```

---

# 🎯 Practice Tasks

### ✔ Task 1  
Create class `Mobile` with constructor parameters `brand` and `price`.  
Use `this` to assign values.

### ✔ Task 2  
Create class `Employee` with:
- Constructor overloading  
- Use `this()` to call another constructor  

### ✔ Task 3  
Create method `setDetails()` which returns `this` and chain calls:
```
obj.setDetails().printDetails();
```

