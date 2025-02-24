In C language, operators are symbols that represent operations to be performed on one or more operands. They are the basic components of the C programming. In this article, we will learn about all the built-in operators in C with examples.

# What is a C Operator?
An operator in C can be defined as the symbol that helps us to perform some specific mathematical, relational, bitwise, conditional, or logical computations on values and variables. The values and variables used with operators are called operands. So we can say that the operators are the symbols that perform operations on operands.

![[Pasted image 20250222201206.png]]

For example,

```
c = a + b;
```

Here, ‘+’ is the operator known as the addition operator, and ‘a’ and ‘b’ are operands. The addition operator tells the compiler to add both of the operands ‘a’ and ‘b’.

# Types of Operators in C
C language provides a wide range of operators that can be classified into 6 types based on their functionality:

- Arithmetic Operators
- Relational Operators
- Logical Operators
- Bitwise Operators
- Assignment Operators
- Other Operators

## 1. Arithmetic Operations in C
The arithmetic operators are used to perform arithmetic/mathematical operations on operands. There are 9 arithmetic operators in C language:

| S. No. | Symbol | Operator | Description              | Syntax |
| ------ | ------ | -------- | ------------------------ | ------ |
| 1      | +      | Plus     | Adds two numeric values. | a + b  |
| 2      | -      | Minus    | Subtracts right operand from left operand. | a – b |
|3|*|Multiply|Multiply two numeric values.|a * b|
|4|/|Divide|Divide two numeric values.|a / b|
|5|%|Modulus|Returns the remainder after diving the left operand with the right operand.|a % b|
|6|+|Unary Plus|Used to specify the positive values.|+a|
|7|–|Unary Minus|Flips the sign of the value.|-a|
|8|++|Increment|Increases the value of the operand by 1.|a++|
|9|—|Decrement|Decreases the value of the operand by 1.|a–-
### Example of C Arithmetic Operators
```c
// C program to illustrate the arithmatic operators
#include <stdio.h>

int main()
{

    int a = 25, b = 5;

    // using operators and printing results
    printf("a + b = %d\n", a + b);
    printf("a - b = %d\n", a - b);
    printf("a * b = %d\n", a * b);
    printf("a / b = %d\n", a / b);
    printf("a % b = %d\n", a % b);
    printf("+a = %d\n", +a);
    printf("-a = %d\n", -a);
    printf("a++ = %d\n", a++);
    printf("a-- = %d\n", a--);

    return 0;
}

```
**Output**
```
a + b = 30
a - b = 20
a * b = 125
a / b = 5
a % b = 0
+a = 25
-a = -25
a++ = 25
a-- = 26
```
## 2. Relational Operators in C
The relational operators in C are used for the comparison of the two operands. All these operators are binary operators that return true or false values as the result of comparison.

These are a total of 6 relational operators in C:

|S. No.|Symbol|Operator|Description|Syntax|
| ---  | ---  | ---    | ---       |---   |
| 1|<|Less than|Returns true if the left operand is less than the right operand. Else false |a < b|
|2|>|Greater than|Returns true if the left operand is greater than the right operand. Else false|a > b|
|3|<=|Less than or equal|to	Returns true if the left operand is less than or equal to the right operand. Else false |a <= b|
|4|>=|Greater than or equal to|Returns true if the left operand is greater than or equal to right operand. Else false|a >= b|
|5|==|Equal to|Returns true if both the operands are equal.|a == b|
|6|!=|Not equal to|Returns true if both the operands are NOT equal.|a != b|

### Example of C Relational Operators
```C
// C program to illustrate the relational operators
#include <stdio.h>

int main()
{

    int a = 25, b = 5;

    // using operators and printing results
    printf("a < b  : %d\n", a < b);
    printf("a > b  : %d\n", a > b);
    printf("a <= b: %d\n", a <= b);
    printf("a >= b: %d\n", a >= b);
    printf("a == b: %d\n", a == b);
    printf("a != b : %d\n", a != b);

    return 0;
}
```
**Output**
```
a < b  : 0
a > b  : 1
a <= b: 0
a >= b: 1
a == b: 0
a != b : 1
```
Here, 0 means false and 1 means true.
## 3. Logical Operator in C
Logical Operators are used to combine two or more conditions/constraints or to complement the evaluation of the original condition in consideration. The result of the operation of a logical operator is a Boolean value either true or false.
### Example of Logical Operators in C
```c
// C program to illustrate the logical operators
#include <stdio.h>

int main()
{

    int a = 25, b = 5;

    // using operators and printing results
    printf("a && b : %d\n", a && b);
    printf("a || b : %d\n", a || b);
    printf("!a: %d\n", !a);

    return 0;
}

```
**Output**
```
a && b : 1
a || b : 1
!a: 0
```
## 4. Bitwise Operators in C
The Bitwise operators are used to perform bit-level operations on the operands. The operators are first converted to bit-level and then the calculation is performed on the operands. Mathematical operations such as addition, subtraction, multiplication, etc. can be performed at the bit level for faster processing.

There are 6 bitwise operators in C:

