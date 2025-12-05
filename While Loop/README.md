# 🔄 While Loop in Java (Simple Explanation)

A **while loop** is used when you want to repeat something **as long as a condition is true**.

### 🧩 Syntax:
```java
while(condition){
    // repeated code
}
```

---

# 💻 Basic Example – Print 1 to 5

```java
int i = 1;

while(i <= 5){
    System.out.println(i);
    i++;   // increase i
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

# 🧠 How It Works?

1. Check condition  
2. If TRUE → execute loop  
3. Update variable  
4. Repeat  

If condition becomes FALSE → loop stops.

---

# ⚠️ Infinite Loop Warning

```java
while(true){
    System.out.println("looping forever...");
}
```

This never stops unless you break it.

---

# 💻 Example 2 – Print Even Numbers from 2 to 10

```java
int i = 2;

while(i <= 10){
    System.out.println(i);
    i += 2;
}
```

---

# 💻 Example 3 – User Input Until They Enter 0

```java
import java.util.Scanner;

Scanner in = new Scanner(System.in);

int num = 1;

while(num != 0){
    System.out.println("Enter a number (0 to stop):");
    num = in.nextInt();
}
```

### ✔ Output (example)
```
Enter a number (0 to stop):
5
Enter a number (0 to stop):
10
Enter a number (0 to stop):
0
```

---

# 💡 Real-World Example – Password Retry

```java
String password = "java";
String input = "";

Scanner in = new Scanner(System.in);

while(!input.equals(password)){
    System.out.println("Enter password:");
    input = in.nextLine();
}

System.out.println("Access Granted!");
```

---

# ⭐ Summary

- While loop runs **as long as condition is true**  
- Must update variable inside loop  
- Use carefully to avoid infinite loops  

---

# 🔥 Practice Tasks

### Task 1  
Print numbers from **10 down to 1** using while loop.

### Task 2  
Keep asking user's name until they type `"stop"`.

### Task 3  
Find the sum of first **N** numbers using while loop (user gives N).
