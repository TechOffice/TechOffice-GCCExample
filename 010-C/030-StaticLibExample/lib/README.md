
## Prepare Static Library

```
cd lib
```

```
gcc -c lib/hello.c lib/world.c
```


```
ar rcs libmylib.a hello.o world.o
```

## Compile Source Code

```
cd ..
```

```
gcc helloworld.c -LLib -lmylib -ILib
``