| S. No. | Symbol | Operator                 | Description                                                                            | Syntax |
| ------ | ------ | ------------------------ | -------------------------------------------------------------------------------------- | ------ |
| 1      | &      | Bitwise AND              | Performs bit-by-bit AND operation and returns the result.                              | a & b  |
| 2      | \|     | Bitwise OR               | Performs bit-by-bit OR operation and returns the result.                               | a \| b |
| 3      | ^      | Bitwise XOR              | Performs bit-by-bit XOR operation and returns the result.                              | a ^ b  |
| 4      | ~      | Bitwise First Complement | Flips all the set and unset bits on the number.                                        | ~a     |
| 5      | <<     | Bitwise Leftshift        | Shifts the number in binary form by one place in the operation and returns the result. | a << b |
| 6      | >>     | Bitwise Rightshilft      | Shifts the number in binary form by one place in the operation and returns the result. | a >> b |
### Example of Bitwise Operators

```c

// C program to illustrate the bitwise operators
#include <stdio.h>

int main()
{

    int a = 25, b = 5;

    // using operators and printing results
    printf("a & b: %d\n", a & b);
    printf("a | b: %d\n", a | b);
    printf("a ^ b: %d\n", a ^ b);
    printf("~a: %d\n", ~a);
    printf("a >> b: %d\n", a >> b);
    printf("a << b: %d\n", a << b);

    return 0;
}
```
Output
```
a & b: 1
a | b: 29
a ^ b: 28
~a: -26
a >> b: 0
a << b: 800
```
## 5. Assignment Operators in C
Assignment operators are used to assign value to a variable. The left side operand of the assignment operator is a variable and the right side operand of the assignment operator is a value. The value on the right side must be of the same data type as the variable on the left side otherwise the compiler will raise an error.

The assignment operators can be combined with some other operators in C to provide multiple operations using single operator. These operators are called compound operators.

In C, there are 11 assignment operators :

| S. No. | Symbol | Operator                | Description                                                                            | Syntax   |
|--------|--------|------------------------|----------------------------------------------------------------------------------------|---------|
| 1      | =      | Simple Assignment      | Assign the value of the right operand to the left operand.                             | a = b   |
| 2      | +=     | Plus and assign        | Add the right operand and left operand and assign this value to the left operand.      | a += b  |
| 3      | -=     | Minus and assign       | Subtract the right operand from the left operand and assign this value to the left operand. | a -= b  |
| 4      | *=     | Multiply and assign    | Multiply the right operand and left operand and assign this value to the left operand. | a *= b  |
| 5      | /=     | Divide and assign      | Divide the left operand by the right operand and assign this value to the left operand. | a /= b  |
| 6      | %=     | Modulus and assign     | Assign the remainder of the division of the left operand by the right operand to the left operand. | a %= b  |
| 7      | &=     | AND and assign         | Performs bitwise AND and assigns this value to the left operand.                        | a &= b  |
| 8      | \|=     | OR and assign          | Performs bitwise OR and assigns this value to the left operand.                         | a \|= b  |
| 9      | ^=     | XOR and assign         | Performs bitwise XOR and assigns this value to the left operand.                        | a ^= b  |
| 10     | >>=    | Right shift and assign | Performs bitwise right shift and assigns this value to the left operand.                | a >>= b |
| 11     | <<=    | Left shift and assign  | Performs bitwise left shift and assigns this value to the left operand.                 | a <<= b |
### Example of C Assignment Operators

```c
// C program to illustrate the assignment operators
#include <stdio.h>

int main()
{
    int a = 25, b = 5;

    // using operators and printing results
    printf("a = b: %d\n", a = b);
    printf("a += b: %d\n", a += b);
    printf("a -= b: %d\n", a -= b);
    printf("a *= b: %d\n", a *= b);
    printf("a /= b: %d\n", a /= b);
    printf("a %%= b: %d\n", a %= b);
    printf("a &= b: %d\n", a &= b);
    printf("a |= b: %d\n", a |= b);
    printf("a >>= b: %d\n", a >>= b); 
    printf("a <<= b: %d\n", a <<= b);

    return 0;
}
```
**Output**
```
a = b: 5 a += b: 10 a -= b: 5 a *= b: 25 a /= b: 5 a %= b: 0 a &= b: 0 a |= b: 5 a >>= b: 0 a <<= b: 0
```
## 6. Other Operators

Apart from the above operators, there are some other operators available in C that perform specific tasks. Some of them are discussed below:

### `sizeof` Operator

- The [[sizeof Operator]] is commonly used in C to determine the size of a variable or datatype.
- It is a compile-time unary operator.
- The result of `sizeof` is an unsigned integral type, usually denoted by `size_t`.

**Syntax**

```c
sizeof(operand)
```
### Comma Operator ( , )
- The [[comma in c|Comma operator]] (represented by the token) is a binary operator that evaluates its first operand and discards the result, it then evaluates the second operand and returns this value (and type).
- The comma operator has the lowest precedence of any C operator.
Comma acts as both operator and separator. 

**Syntax**

```
operand1 , operand2 
```
