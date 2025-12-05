# 🔁 For-Each Loop in Java (Simple Explanation)

The **for-each loop** (also called *enhanced for loop*) is used to easily loop through arrays.

It is simpler and cleaner than the normal `for` loop.

---

# 🧩 Syntax

```java
for(dataType variable : arrayName) {
    // use variable
}
```

- `variable` → each element in the array  
- `arrayName` → the array you want to loop through  

---

# 💻 Example 1 – Print All Array Elements

```java
public class Main {
    public static void main(String[] args) {

        int[] nums = {10, 20, 30, 40, 50};

        for(int n : nums) {
            System.out.println(n);
        }
    }
}
```

### ✔ Output
```
10
20
30
40
50
```

---

# 💻 Example 2 – For-Each Loop With Strings

```java
String[] names = {"Arctic", "Kavin", "Sanjai"};

for(String name : names) {
    System.out.println(name);
}
```

---

# 💻 Example 3 – Sum of Array Values

```java
int[] marks = {80, 90, 75, 60};

int sum = 0;

for(int m : marks) {
    sum += m;
}

System.out.println("Total = " + sum);
```

---

# ⭐ Why Use For-Each Loop?

- No need to use index  
- Cleaner syntax  
- Avoids mistakes in indexing  
- Perfect for reading all array values  

---

# ⚠ When NOT to Use For-Each

You should not use for-each loop when:
- You need the **index number**  
- You want to **modify** array elements  
- You want to skip specific indexes  

In such cases, use normal `for` loop.

---

# 🔥 Practice Tasks

### ✔ Task 1  
Use for-each to print all even numbers from an array.

### ✔ Task 2  
Use for-each to find the **maximum** number in an array.

### ✔ Task 3  
Use for-each to print all names starting with the letter **A**.

