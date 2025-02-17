---
links: "[[Infinite for loop code]]"
---

```C
// C program to demonstrate infinite
// loops using for loop
#include <stdio.h>
 
// Driver code
int main ()
{
  int i;
  
  // This is an infinite for loop 
  // as the condition expression 
  // is blank
  for ( ; ; )
  {
    printf("This loop will run forever.\n");
  }
  
  return 0;
}

```
Output:
```C
This loop will run forever.  
This loop will run forever.  
This loop will run forever.  
........
```