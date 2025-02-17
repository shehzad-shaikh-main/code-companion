---
chosen_subject: C
---

A **for loop** is a repetition control structure that allows us to write a loop that is executed a specific number of times. It is an entry-controlled loop that enables us to perform n number of steps together in one line.
[[For Loop Code Syntax]]

The various ****parts of the for loop**** are:

- ****Initialization****: Initialize the loop variable to some initial value.
- ****Test Condition****: This specifies the test condition. If the condition evaluates to true, then body of the loop is executed, and loop variable is updated according to update expression. If evaluated false, loop is terminated.
- ****Update Expression****: After executing the loop body, this expression increments/decrements the loop variable by some value.

### for loop Flowchart
![[Pasted image 20250217150933.png]]

Example:
[[For Loop Code Example]]

### Important Properties of for Loop

- The initialization and updation statements can perform operations unrelated to the condition statement, or nothing at all – if you wish to do. But the good practice is to only perform operations directly relevant to the loop.
- A variable declared in the initialization statement is visible only inside the scope of the for loop and will be released out of the loop.
- Don’t forget that the variable which was declared in the initialization statement can be modified during the loop, as well as the variable checked in the condition.

### Range Based for Loop

There is a type of for loop that does not need the condition and updation statement. It is called ****range based for loop**** and it can only be used for iteratable objects such as vector, set, etc. For a vector named v, it can be written to print its elements as:

[[Range Based for Loop Code]]

Output:
```Output
1
2
3
4
5
```
