
1. autoscan
2. mv configure.scan configure.in
3. aclocal
4. autoconf
5. create Makefile.am
6. automake --add-missing
7. ./configure
8. make
9. make install



configure.in
```
AC_INIT(hello.c)

AM_INIT_AUTOMAKE(hello, 1.0)

dnl Checks for programs.

AC_PROG_CC

dnl Checks for libraries.

dnl Checks for header files.

dnl Checks for typedefs, structures, and compiler ch aracteristics.

dnl Checks for library functions.

AC_OUTPUT(Makefile)

```



Makefile.am
```
AUTOMAKE_OPTIONS= foreign

bin_PROGRAMS= hello

hello_SOURCES= hello.c
```
