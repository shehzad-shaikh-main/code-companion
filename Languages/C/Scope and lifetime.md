## Scope and Lifetime of Variables in C  

In C programming, **scope** and **lifetime** define where and how long a variable exists in memory. Understanding these concepts ensures efficient memory management and prevents unexpected behavior in programs.  

---

### **Scope of Variables**  
The **scope** of a variable determines where it can be accessed in a program. There are four main types of scope in C:  

1. **Local Scope** – The variable is declared inside a function and is accessible only within that function.  
2. **Global Scope** – The variable is declared outside all functions and is accessible throughout the program.  
3. **Block Scope** – The variable is declared inside a block (`{}`), and its accessibility is limited to that block.  
4. **File Scope** – The variable is declared with `static` outside a function and is accessible only within the same file.  

#### **Local Scope**  
A variable declared inside a function is **local** to that function and cannot be accessed outside of it.  
```c
#include <stdio.h>

void function() {  
    int x = 10; // Local variable  
    printf("%d", x);  
}  

int main() {  
    function();  
    // printf("%d", x); // Error: x is not accessible here  
    return 0;  
}  
```
- The variable `x` exists only inside `function()`.  
- Trying to access it outside the function causes a compilation error.  

#### **Global Scope**  
A variable declared outside all functions is **global** and can be accessed from any function in the program.  
```c
#include <stdio.h>

int globalVar = 50; // Global variable  

void function() {  
    printf("%d", globalVar); // Accessible here  
}  

int main() {  
    function();  
    printf("%d", globalVar); // Accessible here too  
    return 0;  
}  
```
- `globalVar` is accessible in both `main()` and `function()`.  
- Modifying it in one function affects its value globally.  

#### **Block Scope**  
A variable declared inside a specific block `{}` is only accessible within that block.  
```C
#include <stdio.h>

int main() {  
    if (1) {  
        int blockVar = 20; // Block-scoped variable  
        printf("%d", blockVar);  
    }  
    // printf("%d", blockVar); // Error: blockVar is out of scope  
    return 0;  
}  
```
- `blockVar` exists only inside the `if` block.  
- It cannot be accessed outside the block.  

#### **File Scope**  
A variable declared as `static` outside all functions is **restricted to the file** in which it is defined.  
```C
static int fileVar = 100; // File-scoped variable  
void function() {  
    printf("%d", fileVar); // Accessible within this file  
}
```
- `fileVar` is accessible within the same file but **not in other files** if included in a multi-file program.  

---

### **Lifetime of Variables**  
The **lifetime** of a variable defines how long it exists in memory. In C, there are three main storage durations:  

1. **Automatic Storage Duration** – The variable is created when the function/block is entered and destroyed when it exits.  
2. **Static Storage Duration** – The variable exists for the entire program execution.  
3. **Dynamic Storage Duration** – The variable is allocated and deallocated manually using `malloc()` and `free()`.  

#### **Automatic Storage Duration (Default for Local Variables)**  
Local variables in C have **automatic** storage duration, meaning they are created when the function is called and destroyed when it returns.  
```C

void function() {  
    int x = 10; // Created when function is called  
    printf("%d", x);  
} // x is destroyed here  
```
#### **Static Storage Duration**  
Variables with `static` storage duration exist throughout the program execution, even if declared inside a function.  
```C
#include <stdio.h>

void function() {  
    static int x = 0; // Retains value between function calls  
    x++;  
    printf("%d ", x);  
}  

int main() {  
    function(); // Output: 1  
    function(); // Output: 2  
    function(); // Output: 3  
    return 0;  
}  
```
- `x` is only initialized once and retains its value across function calls.  

#### **Dynamic Storage Duration**  
Dynamic variables are allocated at runtime using `malloc()` and freed using `free()`.  
```C
#include <stdio.h>  
#include <stdlib.h>  

int main() {  
    int *ptr = (int *)malloc(sizeof(int)); // Dynamically allocated memory  
    *ptr = 10;  
    printf("%d", *ptr);  
    free(ptr); // Freeing memory to prevent memory leaks  
    return 0;  
}  
```
- `malloc()` allocates memory dynamically.  
- `free()` releases the allocated memory to prevent memory leaks.  

---

### **Conclusion**  
Understanding **scope** helps determine where variables can be accessed, while **lifetime** determines how long they exist. Proper management of variable scope and lifetime ensures better memory usage, avoids unintended modifications, and prevents memory leaks in C programs.