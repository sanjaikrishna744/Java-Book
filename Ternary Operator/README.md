# 🟢 Ternary Operator in Java (Simple Explanation)

The **ternary operator** is a short form of writing an **if–else** statement.  
It helps write conditions in **one line**.

### 🧩 Syntax:
```
condition ? value_if_true : value_if_false;
```

---

# 💻 Basic Example

```java
int age = 20;

String result = (age >= 18) ? "Adult" : "Minor";

System.out.println(result);
```

### ✔ Output
```
Adult
```

---

# 💡 Why Use Ternary?
- Short  
- Clean  
- Perfect for simple if–else conditions

---

# ⚡ Example 2: Even or Odd

```java
int num = 7;

String check = (num % 2 == 0) ? "Even" : "Odd";

System.out.println(check);
```

### ✔ Output
```
Odd
```

---

# 🧠 Example 3: User Input Ternary Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter your marks out of 100:");
        int marks = in.nextInt();

        String result = (marks >= 50) ? "Pass" : "Fail";

        System.out.println(result);
    }
}
```

### ✔ Example Output
```
Pass
```

---

# ⭐ Nested Ternary (Ternary inside ternary)

```java
int mark = 85;

String grade = (mark >= 90) ? "A"
              : (mark >= 75) ? "B"
              : (mark >= 60) ? "C"
              : "Fail";

System.out.println(grade);
```

---

# 🔥 Practice Task

Take from user:
1. Age  

Use ternary to print:
- “Eligible to Vote” if age >= 18
- “Not Eligible” if age < 18

