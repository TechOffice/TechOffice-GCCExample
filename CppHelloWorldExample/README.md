# C++ Hello World Example

hello.cpp
```
#include <iostream>
 
int main()
{
  std::cout << "Hello World!" << std::endl;
  return 0;
}
```


compile by gcc
```
gcc hello.cpp -lstdc++ -o hello.exe
```

alternatively, compile by g++
```
g++ hello.cpp -o hello.exe
```

execute
```
./hello.exe
```

```
Hello World!
```