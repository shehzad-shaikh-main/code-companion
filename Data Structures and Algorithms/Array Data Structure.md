****Array**** is a collection of items of the same variable type that are stored at contiguous memory locations. It is one of the most popular and simple data structures used in programming.

## Basic terminologies of Array

- ****Array Index:**** In an array, elements are identified by their indexes. Array index starts from 0.
- ****Array element:**** Elements are items stored in an array and can be accessed by their index.
- ****Array Length:**** The length of an array is determined by the number of elements it can contain. 

## Memory representation of Array

In an array, all the elements are stored in contiguous memory locations. So, if we initialize an array, the elements will be allocated sequentially in memory. This allows for efficient access and manipulation of elements.

![Memory-Representation-of-Array-(1)](https://media.geeksforgeeks.org/wp-content/uploads/20240405101013/Memory-Representation-of-Array-(1).webp)

## Declaration of Array

Arrays can be declared in various ways in different languages. For better illustration, below are some language-specific array declarations:

[[Declaration of Arrays]]

## Initialization of Array

Arrays can be initialized in different ways in different languages. Below are some language-specific array initializations:

[[Initialization of Array]]

## Why do we Need Arrays?

Assume there is a class of five students and if we have to keep records of their marks in examination then, we can do this by declaring five variables individual and keeping track of records but what if the number of students becomes very large, it would be challenging to manipulate and maintain the data.

What it means is that, we can use normal variables (v1, v2, v3, ..) when we have a small number of objects. But if we want to store a large number of instances, it becomes difficult to manage them with normal variables. The idea of an array is to represent many instances in one variable.
![[Pasted image 20250217182241.jpg]]
## Types of Arrays
Arrays can be classified in two ways:

- On the basis of Size
- On the basis of Dimensions
![[Pasted image 20250217182319.jpg]]

## Types of Arrays on the basis of Size:
### 1.Fixed Sized Arrays:

We cannot alter or update the size of this array. Here only a fixed size (i,e. the size that is mentioned in square brackets `[]`) of memory will be allocated for storage. In case, we don’t know the size of the array then if we declare a larger size and store a lesser number of elements will result in a wastage of memory or we declare a lesser size than the number of elements then we won’t get enough memory to store all the elements. In such cases, static memory allocation is not preferred.

[[Fixed sized array code example]]

### 2.Dynamic Sized Arrays:

The size of the array changes as per user requirements during execution of code so the coders do not have to worry about sizes. They can add and removed the elements as per the need. The memory is mostly dynamically allocated and de-allocated in these arrays.

[[Dynamic sized array code example]]

## Types of Arrays on the basis of Dimensions:
### 1. **One-dimensional Array(1-D Array):**
You can imagine a 1d array as a row, where elements are stored one after another.
![[Pasted image 20250217182637.jpg]]
### 2.**Multi-dimensional Array:** 
A multi-dimensional array is an array with more than one dimension. We can use multidimensional array to store complex data in the form of tables, etc. We can have 2-D arrays, 3-D arrays, 4-D arrays and so on.
- [[Two-Dimensional Array(2-D Array or Matrix)]] 2-D Multidimensional arrays can be considered as an array of arrays or as a matrix consisting of rows and columns.
    ![[Pasted image 20250217182931.jpg]]
- **Three-Dimensional Array(3-D Array)**: A 3-D Multidimensional array contains three dimensions, so it can be considered an array of two-dimensional arrays.
    ![[Pasted image 20250217183014.jpg]]
    
## Operations on Array
### 1. Array Traversal:
Array traversal involves visiting all the elements of the array once. Below is the implementation of Array traversal in different Languages:
[[Array traversal code example]]