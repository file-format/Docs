{
  "date": "2020-01-10",
  "keywords": [
    "c",
    ".c",
    "what is a c file",
    "how to open c file",
    "extension",
    "file",
    "c file",
    "c file format",
    "c file extension"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "C - C Language Programming File",
  "description": "Learn about C file format and APIs that can create and open C files.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c"
    }
  },
  "lastmod": "2020-01-10"
}

## What is a C file?

A file saved with c file extension is a source code file written in C programming language. The **C file** include all the implementation of application's functionality in the form of source code. The declaration of the source code is written in the header files that are saved with [.h](/programming/h/) extension. C++ is the modern form of C language and is used to develop most of the software nowadays. 

## Brief History

C language came into being as a result of creating different utilities for UNIX operating system. Denis Ritchie, the man behind the creation of this programming language, the work originally started in 1960s and early 1970s.

## C File Format

C files are written in plain text file format following the programming language syntax. A typical C file will have:

 * import statement at the top of the file to import any header Files
 * one or more methods to implement desired functionality

### Headers Import

The header files, with .h extension, contain necessary include statements for including other functionality files in the project. In addition, these contain the declarations of methods defined in the implementation file. Header files are included using the include statement as shown below.

```
#include <filename.h>
```

### Source Code Implementation

The actual implementation of the functional requirements are coded as methods in the C file. Each method in a C file has a return type, method name and may have some input parameters. If the return type is not void, the method may be returning some value.

### C Code Example
Here is a c example program:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **References** ##

* [Class Implementation - By Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)
