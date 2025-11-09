# 🧠 Structure of a C Program
> **Author:** Bhaskar Mohan  
> **Date:** 2025-11-09  
> **Category:** Programming Languages → C  

---

## 🧩 Overview
Every C program follows a fixed structure that determines how the code is organized, compiled, and executed.  
It contains several main sections — from including header files to defining the `main()` function and writing executable statements.  
Understanding this structure ensures clarity, readability, and smooth compilation.

Key Point:  
The C compiler always begins execution from the `main()` function.

---

## 🧱 Basic Structure
A typical C program has these sections (in order):

1. Documentation Section  
2. Link Section (#include)  
3. Global Declaration Section  
4. main() Function  
   - Declaration Part  
   - Executable Part  
5. Subprogram Section (User-defined Functions)

---

## ⚙️ Example
#include <stdio.h>   // Link section  
// Program to add two numbers  

int main() {  
 int a = 10, b = 20;     // Declaration part  
 int sum = a + b;        // Executable part  
 printf("Sum = %d", sum);  
 return 0;               // End of program  
}

---

## 🧠 Explanation of Each Section

### 1. Documentation Section
- Used for comments describing the program, purpose, or author details.  
- Only for human readability — ignored by the compiler.  
- Example:  
  // Program to add two numbers  

---

### 2. Link Section (#include)
- Used to include header files that provide predefined functions.  
- These are processed before actual compilation.  
- Example:  
  #include <stdio.h> → for input/output functions like printf(), scanf()  
  #include <math.h> → for mathematical operations like sqrt(), pow()  
- Note: Directives starting with `#` are handled by the preprocessor before compilation.

---

### 3. Global Declaration Section
- Contains variables or functions declared globally, accessible throughout the program.  
- Declared before `main()`.  
- Example:  
  int count = 0;   // global variable  

---

### 4. main() Function
- The entry point of every C program.  
- Every valid program must have one main() function.  
- Syntax:  
  int main() {  
  // Declarations  
  // Executable statements  
  return 0;  
  }  
- Execution starts from the first statement inside main().  
- The statement `return 0;` indicates successful termination.  

Example:  
#include <stdio.h>  
int main() {  
 printf("Hello, World!");  
 return 0;  
}

---

### 5. Declaration Part
- Declares all variables used in the program.  
- Must come before any executable statement.  
- Example:  
  int a, b, sum;  

---

### 6. Executable Part
- Contains the logic or main operations of the program — calculations, loops, conditions, etc.  
- Example:  
  sum = a + b;  
  printf("Sum = %d", sum);  
- Declaration and executable statements together form the body of the main() function.

---

### 7. Subprogram Section (User-defined Functions)
- Optional section used to define custom functions below main().  
- Helps modularize and reuse code.  
- Example:  
  void greet() {  
 printf("Hello, World!");  
  }  

---

## 🧠 Summary
A C program starts by including header files, moves into the main() function, executes declarations and statements, and may call user-defined functions.  
This structured layout ensures clarity, modularity, and successful compilation.

---

## 🧪 Practice
1. Write a simple program that prints your name using proper structure.  
2. Explain the purpose of the `#include` directive.  
3. What happens if `return 0;` is removed from main()?  
4. Write a program using both global and local variables — explain the difference.  
5. Create a C program that uses one user-defined function below main().

---

## 🔗 References
- *The C Programming Language* — Dennis Ritchie & Brian Kernighan  
- GNU C Documentation  
- GeeksforGeeks — Structure of C Program  
- TutorialsPoint — C Basics
