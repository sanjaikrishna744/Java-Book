# ⚡ `static` Keyword in Java (Simple Explanation)

`static` keyword is used to create **class-level** members.

✔ Belongs to the **class**, not objects  
✔ Shared by **all objects**  
✔ Memory created only **once**

You can access static members **without creating an object**.

---

# ⭐ When to Use `static`?

- When a variable should be **common** for all objects  
- When a method should run **without object creation**  
- Utility methods (like Math functions)  
- Memory-efficient programs  

---

# 🧩 Types of static members

| Type | Usage |
|------|--------|
| static variable | Shared value for all objects |
| static method | Can be called without object |
| static block | Runs once when class loads |
| static class | Inner classes only |

---

# 💻 Example 1 – Static Variable (Shared by All Objects)

```java
class Student {
    static String college = "ABC College";  // shared variable
    String name;

    Student(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Arctic");
        Student s2 = new Student("Kavin");

        System.out.println(s1.name + " - " + Student.college);
        System.out.println(s2.name + " - " + Student.college);
    }
}
```

### ✔ Output
```
Arctic - ABC College
Kavin - ABC College
```

---

# 💻 Example 2 – Static Method (No Object Needed)

```java
class MathHelper {

    static int square(int x) {
        return x * x;
    }
}

public class Main {
    public static void main(String[] args) {

        System.out.println(MathHelper.square(5));  // call without object
    }
}
```

### ✔ Output
```
25
```

---

# 💻 Example 3 – Static Block (Runs Once Only)

```java
class Demo {

    static {
        System.out.println("Static block executed");
    }
}

public class Main {
    public static void main(String[] args) {

        Demo d = new Demo();  // object creation
    }
}
```

### ✔ Output
```
Static block executed
```

---

# 💻 Example 4 – Static + Normal Members Difference

```java
class Counter {

    static int count = 0;   // shared
    int num = 0;            // object-only

    Counter() {
        count++;
        num++;
        System.out.println("Static count = " + count);
        System.out.println("Normal num = " + num);
    }
}

public class Main {
    public static void main(String[] args) {

        Counter c1 = new Counter();
        Counter c2 = new Counter();
        Counter c3 = new Counter();
    }
}
```

### ✔ Output (important concept)
```
Static count = 1
Normal num = 1

Static count = 2
Normal num = 1

Static count = 3
Normal num = 1
```

---

# ⭐ Key Points to Remember

- `static` members belong to **class**, not objects  
- Access static methods using the class name  
- Cannot use **this** inside static methods  
- Static block runs once when class loads  
- Great for **constants**, **utility methods**, **counters**

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create class `Bank` with static variable `bankName`.  
Create 3 objects and print same bank name.

### ✔ Task 2  
Create static method `add(int a, int b)` returning sum.  
Call it without object.

### ✔ Task 3  
Create class `IDGenerator` with:
- static int nextId = 1  
- Constructor increases id  
Print IDs for 3 objects.

