# GCC Hello World Example

## Step to create Hello World Program 

Create a hello.c 
```
#include <stdio.h>

int
main (void)
{
  printf ("Hello, world!\n");
  return 0;
}
```

Compile
```
gcc hello.c -o hello.exe
```

Then it would generate hello.exe

```
./hello.exe
```

output
```
Hello, world!
```

## Cygwin

set the PATH include the bin of Cygwin.

e.g. 
```
set PATH=%PATH%;C:\cygwin64\bin
```