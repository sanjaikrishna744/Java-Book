# 🔐 Access Modifiers in Java (Simple Explanation)

Access Modifiers decide **who can access what** in your program.

Java has **four** main access modifiers:

| Modifier     | Access Level | Where Accessible? |
|--------------|--------------|--------------------|
| `public`     | Everywhere   | Same class, same package, different package |
| `private`    | Only inside class | Same class ONLY |
| `protected`  | Class + Same package + Subclass (even in different package) |
| *default* (no keyword) | Package-level | Same package only |

---

# ⭐ 1. `public` – Accessible Everywhere

```java
public class A {
    public int num = 10;
}
```

✔ Same class  
✔ Same package  
✔ Other packages  
✔ Through inheritance  
✔ Through objects  

---

# ⭐ 2. `private` – Accessible ONLY Inside the Same Class

```java
class A {
    private int secret = 555;

    private void show() {
        System.out.println("Private method");
    }
}
```

❌ Cannot be accessed outside the class  
✔ Use getter/setter if needed

---

# ⭐ 3. `protected` – Accessible in:

✔ Same class  
✔ Same package  
✔ Subclasses (even in another package)

```java
class A {
    protected int value = 20;
}

class B extends A {
    void display() {
        System.out.println(value); // allowed
    }
}
```

---

# ⭐ 4. Default (No keyword) – Package Level Access

```java
class A {
    int data = 5;   // default access
}
```

✔ Same package  
❌ Different package

---

# 💻 Example – All Four Modifiers in One Program

```java
class A {

    public int a = 1;
    private int b = 2;
    protected int c = 3;
    int d = 4; // default

    public void method1() {
        System.out.println("Public method");
    }

    private void method2() {
        System.out.println("Private method");
    }

    protected void method3() {
        System.out.println("Protected method");
    }

    void method4() {
        System.out.println("Default method");
    }
}

class B extends A {

    void show() {
        System.out.println(a);  // public - allowed
        // System.out.println(b); // private - NOT allowed
        System.out.println(c);  // protected - allowed
        System.out.println(d);  // default - allowed (same package)
    }
}

public class Main {
    public static void main(String[] args) {

        B obj = new B();
        obj.show();
    }
}
```

---

# ✔ Output
```
1
3
4
```

(Private data is NOT accessible.)

---

# ⭐ Summary Table

| Modifier | Same Class | Same Package | Subclass | Other Package |
|---------|------------|--------------|----------|----------------|
| public | ✔ | ✔ | ✔ | ✔ |
| private | ✔ | ❌ | ❌ | ❌ |
| protected | ✔ | ✔ | ✔ | ❌ (only through inheritance) |
| default | ✔ | ✔ | ❌ | ❌ |

---

# 🔥 Practice Tasks

### ✔ Task 1  
Create a class `BankAccount` with:
- private balance  
Create methods deposit() and withdraw() to control access.

### ✔ Task 2  
Create class `Vehicle` with protected variable `brand`.  
Access it in child class `Car`.

### ✔ Task 3  
Create class `Person` with default variable age.  
Try accessing it from another package.

