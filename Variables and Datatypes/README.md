Variables are how we store information in Java so we can use it later.  
For example, just like a container, That stores element

---

## 💻 Code Example

```java

public class Main {
    public static void main(String[] args) {

        // Creating variables
        int age = 20;                // whole number
        String name = "Arctic";      // text
        double mark = 92.5;          // decimal value

        // Printing the variables
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Mark: " + mark);
    }
}

```
```
Name: Arctic
Age: 20
Mark: 92.5
```

Datatypes

# 📘 Java Datatypes (Simple Explanation)

Datatypes tell Java **what kind of value** a variable will store.  
Example: number, text, decimal, true/false… etc.

Java datatypes are divided into two types:

---

# 🔹 1. Primitive Datatypes (Basic types)

These are the most common datatypes.  
They store simple values.

| Datatype | Size | Stores | Example |
|----------|------|--------|---------|
| `byte`   | 1 byte | small numbers | `byte b = 10;` |
| `short`  | 2 bytes | medium numbers | `short s = 200;` |
| `int`    | 4 bytes | normal whole numbers | `int age = 20;` |
| `long`   | 8 bytes | very big numbers | `long population = 100000L;` |
| `float`  | 4 bytes | decimal numbers (small) | `float price = 5.99f;` |
| `double` | 8 bytes | decimal numbers (large) | `double mark = 92.5;` |
| `char`   | 2 bytes | single character | `char grade = 'A';` |
| `boolean`| 1 bit  | true / false | `boolean pass = true;` |

---

## 💻 Simple Code Example (Primitive Types)

```java
public class DataTypesExample {
    public static void main(String[] args) {

        int age = 20;
        double mark = 92.5;
        char grade = 'A';
        boolean pass = true;

        System.out.println("Age: " + age);
        System.out.println("Mark: " + mark);
        System.out.println("Grade: " + grade);
        System.out.println("Passed: " + pass);
    }
}
```

---

# 🔹 2. Non-Primitive Datatypes (Reference types)

These datatypes store **objects**, not simple values.

| Datatype | Meaning | Example |
|----------|----------|---------|
| `String` | Stores text | `String name = "Arctic";` |
| `Array` | Stores multiple values | `int[] nums = {1, 2, 3};` |
| `Class` | User-defined type | `Car myCar = new Car();` |
| `Object` | Parent of all classes | `Object obj = new Object();` |

---

## 💻 Simple Non-Primitive Example

```java
public class NonPrimitiveExample {
    public static void main(String[] args) {

        String name = "Arctic";
        int[] marks = {85, 90, 92};

        System.out.println("Name: " + name);
        System.out.println("First Mark: " + marks[0]);
    }
}
```

---

# 🌟 Summary

- **Primitive types** → numbers, characters, true/false  
- **Non-primitive types** → Strings, Arrays, Classes  
- Datatypes help Java understand **what kind of data** you want to store  

---

# 🎯 Practice Task

Create variables of these types:  
- `String`  
- `int`  
- `double`  
- `boolean`  

Print all values.

# 🔄 Java Type Conversion (Simple Explanation)

Type Conversion = One datatype value → another datatype value-a mathuradhu.

Java has **two types** of type conversion:

---

# 1️⃣ Widening Conversion (Automatic)
Small type → Big type  
Java **automatically converts** it.  
No data loss.

Order (small → big):

```
byte → short → int → long → float → double
```

### ✅ Example (Automatic Conversion)

```java
public class WideningExample {
    public static void main(String[] args) {

        int num = 10;
        double result = num;  // int → double (automatic)

        System.out.println(result); // 10.0
    }
}
```

---

# 2️⃣ Narrowing Conversion (Manual)
Big type → Small type  
**You must force Java to convert** using `(type)`  
Possible data loss!

### ⚠️ Example (Manual Conversion)

```java
public class NarrowingExample {
    public static void main(String[] args) {

        double mark = 92.7;
        int finalMark = (int) mark; // double → int

        System.out.println(finalMark); // 92
    }
}
```

---

# ⭐ Shortcut to Remember

| Conversion Type | Meaning | Example |
|-----------------|---------|---------|
| Widening | small → big (automatic) | int → double |
| Narrowing | big → small (manual) | double → int |

---

# 📌 Extra: String Conversion

### String → int

```java
int num = Integer.parseInt("123");
```

### int → String

```java
String value = String.valueOf(123);
```

---

# 🌟 Summary

- **Widening** = automatic, safe  
- **Narrowing** = manual, may lose data  
- String parsing uses `Integer.parseInt()`  
- Use `(type)` for manual casting  

---

# 🎯 Practice Task

Convert:
1. `long` → `int`  
2. `int` → `double`  
3. `"56"` (String) → `int`



