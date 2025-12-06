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

# 🔐 Access Modifiers – Which Is Accessible? (Simple Example)

This example shows **which variables can be accessed** from a child class object based on **access modifiers**.

---

## 💻 Code Example

```java
class Person {

    public String name;                // public → accessible everywhere
    protected int age;                 // protected → accessible in subclass
    private String socialSecurityNumber; // private → ONLY inside Person class
    String address;                    // default → same package only

    Person(String name, int age, String ssn, String address) {
        this.name = name;
        this.age = age;
        this.socialSecurityNumber = ssn;
        this.address = address;
    }
}

class Employee extends Person {

    Employee(String name, int age, String ssn, String address) {
        super(name, age, ssn, address);
    }
}

public class Main {
    public static void main(String[] args) {

        Employee e1 = new Employee("Arctic", 20, "IQ23S", "Erode");

        System.out.println(e1.name);      // ✅ allowed (public)
        System.out.println(e1.age);       // ✅ allowed (protected)
        // System.out.println(e1.socialSecurityNumber); ❌ ERROR
        System.out.println(e1.address);   // ✅ allowed (default, same package)
    }
}
```

---

## ❌ Compile-Time Error Explanation

```java
System.out.println(e1.socialSecurityNumber);
```

❌ ERROR because:

- `socialSecurityNumber` is **private**
- Private variables are accessible **ONLY inside the same class**
- Even a child class **cannot access private data**

---

## ✅ Correct Output (After Commenting Private Access)

```
Arctic
20
Erode
```

---

## 🧠 Access Modifier Rules (Quick Table)

| Modifier | Same Class | Subclass | Same Package | Other Package |
|--------|------------|----------|--------------|---------------|
| public | ✅ | ✅ | ✅ | ✅ |
| protected | ✅ | ✅ | ✅ | ❌ |
| default | ✅ | ❌ | ✅ | ❌ |
| private | ✅ | ❌ | ❌ | ❌ |

---

## ✅ How to Access `private` Variable Properly?

Use **getter method** inside the class.

```java
class Person {
    private String socialSecurityNumber;

    public String getSSN() {
        return socialSecurityNumber;
    }
}
```

Then access like:

```java
System.out.println(e1.getSSN());
```

---

## ⭐ Key Takeaways

- `public` → everywhere  
- `protected` → subclass allowed  
- `default` → same package only  
- `private` → SAME CLASS ONLY  
- Private data needs **getter/setter**

---

## 🔥 Practice Task

1. Make `balance` private in `BankAccount`
2. Create `deposit()` and `getBalance()` methods
3. Try accessing balance directly → observe error
4. Access using method → works ✅

