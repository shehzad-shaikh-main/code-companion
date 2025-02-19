## **What is a Variable?**  
A **variable** is a named storage location in the memory that holds a value. Think of it like a box that holds information. It has a name and stores a value that can be used later in a program.  

### **Example:**  
Imagine you have a notebook, and you write your age in it. If your age changes, you erase the old number and write the new one. A variable works the same way!  

---

## **How to Create a Variable?**  
Different programming languages have different ways to create variables.  

### **Example in Python:**  
```Python
name = "Shehzad"  # Stores the text "Shehzad" in a variable called name  
age = 20  # Stores the number 20 in a variable called age  
```

### **Example in C:**  
```C
int age = 20;  // Stores the number 20 in a variable called age
char grade = 'A';  // Stores the letter 'A' in a variable called grade  

### **Example in Java:**  
String name = "Shehzad";  // Stores the text "Shehzad" in a variable called name  
double pi = 3.14;  // Stores the number 3.14 in a variable called pi  
```
---

## **Rules for Naming Variables**  
When creating a variable, follow these rules:  
1. Use letters, numbers, or underscores (`_`).  
2. The name should start with a letter or an underscore.  
3. The name **cannot** start with a number.  
4. No spaces or special symbols (@, #, %, etc.).  

### **Good Variable Names:**  
-  `student_name`  
-  `count1`  
-  `_result`  

### **Bad Variable Names:**  
-  `1number` (Starts with a number)  
-  `total cost` (Has a space)  
-  `if` (Reserved word in programming)  

---

## **Types of Variables**  
There are different kinds of variables based on what they store:  
- **Numbers** → `10`, `3.14`, `-5`  
- **Text** → `"Hello"`, `"Python"`
- **True/False (Boolean)** → `true`, `false`  

### **Example in Python:**  
```Python
price = 100  # Stores a number  
message = "Welcome!"  # Stores text  
is_open = True  # Stores True or False  
```
---

## **Where Can Variables Be Used? (Scope)**  
- **Local Variable** → Used inside a function (temporary).  
- **Global Variable** → Used everywhere in the program.  

### **Example:**  
```python
global_message = "Hello, World!"  # Global Variable  

def greet():  
	local_message = "Hi!"  # Local Variable  
	print(local_message)  

greet()  
print(global_message)  
```
---

## **Summary**  
-  A variable stores information in a program.  
-  Different languages have different ways to create variables.  
-  Variable names should follow specific rules.  
-  Variables can store numbers, text, and True/False values.  
-  Some variables are used only inside functions (local), while others can be used everywhere (global).  

