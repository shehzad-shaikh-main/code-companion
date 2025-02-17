---
Links: "[[Infinite do while loop code]]"
---

```C
// C program to demonstrate 
// infinite loop using do-while 
// loop
#include <stdio.h>

// Driver code
int main()
{
  do 
  {
    printf("This loop will run forever.\n");
  } while (1);
  
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