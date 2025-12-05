# 🔁 Do–While Loop in Java (Simple Explanation)

A **do–while loop** is similar to a while loop,  
**but it runs at least one time**, even if the condition is false.

### 🧩 Syntax:
```java
do {
    // repeated code
} while(condition);
```

---

# 💻 Basic Example – Prints 1 to 5

```java
int i = 1;

do {
    System.out.println(i);
    i++;
} while(i <= 5);
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

# ⭐ Key Difference (While vs Do-While)

| Loop | Condition Checked | Runs At Least Once? |
|------|------------------|----------------------|
| while | Before loop starts | ❌ No |
| do–while | After loop runs | ✔ Yes |

---

# ⚡ Example 2 – Condition False but Loop Runs Once

```java
int i = 10;

do {
    System.out.println(i);
    i++;
} while(i < 5);
```

### ✔ Output
```
10
```

(Loop runs once even though condition is false!)

---

# 💻 Example 3 – Keep Asking Until User Enters "stop"

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        String input;

        do {
            System.out.println("Type anything ('stop' to exit):");
            input = in.nextLine();
        } while(!input.equalsIgnoreCase("stop"));

        System.out.println("Program Ended.");
    }
}
```

---

# 💻 Example 4 – Sum of Numbers Until User Enters 0

```java
import java.util.Scanner;

Scanner in = new Scanner(System.in);

int num;
int sum = 0;

do {
    System.out.println("Enter a number (0 to stop):");
    num = in.nextInt();
    sum += num;
} while(num != 0);

System.out.println("Total Sum = " + sum);
```

---

# ⭐ Summary

- `do–while` runs **at least once**
- Condition checked **after** loop body  
- Used for **menu programs**, **retry inputs**, **user prompts**  

---

# 🔥 Practice Tasks

### Task 1  
Keep asking a number until user enters **negative**, then print total count.

### Task 2  
Create a "PIN Login" program:
- Ask for PIN using do–while  
- If wrong → retry  
- Stop only when correct PIN entered

### Task 3  
Print table of a number using do–while.

