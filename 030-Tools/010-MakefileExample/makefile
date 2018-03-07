build: main.o print_hello.o
	g++ -o main.exe main.o print_hello.o
	rm main.o print_hello.o
	
main.o: main.cpp print_hello.h
	g++ -c main.cpp
	
print_hello.o: print_hello.cpp print_hello.h
	g++ -c print_hello.cpp
