# ⌨️ User Input in Java (Simple Explanation)

To take input from the user in Java, we use:

```
Scanner sc = new Scanner(System.in);
```

`Scanner` class helps us read:
- Numbers  
- Words  
- Full sentences  
- Decimal values  

---

# 📥 Step-by-step: How User Input Works

### 1️⃣ Import the Scanner
Java-ku input edukka Scanner venum.

```java
import java.util.Scanner;
```

---

### 2️⃣ Create Scanner Object

```java
Scanner sc = new Scanner(System.in);
```

`System.in` → keyboard input

---

# 💻 Basic Input Example

```java
import java.util.Scanner;

public class UserInputExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```

---

# 📝 Input Types in Scanner

| Method | Reads | Example |
|--------|--------|---------|
| `nextInt()` | integer | age, count |
| `nextDouble()` | decimal | marks, price |
| `next()` | one word | name |
| `nextLine()` | full sentence | address |

---

# ⚠️ Common Mistake

`nextLine()` after `nextInt()` or `nextDouble()` sometimes **skips input**  
Because numbers don’t consume the newline `\n`.

Fix:

```java
sc.nextLine(); // clear the buffer
```

---

# 🎯 Example: Read All Types

```java
import java.util.Scanner;

public class InputAllExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter name: ");
        String name = sc.nextLine();

        System.out.print("Enter age: ");
        int age = sc.nextInt();

        System.out.print("Enter mark: ");
        double mark = sc.nextDouble();

        System.out.println("Hello " + name + ", Age: " + age + ", Mark: " + mark);
    }
}
```

---

# 🌟 Summary

- User input → use `Scanner`
- `nextInt()` → numbers  
- `nextLine()` → full sentence  
- Always import: `import java.util.Scanner;`  

---

# 🔥 Practice Task

Ask the user:
1. Name  
2. Favorite Sport  
3. Jersey Number  

Print a message like:

```
Hello Arctic! Your favorite sport is Football and your jersey number is 10.
```
# 🧩 Example Problem – Taking User Input in Java

This example shows how to take **String**, **int**, and **full sentence** inputs from the user.  
It also fixes the common issue where `nextLine()` gets skipped after `nextInt()`.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter your name:");
        String name = in.nextLine();     

        System.out.println("Enter your age:");
        int age = in.nextInt();

        in.nextLine(); // clears leftover newline

        System.out.println("Enter your address:");
        String address = in.nextLine();

        System.out.println("My name is " + name);
        System.out.println("My age is " + age);
        System.out.println("My address is " + address);
    }
}
```

---

## 🧠 Why do we use `in.nextLine()` after `nextInt()`?

`nextInt()` reads only the number.  
The **Enter key (`\n`)** remains in the input buffer.

So the next `nextLine()` reads that **empty newline** instead of actual input.

To fix this:  
```java
in.nextLine();
```
It clears the leftover newline.

---

## 🎯 Sample Output

```
Enter your name:
Arctic
Enter your age:
20
Enter your address:
Erode, Tamil Nadu

My name is Arctic
```
# 🧩 Example Problem – Multiply, Add & Divide Three Numbers

This program takes **three integer inputs** from the user:

- Multiply all three numbers → store in `d`  
- Add all three numbers → store in `e`  
- Divide `d` by `e` → print the result  

This helps understand basic arithmetic operations and user input in Java.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter value for a:");
        int a = in.nextInt();

        System.out.println("Enter value for b:");
        int b = in.nextInt();

        System.out.println("Enter value for c:");
        int c = in.nextInt();

        int d = a * b * c;   // multiplication
        int e = a + b + c;   // addition

        System.out.println("The answer is: " + (d / e));
    }
}
```

---

## 🧠 How It Works

| Step | Operation | Example |
|------|-----------|----------|
| 1 | Multiply a, b, c | `d = a * b * c` |
| 2 | Add a, b, c | `e = a + b + c` |
| 3 | Divide d by e | `d / e` |

---

## 🎯 Sample Input
```
2
3
4
```

## ✔️ Sample Output
```
The answer is: 2
```

(Explanation: d = 24, e = 9 → 24 / 9 = 2 because integer division)

---

## ⚠️ Note on Integer Division
`d / e` uses **integer division**, so decimal values are removed.

Example: `24 / 9 = 2` (not 2.66)

If you want decimal output, use:

```java
double result = (double)d / e;
```

---

## 🔥 Practice Task

Write a program to:

1. Take 4 integer inputs  
2. Multiply all → store in `p`  
3. Add all → store in `q`  
4. Print `p % q` (modulus operation)


# 🧩 Example Problem – Convert Score (100 Marks → 10 Marks)

This program takes **Name**, **Score (out of 100)**, and **Department** as input.  
The score entered by the user is converted into **a value out of 10** by dividing it by 10.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter your name:");
        String Name = in.nextLine();

        System.out.println("Enter your score out of 100:");
        double Score = in.nextDouble();

        in.nextLine(); // clear extra newline

        System.out.println("Enter your department:");
        String dept = in.nextLine();

        // Convert score out of 100 → score out of 10
        double convertedScore = Score / 10;

        System.out.println("My Name is " + Name);
        System.out.println("My Score is " + convertedScore + "/10");
        System.out.println("My Department is " + dept);
    }
}
```

---

## 🧠 How Conversion Works

If a student scores **85/100**:

```
85 / 10 = 8.5
```

So final score printed = `8.5 / 10`

---

## 🎯 Sample Input
```
Arctic
92
CSE
```

## ✔️ Sample Output
```
My Name is Arctic
My Score is 9.2/10
My Department is CSE
```

---

## 🔥 Practice Task

Ask the user for:
- Name  
- 3 subject scores (out of 100)

Convert each score out of 10 and print the **average score**.



























