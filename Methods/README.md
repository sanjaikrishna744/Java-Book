# 🛠️ Methods / Functions in Java (Simple Explanation)

A **method** (also called *function*) is a block of code that performs a task.  
Instead of writing the same code again and again, we put it inside a method and **reuse** it.

---

# 📌 Why Use Methods?

- Avoid repeating code  
- Better organization  
- Cleaner program  
- Reusable actions  

---

# 🧩 Syntax

```java
returnType methodName() {
    // code
}
```

Example:
```java
void greet() {
    System.out.println("Hello!");
}
```

---

# 💻 Example 1 – Simple Method (No input, No return)

```java
class Main {

    void greet() {
        System.out.println("Hello Arctic!");
    }

    public static void main(String[] args) {

        Main obj = new Main();
        obj.greet();   // calling method
    }
}
```

### ✔ Output
```
Hello Arctic!
```

---

# 💻 Example 2 – Method With Parameters

```java
class Main {

    void details(String name, int age) {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }

    public static void main(String[] args) {

        Main obj = new Main();
        obj.details("Arctic", 20);
    }
}
```

---

# 💻 Example 3 – Method That Returns a Value

```java
class Main {

    int square(int n) {
        return n * n;   // returning value
    }

    public static void main(String[] args) {

        Main obj = new Main();
        int result = obj.square(5);

        System.out.println("Square: " + result);
    }
}
```

### ✔ Output
```
Square: 25
```

---

# ⭐ Types of Methods

| Type | Meaning |
|------|---------|
| No-parameter method | Doesn't take input |
| Parameterized method | Takes input |
| Return method | Sends output back using `return` |
| Void method | Does NOT return anything |

---

# 🧠 Calling a Method

Use the object + dot operator:

```java
obj.methodName();
```

or with inputs:

```java
obj.methodName(10, 20);
```

---

# 🔥 Real-World Example – Calculator Methods

```java
class Calc {

    int add(int a, int b) {
        return a + b;
    }

    int multiply(int a, int b) {
        return a * b;
    }
}

public class Main {
    public static void main(String[] args) {

        Calc c = new Calc();

        System.out.println("Sum = " + c.add(10, 20));
        System.out.println("Product = " + c.multiply(5, 4));
    }
}
```

---

# 🎯 Practice Tasks

### ✔ Task 1  
Create a method `greetUser(String name)` that prints:
```
Hello <name>, welcome!
```

### ✔ Task 2  
Create a method `max(int a, int b)` that returns the bigger value.

### ✔ Task 3  
Create a method `area(int r)` that returns the area of a circle.

