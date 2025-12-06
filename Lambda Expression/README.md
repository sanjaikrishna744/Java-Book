# ⚡ Functional Interface & Lambda Expression in Java (Simple Explanation)

---

## 🔹 What is a Functional Interface?

A **Functional Interface** is an interface that has  
✅ **ONLY ONE abstract method**

It may have:
- default methods  
- static methods  

But abstract method **only one** irukkanum.

👉 Functional interface is mainly used for **Lambda Expressions**.

---

## ✅ Functional Interface Rules

✔ Only ONE abstract method  
✔ Can use `@FunctionalInterface` annotation (optional but recommended)  
✔ Used to reduce code using lambda expressions  

---

## 💻 Example 1 – Simple Functional Interface

```java
@FunctionalInterface
interface MyInterface {
    void show();
}
```

---

## 🔹 What is Lambda Expression?

**Lambda Expression** is a **short form of method/function**.

👉 No need:
- method name  
- return keyword (sometimes)  
- class creation  

👉 Used ONLY with **functional interfaces**.

---

## 🧩 Lambda Syntax

```java
(parameters) -> { body }
```

Example:
```java
() -> System.out.println("Hello");
```

---

## 💻 Example 2 – Without Lambda (Normal Way)

```java
interface Hello {
    void sayHello();
}

class Test implements Hello {
    public void sayHello() {
        System.out.println("Hello World");
    }
}

public class Main {
    public static void main(String[] args) {
        Hello h = new Test();
        h.sayHello();
    }
}
```

---

## 💻 Example 3 – SAME Program Using Lambda (Simple 🚀)

```java
@FunctionalInterface
interface Hello {
    void sayHello();
}

public class Main {
    public static void main(String[] args) {

        Hello h = () -> System.out.println("Hello World");
        h.sayHello();
    }
}
```

✅ Less code  
✅ More readable  
✅ Modern Java

---

## 💻 Example 4 – Lambda with Parameters

```java
@FunctionalInterface
interface Add {
    int sum(int a, int b);
}

public class Main {
    public static void main(String[] args) {

        Add obj = (a, b) -> a + b;

        System.out.println(obj.sum(10, 20));
    }
}
```

### ✔ Output
```
30
```

---

## 💻 Example 5 – Real World Example

```java
@FunctionalInterface
interface Calculator {
    int operate(int a, int b);
}

public class Main {
    public static void main(String[] args) {

        Calculator add = (a, b) -> a + b;
        Calculator mul = (a, b) -> a * b;

        System.out.println("Add = " + add.operate(5, 3));
        System.out.println("Multiply = " + mul.operate(5, 3));
    }
}
```

---

## ⭐ Why Lambda Expression?

✅ Reduces boilerplate code  
✅ Cleaner & shorter syntax  
✅ Makes code readable  
✅ Widely used in Java 8+ (Streams, Collections)

---

## 🔍 Functional Interface Examples (Built-in)

| Interface | Method |
|---------|--------|
| Runnable | run() |
| Comparator | compare() |
| Callable | call() |
| Consumer | accept() |
| Supplier | get() |
| Predicate | test() |

---

## 💻 Example 6 – Runnable with Lambda

```java
public class Main {
    public static void main(String[] args) {

        Runnable r = () -> System.out.println("Thread running");
        r.run();
    }
}
```

---

## ⭐ Summary

- Functional Interface → ONLY ONE abstract method  
- Lambda works ONLY with functional interface  
- Lambda makes code short & clean  
- Introduced in **Java 8**  

---

## 🔥 Practice Tasks

### ✔ Task 1  
Create functional interface `Greeting`  
Method: greet(String name)  
Use lambda to print greeting.

### ✔ Task 2  
Create functional interface `Square`  
Return square of number using lambda.

### ✔ Task 3  
Use lambda to check even or odd number.

