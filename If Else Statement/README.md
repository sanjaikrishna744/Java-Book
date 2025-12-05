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

# 🧩 Else–If Ladder Example (Simple Explanation)

The **else–if ladder** is used when we have **multiple conditions** to check.  
Only the **first true condition** will run.

This example reads a score and prints a reward based on the range.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {

        Scanner in = new Scanner(System.in);

        int score = in.nextInt();

        if (score > 35 && score < 60) {
            System.out.println("video game");
        }
        else if (score > 60 && score < 90) {
            System.out.println("iphone");
        }
        else {
            System.out.println("macbook pro");
        }
    }
}
```

---

## 🧠 Explanation of Conditions

| Condition | Meaning | Output |
|----------|----------|---------|
| score > 35 AND score < 60 | Score between 36–59 | “video game” |
| score > 60 AND score < 90 | Score between 61–89 | “iphone” |
| All other values | Anything else | “macbook pro” |

---

## ✔️ Sample Inputs & Outputs

### Input:
```
45
```
Output:
```
video game
```

### Input:
```
75
```
Output:
```
iphone
```

### Input:
```
95
```
Output:
```
macbook pro
```

---

# ⭐ Why use else–if?

- Helps check **more than one condition**  
- Cleaner than using multiple IF statements  
- Stops checking when a true condition is found  

---

# 🔥 Practice Task

Ask the user to enter their age:

- If age < 13 → print “Child”  
- If age between 13–19 → print “Teenager”  
- If age between 20–59 → print “Adult”  
- Else → print “Senior Citizen”

# 🏢 Nested If Statement (Simple Explanation)

A **nested if** means an **if statement inside another if statement**.  
We use this when one condition depends on another condition.

Example flow:
- If you enter KFC  
  - then only you can order chicken  
    - then only you can drink Pepsi  

---

## 💻 Code Example

```java
public class Main {                                                          
    public static void main(String args[]) {                              
         
        boolean kfc = true;
        boolean chicken = true;
        boolean pepsi = true;
        
        if (kfc) {
            System.out.println("Entering into KFC");
          
            if (chicken) {
                System.out.println("Eating chicken");
              
                if (pepsi) {
                    System.out.println("Drinking Pepsi");
                }
            }
        }
    }
}
```

---

## 🧠 How It Works

| Condition | True? | Action |
|----------|--------|---------|
| kfc == true | ✔ | Enter KFC |
| chicken == true | ✔ | Eat chicken |
| pepsi == true | ✔ | Drink Pepsi |

All three conditions must be **true** for all three actions to print.

---

## ✔️ Sample Output
```
Entering into KFC
Eating chicken
Drinking Pepsi
```

---

## ⭐ Concept Summary

- Nested IF = decision inside another decision  
- Inner `if` runs **only if** the outer `if` is true  
- Useful for step-by-step conditions

---

## 🔥 Practice Task

Create a program:

- boolean `onlineOrder = true`  
- boolean `paymentDone = true`  
- boolean `orderPacked = true`  

Use nested if:

- If onlineOrder → print “Order placed”  
- Inside that: if paymentDone → print “Payment successful”  
- Inside that: if orderPacked → print “Order ready for delivery”

# 🏦 Real-World Nested If Example – Loan Eligibility Check

This program checks whether a person is eligible for a loan based on:
- Salary  
- Age  
Then checks how much loan they are requesting.

It uses a **nested if** because the *second decision* (loan amount) must run **only if** the person is eligible.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {                                                          
    public static void main(String args[]) {                              
        
        Scanner in = new Scanner(System.in);

        System.out.println("Enter your salary:");
        int salary = in.nextInt();

        System.out.println("Enter your age:");
        int age = in.nextInt();
        
        // First condition: salary OR age eligibility
        if (salary >= 20000 || age <= 25) {

            System.out.println("How much loan amount you want?");
            int loan = in.nextInt();

            // Nested if: checks loan limit
            if (loan <= 50000) {
                System.out.println("You are eligible for the loan");
            } else {
                System.out.println("Maximum loan amount is 50000");
            }
        } 
        
        else {
            System.out.println("You are not eligible");
        }
    }
}
```

---

## 🧠 Explanation

### ✔ Condition 1 (Outer If)  
```
salary >= 20000  OR  age <= 25
```
If either is true → user moves to the next step.

### ✔ Condition 2 (Nested If)  
Only if user is eligible:

```
loan <= 50000
```
→ Approve loan  
Else → Show maximum limit

---

## ✔️ Sample Input
```
Enter your salary:
18000
Enter your age:
22
How much loan amount you want?
40000
```

## ✔️ Sample Output
```
You are eligible for the loan
```

---

## ⭐ Why Use Nested If?

- Loan amount check must run **only after** eligibility check  
- Organizes the logic clearly  
- Good for real-world decision systems (banking, shopping, etc.)

---

## 🔥 Practice Task

Create a program:

- Ask for `income`
- Ask for `creditScore`
- If `income > 30000` AND `creditScore > 700`  
  - Ask for loan amount  
  - If amount ≤ 1,00,000 → approve  
  - Else → reject  
Else  
  - print **“Not eligible for loan”**


