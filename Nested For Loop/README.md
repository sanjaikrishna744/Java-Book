# 🔁 Nested For Loop in Java (Simple Explanation)

A **nested for loop** means a for loop **inside another for loop**.  
Used for:
- Patterns  
- Tables  
- Matrix operations  
- Working with 2D data  

In nested loops:

```
Outer loop → controls rows  
Inner loop → controls columns
```

---

# 💻 Example 1 – Print a 3×3 Grid of Numbers

```java
for (int i = 1; i <= 3; i++) {        // outer loop (rows)
    for (int j = 1; j <= 3; j++) {    // inner loop (columns)
        System.out.print(j + " ");
    }
    System.out.println(); // new line after each row
}
```

### ✔ Output
```
1 2 3
1 2 3
1 2 3
```

---

# 💻 Example 2 – Star Pattern (Triangle)

```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

### ✔ Output
```
* 
* * 
* * * 
* * * * 
* * * * * 
```

---

# 📦 Example 3 – Multiplication Table Using Nested Loop

```java
for (int i = 1; i <= 5; i++) {  
    for (int j = 1; j <= 10; j++) {
        System.out.println(i + " x " + j + " = " + (i * j));
    }
    System.out.println("-----------");
}
```

---

# 🧠 How Nested Loops Work?

Example:
```
for i = 1 → inner loop runs fully  
for i = 2 → inner loop runs fully  
for i = 3 → inner loop runs fully  
```

Total runs = `outerLoop × innerLoop`

---

# ⭐ Real-World Uses

- Printing patterns  
- Tables  
- Working with 2D arrays  
- Game development (grids)  
- Matrix multiplication  

---

# 🔥 Practice Tasks

### Task 1  
Print a square pattern of `#` of size 4:
```
####
####
####
####
```

### Task 2  
Print numbers like this:

```
1  
1 2  
1 2 3  
1 2 3 4  
```

### Task 3  
Print a multiplication table from **1 to 3** using nested loops.

# 🔁 More Nested For Loop Examples (Easy + Useful)

Nested loops help print patterns, grids, tables, and more.  
Here are extra examples to understand them clearly.

---

# 💻 Example 1 – Rectangle Pattern

```java
for (int i = 1; i <= 4; i++) {        // 4 rows
    for (int j = 1; j <= 6; j++) {    // 6 columns
        System.out.print("* ");
    }
    System.out.println();
}
```

### ✔ Output
```
* * * * * *
* * * * * *
* * * * * *
* * * * * *
```

---

# 💻 Example 2 – Number Triangle

```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print(j + " ");
    }
    System.out.println();
}
```

### ✔ Output
```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

---

# 💻 Example 3 – Reverse Number Triangle

```java
for (int i = 5; i >= 1; i--) {
    for (int j = 1; j <= i; j++) {
        System.out.print(j + " ");
    }
    System.out.println();
}
```

### ✔ Output
```
1 2 3 4 5
1 2 3 4
1 2 3
1 2
1
```

---

# 💻 Example 4 – Hollow Square Pattern

```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= 5; j++) {
        if (i == 1 || i == 5 || j == 1 || j == 5)
            System.out.print("* ");
        else
            System.out.print("  ");
    }
    System.out.println();
}
```

### ✔ Output
```
* * * * *
*       *
*       *
*       *
* * * * *
```

---

# 💻 Example 5 – X Pattern (Cross Pattern)

```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= 5; j++) {
        if (i == j || i + j == 6)
            System.out.print("* ");
        else
            System.out.print("  ");
    }
    System.out.println();
}
```

### ✔ Output
```
*       *
  *   *
    *
  *   *
*       *
```

---

# 💻 Example 6 – Multiplication Grid (1 to 5)

```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= 5; j++) {
        System.out.print((i * j) + "\t");
    }
    System.out.println();
}
```

### ✔ Output
```
1   2   3   4   5
2   4   6   8   10
3   6   9   12  15
4   8   12  16  20
5   10  15  20  25
```

---

# 💡 Quick Rules for Nested Loops

- Outer loop → rows  
- Inner loop → columns  
- Total loops executed = **outer × inner**  
- Perfect for patterns + tables  

---

# 🔥 Practice Tasks

### Task 1  
Print this pattern:

```
*
* *
* * *
* * * *
```

### Task 2  
Print this number pattern:

```
5
5 4
5 4 3
5 4 3 2
5 4 3 2 1
```

### Task 3  
Print a **hollow triangle** using nested loops.


