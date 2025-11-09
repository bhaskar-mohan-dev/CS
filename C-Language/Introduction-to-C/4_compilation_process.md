# ⚙️ Compilation Process in C
> **Author:** Bhaskar Mohan  
> **Date:** 2025-11-09  
> **Category:** Programming Languages → C  

---

## 🧩 Overview
The compilation process in C converts human-readable source code (.c file) into an executable program.  
It proceeds through five major stages:

1. Preprocessing  
2. Compilation  
3. Assembly  
4. Linking  
5. Execution  

---

## 🧱 Overall Flow
Source Code (.c)  
↓  
Preprocessing → expands macros and includes headers  
↓  
Compilation → converts to assembly code  
↓  
Assembly → generates object file (.o / .obj)  
↓  
Linking → combines object files and libraries  
↓  
Execution → runs the final program  

---

## 1️⃣ Preprocessing
• The first phase, handled by the C preprocessor.  
• Processes all lines starting with # before compilation.  
• Main tasks:  
  – Include header files (#include <stdio.h>)  
  – Replace macros (#define)  
  – Remove comments and extra spaces  
  – Handle conditional compilation (#ifdef, #endif)  

Example:
#include <stdio.h>  
#define PI 3.14  
int main() { printf("%f", PI); return 0; }  

Output: Expanded source code.  

---

## 2️⃣ Compilation
• The compiler translates preprocessed source into assembly language.  
• Performs syntax checking, type checking, and optimization.  
• Errors like missing semicolons or undeclared variables occur here.  
• Produces an assembly file (.s).  

Command: gcc -S program.c  
Output: program.s (assembly code).  

---

## 3️⃣ Assembly
• The assembler converts assembly code into object code (binary).  
• Generates program.o which contains machine instructions.  
• Object files are not human-readable.  

Command: gcc -c program.c  
Output: program.o (object file).  

---

## 4️⃣ Linking
• Linker joins all object files and library code into one executable.  
• Resolves function calls such as printf() from stdio.h.  
• Missing references cause linker errors (undefined reference).  

Command: gcc program.o -o program  
Output: program (executable file).  

---

## 5️⃣ Execution
• Loader loads the executable into main memory for execution.  
• CPU begins execution from main().  
• OS allocates memory for code, stack, heap, and data segments.  

Run: ./program  
Output: Sum = 30  

---

## 🧠 Summary Table
Phase | Tool Used | Input | Output | Purpose  
------|------------|--------|---------|----------  
Preprocessing | Preprocessor | Source (.c) | Expanded source | Handle macros, includes  
Compilation | Compiler | Expanded source | Assembly (.s) | Syntax check, optimization  
Assembly | Assembler | Assembly code | Object (.o) | Convert to machine code  
Linking | Linker | Object files + Libraries | Executable | Combine and resolve references  
Execution | Loader | Executable | Running program | Load into memory and execute  

---

## 💡 Key Points
• Each phase’s output becomes input for the next.  
• Compilation errors = syntax or type errors.  
• Linking errors = undefined references.  
• Runtime errors occur after execution starts.  
• The full process can be run automatically:  
  gcc program.c -o program  

---

## 🧪 Practice
1. Compile a program using gcc -E, gcc -S, gcc -c, and gcc to observe each phase.  
2. Identify which stage checks syntax.  
3. What happens if printf() is not linked?  
4. Difference between object file and executable file.  
5. Explain loader’s role in execution.  

---

## 🔗 References
• The C Programming Language — Dennis Ritchie & Brian Kernighan  
• GNU GCC Documentation  
• GeeksforGeeks — Compilation Process in C  
• TutorialsPoint — Compilation Phases in C  
