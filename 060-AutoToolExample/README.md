
1. autoscan
2. mv configure.scan configure.in
3. update configure.in
4. aclocal
5. autoconf
6. create Makefile.am
7. automake --add-missing --foreign 
8. ./configure
9. make
10. make install


configure.in
```
#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_INIT(lib/libsrc.c)
AM_INIT_AUTOMAKE(hello, 1.0)

# Checks for programs.
AC_PROG_CC
AC_PROG_RANLIB

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_OUTPUT(Makefile src/Makefile lib/Makefile)
```

Makefile.am
```
SUBDIRS = lib src
```

src/Makefile.am
```
bin_PROGRAMS = main
main_SOURCES = main.c
LDADD = -L../lib
INCLUDES = -I$(top_builddir)/lib
```

lib/Makefile.am
```
noinst_LIBRARIES = libexample.a
libexample_a_SOURCES = libsrc.c
```

main.c
```
#include <stdio.h>
#include "libsrc.h"

int main(){
	printf("Hello World!");
	return 0;
}
```

libsrc.h
```
char * greeting();
```

libsrc.c
```
char * greeting(){
	return "Hello World";
}
```