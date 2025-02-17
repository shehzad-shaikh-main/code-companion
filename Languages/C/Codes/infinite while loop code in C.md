---
Links: "[[Infinite while loop code]]"
---
```C
// C program to demonstrate 
// infinite loop using while 
// loop
#include <stdio.h>
 
// Driver code
int main() 
{
  while (1)
    printf("This loop will run forever.\n");
  return 0;
}

```
**Output:**
```Output
This loop will run forever.  
This loop will run forever.  
This loop will run forever.  
...
```