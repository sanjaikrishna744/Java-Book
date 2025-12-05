# 🔁 For Loop in Java (Simple Explanation)

A **for loop** is used when you want to repeat a block of code a fixed number of times.

### 🧩 Syntax:
```java
for(initialization; condition; update){
    // repeated code
}
```

---

# 💻 Basic Example – Print 1 to 5

```java
for(int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### ✔ Output
```
1
2
3
4
5
```

---

# 🧠 Explanation

| Part | Meaning |
|------|---------|
| `int i = 1` | loop starts at 1 |
| `i <= 5` | loop runs till 5 |
| `i++` | increases i by 1 each time |

---

# ⚡ Example 2 – Print Your Name 3 Times

```java
for(int i = 1; i <= 3; i++){
    System.out.println("Arctic");
}
```

---

# 🍎 Example 3 – Print Even Numbers 2 to 10

```java
for(int i = 2; i <= 10; i += 2){
    System.out.println(i);
}
```

---

# 💡 Example 4 – Reverse Loop (Print 5 to 1)

```java
for(int i = 5; i >= 1; i--){
    System.out.println(i);
}
```

---

# 💻 Real-World Example – Sum of First 5 Numbers

```java
int sum = 0;

for(int i = 1; i <= 5; i++){
    sum = sum + i;
}

System.out.println("Sum = " + sum);
```

### ✔ Output
```
Sum = 15
```

---

# ⭐ When to Use For Loop?

- When you **know** how many times the loop will run  
- For printing series of numbers  
- For doing calculations repeatedly  

---

# 🔥 Practice Task

Write a program using for loop to:

1. Print numbers from 10 to 1  
2. Print squares of numbers from 1 to 5  
3. Print your name 5 times  

# 🔢 For Loop Example – Print Numbers Between Two Inputs

In this example, the user enters **two numbers: a and b**.  
The program prints all numbers from **a to b** using a for loop.

This helps understand:
- How to take user input  
- How to control loop start and end values  
- Basic iteration logic  

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter the a:");
        int a = in.nextInt();

        System.out.println("Enter the b:");
        int b = in.nextInt();

        System.out.println("Your numbers are:");

        for (int i = a; i <= b; i++) {
            System.out.println(i);
        }
    }
}
```

---

## 🧠 How It Works

| Part | Meaning |
|------|----------|
| `int i = a` | loop starts at user value `a` |
| `i <= b` | loop continues till it reaches `b` |
| `i++` | increases value by 1 each time |

---

## ✔️ Sample Input
```
Enter the a:
5
Enter the b:
10
```

## ✔️ Sample Output
```
your numbers are:
5
6
7
8
9
10
```

---

## ⭐ Where This Is Used?

- Printing ranges  
- Counting numbers  
- Generating sequences  
- Loops that depend on user input  

---

## 🔥 Practice Task

Ask user for:
- Start number  
- End number  

Print only **even numbers** between them using a for loop.

# 🔢 For Loop Example – Count Even & Odd Numbers (1 to 10)

This program prints numbers from **1 to 10**, checks if they are **even or odd**,  
prints them, and counts how many even and odd numbers appear.

This helps understand:
- For loop  
- If–else  
- Modulus operator `%`  
- Counters  

---

## 💻 Code Example

```java
public class Main {
    public static void main(String args[]) {

        int evencount = 0;
        int oddcount = 0;

        for (int i = 1; i <= 10; i++) {

            if (i % 2 == 0) {
                evencount++;
                System.out.println("even:");
                System.out.println(i);
            } else {
                oddcount++;
                System.out.println("odd:");
                System.out.println(i);
            }
        }

        System.out.println("The even number count is :");
        System.out.println(evencount);

        System.out.println("The odd number count is :");
        System.out.println(oddcount);
    }
}
```

---

## 🧠 Explanation

### ✔ `i % 2 == 0`  
If number modulo 2 equals 0 → **even number**  

Else → **odd number**

### ✔ Counters  
- `evencount++` → increases even count each time  
- `oddcount++` → increases odd count each time  

---

## ✔️ Expected Output (Shortened)

```
even:
2
odd:
1
even:
4
odd:
3
...
The even number count is :
5
The odd number count is :
5
```

---

## ⭐ What You Learn Here

- How to check if a number is even or odd  
- How to count using variables  
- How to use a loop for repeated tasks  

---

## 🔥 Practice Task

Write a program to:

- Count how many numbers between **1 and 50** are divisible by 3  
- Print the count  
- Print every number divisible by 3  

