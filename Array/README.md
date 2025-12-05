# 📦 Arrays in Java (Simple Explanation)

An **array** is used to store **multiple values** in a **single variable**.  
Example: 5 marks, 10 numbers, list of names, etc.

Instead of creating many variables:

```
int m1, m2, m3, m4, m5;
```

We can create ONE array:

```
int[] marks = {90, 85, 75, 88, 92};
```

---

# 🔹 Why Arrays?

- Store multiple values  
- Same datatype only  
- Access values using **index**  
- Index starts from **0**

Example:  
`marks[0]` → first value  
`marks[4]` → fifth value  

---

# 💻 Basic Example – Create & Print an Array

```java
public class Main {
    public static void main(String[] args) {

        int[] nums = {10, 20, 30, 40, 50};

        System.out.println(nums[0]); // 10
        System.out.println(nums[3]); // 40
    }
}
```

---

# 👉 Create Empty Array & Fill Values

```java
int[] arr = new int[5];

arr[0] = 11;
arr[1] = 22;
arr[2] = 33;
arr[3] = 44;
arr[4] = 55;
```

---

# 🔁 Using For Loop to Print Array

```java
int[] nums = {2, 4, 6, 8, 10};

for(int i = 0; i < nums.length; i++){
    System.out.println(nums[i]);
}
```

### ✔ Output
```
2
4
6
8
10
```

---

# 🌟 Using Enhanced For Loop (for-each)

```java
int[] nums = {5, 10, 15, 20};

for(int n : nums){
    System.out.println(n);
}
```

---

# 🧠 Array Length

Use `.length` to find size of array:

```java
System.out.println(nums.length);
```

---

# 💻 Real-World Example – Sum of All Array Values

```java
int[] marks = {85, 90, 75, 60, 95};
int sum = 0;

for(int i = 0; i < marks.length; i++){
    sum += marks[i];
}

System.out.println("Total = " + sum);
```

---

# ⭐ Summary

- Arrays store multiple values  
- Index starts at 0  
- Use `array[index]` to access  
- Use `array.length` to get size  
- Use loops to print or process arrays  

---

# 🔥 Practice Task

Create an array of 5 numbers and:

1. Print all values  
2. Print only even numbers  
3. Find the **maximum** number  
4. Find the **sum** of all numbers

 # 🔢 Array Example – Get 5 Numbers from User & Print Them

This program shows how to:

- Create an integer array  
- Get **5 inputs** from the user  
- Store them in the array  
- Print all values using a for loop  

This helps understand **arrays + loops + user input**.

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {
        
        Scanner in = new Scanner(System.in);

        int[] marks = new int[5];   // array of size 5

        // Taking input into array
        for (int i = 0; i < marks.length; i++) {
            marks[i] = in.nextInt();
        }

        // Printing array values
        for (int i = 0; i < marks.length; i++) {
            System.out.println(marks[i]);
        }
    }
}
```

---

## 🧠 How It Works

### ✔ Create array  
```
int[] marks = new int[5];
```

### ✔ Input using loop  
Each loop iteration reads one value:
```
marks[i] = in.nextInt();
```

### ✔ Print using loop  
```
System.out.println(marks[i]);
```

---

## 📌 Example Input
```
10
20
30
40
50
```

## ✔ Output
```
10
20
30
40
50
```

---

## ⭐ Why This Is Useful?

- Avoids writing 5 separate variables  
- Easily expand to 10, 50, or 100 values  
- Fast + clean code  

---

## 🔥 Practice Task

Create an array of 5 numbers and:
1. Print values  
2. Print only numbers greater than 50  
3. Count how many numbers are even  

# 🎯 Array Example – Find the Middle Element

This program performs:

1️⃣ Takes input for **size of the array**  
2️⃣ Reads all elements from the user  
3️⃣ Finds the **middle index**  
4️⃣ Prints the **middle element** in the array  

---

## 💻 Code Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String args[]) {

        Scanner in = new Scanner(System.in);

        System.out.println("Enter the size of the array:");
        int size = in.nextInt();

        int[] num = new int[size];

        System.out.println("Enter the numbers:");
        for (int i = 0; i < num.length; i++) {
            num[i] = in.nextInt();
        }

        int midIndex = size / 2;      // middle index
        int midElement = num[midIndex]; // actual middle element

        System.out.println("Middle index: " + midIndex);
        System.out.println("Middle element: " + midElement);
    }
}
```

---

## 🧠 Explanation

### ✔ Step 1: Get size  
User decides array size.

### ✔ Step 2: Fill array  
Loop stores user input values.

### ✔ Step 3: Find middle  
Middle index = `size / 2`  
(Works for both even & odd sizes)

### ✔ Step 4: Print middle element  
`num[midIndex]`

---

## 📌 Example Input
```
Enter the size of the array:
5
Enter the numbers:
10
20
30
40
50
```

## ✔ Output
```
Middle index: 2
Middle element: 30
```

---

## ⭐ Notes

- Array indexing starts from **0**  
- Middle element is the one at `index = size/2`  
- Example: size = 5 → mid index = 2 (3rd element)

---

## 🔥 Practice Task

Ask the user for:
- Even-sized array  
- Print the **two middle elements**  
(e.g., array size = 6 → print elements at index 2 and 3)


  
