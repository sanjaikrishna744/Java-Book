# 🔙 Return Keyword in Java (Simple Explanation)

The **return keyword** is used inside a method to send a value back to the place where the method was called.

### 🧩 Why use return?
- To give back a result  
- To stop a method  
- To use method output in calculations  

---

# 🧩 Syntax

```java
return value;
```

Every method that returns something must have a **return type**:

```
int
double
String
boolean
```

If a method returns nothing → use `void`.

---

# 💻 Example 1 – Method That Returns an Integer

```java
class Main {

    int add(int a, int b) {
        return a + b;   // returning result
    }

    public static void main(String[] args) {

        Main obj = new Main();

        int ans = obj.add(10, 20);  // receiving return value
        System.out.println("Sum = " + ans);
    }
}
```

### ✔ Output
```
Sum = 30
```

---

# 💻 Example 2 – Returning a String

```java
class Main {

    String greet(String name) {
        return "Hello " + name;
    }

    public static void main(String[] args) {

        Main m = new Main();

        String msg = m.greet("Arctic");
        System.out.println(msg);
    }
}
```

---

# 💻 Example 3 – Return Stops the Method

```java
void check(int age) {

    if(age < 18){
        System.out.println("Not eligible");
        return;   // method stops here
    }

    System.out.println("Eligible to vote");
}
```

---

# 💻 Example 4 – Real World Example (Calculate Discount)

```java
class Shop {

    double discount(double price) {
        return price * 0.10;   // 10% discount
    }
}

public class Main {
    public static void main(String[] args) {

        Shop s = new Shop();

        double d = s.discount(500);
        System.out.println("Discount = " + d);
    }
}
```

---

# ⭐ Key Points

- `return` gives back a value  
- Method return type and returned value must match  
  Example:  
  - return int → method must be `int`  
  - return String → method must be `String`  
- `void` methods cannot return a value  
- `return` also stops the method from executing further  

---

# 🔥 Practice Tasks

### ✔ Task 1  
Write method `square(int n)` that returns the square of a number.

### ✔ Task 2  
Write method `max(int a, int b)` that returns the larger number.

### ✔ Task 3  
Write method `isEven(int n)` that returns:
- true → if number is even  
- false → if odd  

