# 🔍 If–Else Statement (Simple Explanation)

If–Else is used when you want the program to make a **decision**.

- **if** → condition true na run aagum  
- **else** → condition false na run aagum  

Java checks the condition and chooses one block.

---

# 💻 Basic Example

```java
int age = 18;

if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are a minor.");
}
```

### ✔️ Output
```
You are an adult.
```

---

# 🧠 How It Works

| Condition | Result |
|----------|--------|
| True | `if` block runs |
| False | `else` block runs |

---

# ⚡ Example with User Input

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter your marks out of 100:");
        int marks = in.nextInt();

        if (marks >= 50) {
            System.out.println("You Passed! 🎉");
        } else {
            System.out.println("You Failed ❌");
        }
    }
}
```

---

# 📝 Example 2 – Check Even or Odd Number

```java
int num = 7;

if (num % 2 == 0) {
    System.out.println("Even number");
} else {
    System.out.println("Odd number");
}
```

---

# 🔁 If–Else Ladder (Multiple Conditions)

```java
int mark = 85;

if (mark >= 90) {
    System.out.println("Grade A");
}
else if (mark >= 75) {
    System.out.println("Grade B");
}
else if (mark >= 60) {
    System.out.println("Grade C");
}
else {
    System.out.println("Fail");
}
```

---

# ⭐ Summary

- `if` = executes when condition is true  
- `else` = executes when condition is false  
- For multiple conditions → use **else-if ladder**  
- Always use `==` for comparison, not `=`  

---

# 🔥 Practice Task

Take a number from the user:
- If number > 0 → print **Positive**  
- If number < 0 → print **Negative**  
- Else → print **Zero**

# 🌦️ Example Problem – Check Weather Using Boolean (If–Else)

This program checks if it is raining using a **boolean variable**.  
If `rain = true`, the program asks you to take an umbrella.  
If `rain = false`, it tells you to enjoy the sunlight.

---

## 💻 Code Example

```java
public class Main {
    public static void main(String[] args) {

        boolean rain = true;

        if (rain) {
            System.out.println("Take an umbrella ☔");
        } else {
            System.out.println("Enjoy the sunlight ☀️");
        }
    }
}
```

---

## 🧠 Explanation

- `boolean` can store **true** or **false** only.
- If `rain` is true → `if` block runs.
- If `rain` is false → `else` block runs.

---

## ✔️ Sample Output (when rain = true)
```
Take an umbrella ☔
```

## ✔️ Sample Output (when rain = false)
```
Enjoy the sunlight ☀️
```

---

## 🔥 Practice Task

Create a boolean variable:
- `isHungry`

If true → print **“Eat some food”**  
Else → print **“You are not hungry”**

# 🔢 Example Problem – Compare Two Numbers Using If–Else

This program accepts **two integer inputs** from the user and checks which number is greater.  
It also includes simple comments explaining **compile-time** and **runtime** errors.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {

        Scanner in = new Scanner(System.in);

        int num1 = in.nextInt();
        int num2 = in.nextInt();

        // Compile-time error → happens when code has mistakes while compiling
        // Runtime error → happens when program runs (e.g., divide by zero)

        if (num1 > num2) {
            System.out.println("num1 is greater");
        } else {
            System.out.println("num2 is greater");
        }
    }
}
```

---

## 🧠 How It Works

1. User enters two numbers  
2. Program compares `num1` and `num2`  
3. If num1 is bigger → print “num1 is greater”  
4. Else → print “num2 is greater”

---

## 🎯 Sample Input
```
10
7
```

## ✔️ Sample Output
```
num1 is greater
```

---

## 📘 Notes  
- If both values are equal, program will print `num2 is greater`  
  (because there is no `==` condition)  
- Want equality check? Add:

```java
if (num1 > num2) {
    System.out.println("num1 is greater");
} else if (num1 < num2) {
    System.out.println("num2 is greater");
} else {
    System.out.println("Both numbers are equal");
}
```

---

## 🔥 Practice Task

Ask the user for **three numbers** and print the **largest** one.


