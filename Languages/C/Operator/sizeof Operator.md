Sizeof is a much-used operator in the C. It is a compile-time unary operator which can be used to compute the size of its operand. The result of sizeof is of the unsigned integral type which is usually denoted by size_t. sizeof can be applied to any data type, including primitive types such as integer and floating-point types, pointer types, or compound datatypes such as Structure, union, etc.

Syntax:
```c
sizeof(Expression);
```
where ‘*Expression*‘ can be a data type or a variable of any type.

**Return**: It returns the size size of the given expression.

**Time Complexity:** O(1)
**Auxiliary Space**: O(1)

## Usage of sizeof() operator 
*sizeof()* operator is used in different ways according to the operand type. 

1. **When the operand is a Data Type:** When *sizeof()* is used with the data types such as int, float, char… etc it simply returns the amount of memory allocated to that data types. 
**Example:**
```c
// C Program To demonstrate
// sizeof operator
#include <stdio.h>
int main(){
    printf("Size of char: %lu bytes\n", sizeof(char));
    printf("Size of int: %lu bytes\n", sizeof(int));
    printf("Size of float: %lu bytes\n", sizeof(float));
    printf("Size of double: %lu bytes\n", sizeof(double));
    printf("Size of pointer: %lu bytes\n", sizeof(void *));
    return 0;
}
```
```
Output
Size of char: 1 bytes
Size of int: 4 bytes
Size of float: 4 bytes
Size of double: 8 bytes
Size of pointer: 8 bytes
```
 
> [!NOTE]
> sizeof() may give different output according to machine, we have run our programs on a 64-bit gcc compiler.




1. **When the operand is an expression:** When *sizeof()* is used with the expression, it returns the size of the expression. 
**Example:**
```c
// C Program To demonstrate
// operand as expression
#include <stdio.h>
int main()
{
    int a = 0;
    double d = 10.21;
    printf("%lu", sizeof(a + d));
    return 0;
}
```
Output
```
8
```
As we know from the first case size of int and double is 4 and 8 respectively, a is int variable while d is a double variable. The final result will be double, Hence the output of our program is 8 bytes.

## Type of operator
sizeof() is a compile-time operator. compile time refers to the time at which the source code is converted to a binary code. It doesn’t execute (run) the code inside (). 
**Example:**
```c
// C Program to illustrate
// that the 'sizeof' operator
// is a 'compile time operator'
#include <stdio.h>

int main(void)
{
    int y;
    int x = 11;

    // value of x doesn't change
    y = sizeof(x++);

    // prints 4 and 11
    printf("%i %i", y, x);

    return (0);
}
```
**Output**
```
4 11
```

If we try to increment the value of x, it remains the same. This is because x is incremented inside the parentheses and sizeof() is a compile-time operator. 
## Need of Sizeof 
1. **To find out the number of elements in an array:** Sizeof can be used to calculate the number of elements of the array automatically. 
**Example:**
```c
// C Program
// demonstrate the method
// to find the number of elements
// in an array
#include <stdio.h>
int main()
{
    int arr[] = { 1, 2, 3, 4, 7, 98, 0, 12, 35, 99, 14 };
    printf("Number of elements:%lu ",
           sizeof(arr) / sizeof(arr[0]));
    return 0;
}
```
**Output**
```
Number of elements:11 
```

1. **To allocate a block of memory dynamically:** sizeof is greatly used in dynamic memory allocation. For example, if we want to allocate memory that is sufficient to hold 10 integers and we don’t know the sizeof(int) in that particular machine. We can allocate with the help of sizeof. 
**Syntax:**
```c
int* ptr = (int*)malloc(10 * sizeof(int));
```
