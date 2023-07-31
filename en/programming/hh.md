{
  "date" : "2019-10-11",
  "keywords" : [ "h", ".hh","what is a .hh file","how to open .hh file", "extension", "file", ".hh file",".hh file format",  ".hh file extension",".HH File Example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HH - C++ Header File Format",
  "description":"Learn about HH file format and APIs that can create and open HH file.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-06-20"
}

## What is an HH file?

A file with .hh extension is a C++ header file that includes the declaration of variables, constants, and functions. These declarations are used by the corresponding C++ implementation files, usually saved as [.cpp](/programming/cpp/) files that contain the actual implementation of user logic. The .hh header files are referenced in the implementation CPP files using the `#include` directive. You can add as many as possible header files to your C++ project to include project level declarations.

## .HH File Format

A .hh file is a plain text file that is created keeping in view the header file definition rules. Most common information declared in a .hh file include the following.

**`Variables`** - In case of Object Oriented Programming (OOP), a class header file contains definitions of all class level variables that are accessible across the implementation source code files
**`Methods Declaration`** - All the methods declarations are included in the .h header files to be accessible across multiple implementation files.
**`Non-Inline Function Definitions`** - Header files can also contain definitions of a non-inline methods.
**`Message Maps`** - A header file can also contain message maps in case of an MFC source code implementation. In such case, the message maps are linked to the functionality implementation which is linked to UI elements such as button, checkbox, radio buttons, etc.

## Difference Between .H and .HH Files

Apparently, there is no such difference between the .h and .hh header files other than the recommended way of using these for respective languages i.e. [C](/programming/c/) or C++. Naming your header files according to these languages help you distinguish between these in a large project that can be a mix of C and C++ implementations.

In addition, if the headers are separated by extension, your editor can apply the appropriate formatting automatically for respectively.

Overall, the differentiation of these two file formats will not do any harm, but will be advantageous, and is encouraged to follow for C and C++ distinction.

### Header Guards

Header files can raise to complex errors where multiple declarations are included in the same file as a result of adding other header files. This duplicate definitions raise compiler errors. This problematic situation can be avoided via a mechanism called header guard that are conditional compilation directives as shown below.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
With this header, the preprocessor checks whether the `ANY_UNIQUE_NAME_HERE_HPP` has already been defined. If the header is repeatedly included into the same file, the contents of the header will be ignored.

## References

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Difference between .h and .hh file formats](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)
