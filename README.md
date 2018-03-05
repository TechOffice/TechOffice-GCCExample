# TechOffice-GCCExample


## GCC 
GNU Compiler Collection (GCC) is compiler system for GNU project which include many compilers for different programming language. 

### Window 
GCC is not designed for Windows. Thankfully, there are many vendor which ported GCC to Windows.

* MingGW
* Cygwin

#### Cygwin

set the PATH include the bin of Cygwin.

e.g. 
```
set PATH=%PATH%;C:\cygwin64\bin
```

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