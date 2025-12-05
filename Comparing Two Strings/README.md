# 🔤 String Comparison in Java (Simple Explanation)

In Java, **Strings are objects**, so we CANNOT compare them using `==` for content.  
We use **`.equals()`** to check if two strings have the same text.

---

# ❌ Wrong Way (Do NOT use)
```java
if(name1 == name2) {
    System.out.println("Same");
}
```
`==` checks **memory location**, NOT text/content.

---

# ✅ Correct Way – Use `.equals()`
```java
if(name1.equals(name2)) {
    System.out.println("Both strings are equal");
} else {
    System.out.println("Strings are different");
}
```

---

# 💻 Example with User Input

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter first name:");
        String name1 = in.nextLine();

        System.out.println("Enter second name:");
        String name2 = in.nextLine();

        if (name1.equals(name2)) {
            System.out.println("Both names are same");
        } else {
            System.out.println("Names are different");
        }
    }
}
```

---

# 🧠 Case-Sensitive vs Case-Insensitive

### ✔ Case-sensitive (A ≠ a)
```java
name1.equals(name2);
```

Example: `"Arctic"` and `"arctic"` are NOT equal.

### ✔ Case-insensitive (A = a)
```java
name1.equalsIgnoreCase(name2);
```

Example: `"Arctic"` and `"arctic"` ARE equal.

---

# 🎯 Sample Input
```
Arctic
arctic
```

## ✔ Sample Output (using equalsIgnoreCase)
```
Both names are same
```

---

# ⭐ Summary

- `==` → compares memory (DON'T USE for strings)  
- `.equals()` → compares text  
- `.equalsIgnoreCase()` → compares text ignoring upper/lower case  

---

# 🔥 Practice Task

Ask the user:
1. A username  
2. A confirmation username  

If both match (case-insensitive), print **“Login Successful”**  
Else print **“Try Again”**

# 🍎 String Pool vs Heap in Java (Simple Explanation)

In Java, Strings behave differently based on how they are created.

There are two ways:
1. **Using `new String("apple")`** → Creates a *new object in heap* every time  
2. **Using string literals `"apple"`** → Stored in the *String Pool*, reused to save memory  

---

# 💻 Code Example

```java
public class Main {
    public static void main(String args[]) {

        String f1 = new String("apple");
        String f2 = new String("apple");

        String a1 = "apple";
        String a2 = "apple";

        System.out.println(f1 == f2);     // false → different heap objects
        System.out.println(a1 == a2);     // true  → same string pool reference
        System.out.println(f1.equals(f2)); // true → both contain same text
    }
}
```

---

# 🧠 Explanation

### 🔹 1. `String f1 = new String("apple");`
- Creates a NEW object in **Heap memory**
- Even if same text exists, Java **creates a fresh object**
- So `f1 == f2` → **false**

### 🔹 2. `String a1 = "apple";`
- Java checks String Pool  
- If "apple" already exists, it **reuses the same memory**
- So `a1 == a2` → **true**

### 🔹 `.equals()` compares *content*
- `f1.equals(f2)` → **true** (text same)

---

# ✔️ Expected Output
```
false
true
true
```

---

# ⭐ Summary

| Comparison | Meaning | Why |
|-----------|---------|-----|
| `==` | compares memory address | f1 & f2 point to different heap objects |
| `.equals()` | compares text | “apple” = “apple” |
| String Literal | stored in String Pool | memory efficient |
| new String() | creates new object | always different reference |

---

# 🔥 Practice Task

Create:
- Two Strings using **new**
- Two Strings using **literals**

Print:
- `==` comparison  
- `.equals()` comparison  

Try to predict the output before running!
