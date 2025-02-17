---
Links: "[[Do while loop code example]]"
---
```C
// C program to illustrate 
// do-while loop
#include <stdio.h>
 
// Driver code
int main()
{
  // Initialization expression
  int i = 2; 
  
  do
  {
    // loop body
    printf( "Hello World\n");   
 
    // Update expression
    i++;
    
    // Test expression
  }  while (i < 1);   
  
  return 0;
}

```
output:
```Output
Hello World
```