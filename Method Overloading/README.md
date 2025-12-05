# 🔄 Method Overloading in Java (Simple Explanation)

**Method Overloading** means:
➡️ Same method name  
➡️ Different parameters  

Java decides which method to call based on:
- Number of parameters  
- Type of parameters  
- Order of parameters  

Overloading makes code **clean, readable, and reusable**.

---

# 🧩 Syntax Example

```java
void info(int a) { }

void info(int a, int b) { }

void info(String name) { }
```

Same method name → different parameter list.

---

# 💻 Example 1 – Simple Overloading

```java
class Main {

    void greet() {
        System.out.println("Hello!");
    }

    void greet(String name) {
        System.out.println("Hello " + name);
    }

    public static void main(String[] args) {

        Main obj = new Main();

        obj.greet();           // calls 1st method
        obj.greet("Arctic");   // calls 2nd method
    }
}
```

### ✔ Output
```
Hello!
Hello Arctic
```

---

# 💻 Example 2 – Overloading add() Method

```java
class Calc {

    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {

        Calc c = new Calc();

        System.out.println(c.add(10, 20));        // int version
        System.out.println(c.add(5.5, 4.5));      // double version
    }
}
```

### ✔ Output
```
30
10.0
```

---

# 💻 Example 3 – Different Number of Parameters

```java
class PrintData {

    void show(String name) {
        System.out.println("Name: " + name);
    }

    void show(String name, int age) {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    void show(String name, int age, String city) {
        System.out.println(name + ", " + age + ", " + city);
    }
}

public class Main {
    public static void main(String[] args) {

        PrintData p = new PrintData();

        p.show("Arctic");
        p.show("Kavin", 21);
        p.show("Arun", 22, "Erode");
    }
}
```

---

# ⭐ Why Use Method Overloading?

- Same action with different inputs  
- Increases readability  
- Cleaner code  
- Avoids writing multiple method names  

Example:
```
area(int side)
area(int length, int width)
area(double radius)
```

All calculate area but using different inputs.

---

# ⚠ Important Rules

- Parameter **must be different**  
- Return type alone cannot overload  
- Method name must be same  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create overloaded method `area()` for:
- Square  
- Rectangle  
- Circle  

### ✔ Task 2  
Create overloaded method `details()`:
- details(String name)  
- details(String name, int age)  

### ✔ Task 3  
Create overloaded `multiply()` that works with:
- int × int  
- double × double  

# 🔄 Method Overloading – Simple Example

Method Overloading means:
- **Same method name**
- **Different parameters**  
(Java chooses which one to run based on the parameter list.)

---

## 💻 Code Example

```java
public class Main {

    void sanjai() {
        System.out.println("one");
    }

    void sanjai(int a) {
        System.out.println("two");
    }

    public static void main(String args[]) {

        Main obj = new Main();

        obj.sanjai();      // calls method with no parameters
        obj.sanjai(20);    // calls method with int parameter
    }
}
```

---

## ✔️ Output
```
one
two
```

---

## 🧠 Explanation

### ✔ sanjai()
- No parameters  
- Prints `"one"`

### ✔ sanjai(int a)
- Takes 1 integer parameter  
- Prints `"two"`

Both methods have the **same name**, but different parameter lists → this is Method Overloading.

---

# ⭐ Why Use Overloading?

- Same behavior with different inputs  
- Cleaner and more readable code  
- No need to create multiple method names  

Example:
```
print(String s)
print(int n)
print(double d)
```

All named `print`, but accept different types.

---

# 🔥 Practice Task

Create a class with overloaded `display()` methods:
1. display(String name)  
2. display(int age)  
3. display(String name, int age)  

Call all three in main().
