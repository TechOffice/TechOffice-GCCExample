# GNU Make
GNU Make is a utiltiy that automates the building executable from source code. It uses a configuration file so-called makefile which contains rules on how to build the executable.

# Makefile

A makefile is a file describe how to compile and link a program

## Format
```
<target>: <dependencies>
	<System Command(s)>
```

e.g. makefile
```
build: main.o print_hello.o
	g++ -o main.exe main.o print_hello.o
	rm main.o print_hello.o
	
main.o: main.cpp print_hello.h
	g++ -c main.cpp
	
print_hello.o: print_hello.cpp print_hello.h
	g++ -c print_hello.cpp
```


**main.cpp**
```
#include "print_hello.h"

int main(){
	print_hello();
}
```

**print_hello.h**
```
void print_hello();
```

**print_hello.cpp**
```

#include <iostream>

using namespace std;

#include "print_hello.h"

void print_hello(){
	cout << "Hello World!";
}
```


Use Make to compile source code
```
make 
```
It would generate main.exe


**Execution**
```
main.exe
```


**Output**
```
Hello World!
```


