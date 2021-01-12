{
  "date" : "2020-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "C",
  "description":"Learn about C file format and APIs that can create and open C files.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-01-10"
}

## What is a C file?

A file with .c extension is a source code file for writing software applications in C programming language. C files include all the implementation of application's functionality in the form of source code. The declaration of the source code is written in the header files that are saved with [.h](/programming/h/) extension. C++ is the modern form of C language and is used to develop most of the software nowadays. C files can be opened with applications such as Notepad++, [Eclipse IDE](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-cc-developers), [Microsoft Visual Studio](https://fileinfo.com/software/microsoft/visual_studio), and [Borland C++ Builder](https://www.embarcadero.com/products/cbuilder).

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

### C Source Code Example

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
* [Introduction to C++ - W3 Schools](https://www.w3schools.in/cplusplus-tutorial/intro/)
