# 🎯 Parameterized Methods in Java (Simple Explanation)

A **parameterized method** is a method that receives values (inputs) when it is called.

Parameters = inputs  
Method uses those inputs to do some work.

---

# 🧩 Syntax

```java
returnType methodName(type param1, type param2) {
    // use the parameters
}
```

Example:
```java
void greet(String name) {
    System.out.println("Hello " + name);
}
```

---

# 💻 Example 1 – Method with One Parameter

```java
class Main {

    void greet(String name) {
        System.out.println("Hello " + name);
    }

    public static void main(String[] args) {

        Main obj = new Main();
        obj.greet("Arctic");
        obj.greet("Kavin");
    }
}
```

### ✔ Output
```
Hello Arctic
Hello Kavin
```

---

# 💻 Example 2 – Method With Two Parameters

```java
class Main {

    void add(int a, int b) {
        System.out.println("Sum = " + (a + b));
    }

    public static void main(String[] args) {

        Main m = new Main();
        m.add(10, 20);
        m.add(5, 7);
    }
}
```

### ✔ Output
```
Sum = 30
Sum = 12
```

---

# 💻 Example 3 – Parameterized Method (Real World Example)

```java
class Laptop {

    void specs(String brand, int price) {
        System.out.println("Brand: " + brand);
        System.out.println("Price: " + price);
    }
}

public class Main {
    public static void main(String[] args) {

        Laptop lap = new Laptop();

        lap.specs("Asus", 60000);
        lap.specs("HP", 55000);
    }
}
```

---

# ⭐ Why Use Parameterized Methods?

- Pass different values to the same method  
- Reuse one method for multiple inputs  
- Code becomes clean and flexible  

Example:

```
add(10, 20)
add(100, 200)
add(1, 5)
```

Same method, different inputs.

---

# 🔥 Example 4 – Method That Returns Value (Parameterized)

```java
class Calc {

    int multiply(int x, int y) {
        return x * y;
    }
}

public class Main {
    public static void main(String[] args) {

        Calc c = new Calc();
        int ans = c.multiply(6, 7);

        System.out.println("Result = " + ans);
    }
}
```

---

# 🎯 Practice Tasks

### ✔ Task 1  
Create method `fullName(String first, String last)` that prints:
```
Full Name: <first> <last>
```

### ✔ Task 2  
Create method `area(int length, int width)` that prints rectangle area.

### ✔ Task 3  
Create method `grade(int marks)` that prints:
- A if marks >= 90  
- B if >= 75  
- C if >= 60  
- Fail otherwise  

