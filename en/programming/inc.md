{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "INC File Extension - What is an INC file?",
  "description":"Learn about INC Include file format and APIs that can create and open INC files.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-07-14"
}

## What is an INC file?

An INC file is an include file that is used by software program's source code to reference headers information. It is similar to the [.h file format](/programming/h/) and contains declarations, functions, headers, or macros that can be reused by source code files such as C++. INC files are used by a variety of programming languages like C, [C++](/programming/cpp/), Pascal, [PHP](/programming/php/), and [Java](/programming/java/). Text editors such as Microsoft Notepad, Notepad++, and TextEdit can be used to open INC files.

## INC File Format - More Information

An INC file is saved as plain text file with all the declarations included as per the declaration syntax. One INC file can reference other INC files as well. Once created, the INC file becomes part of the project and can be referenced from source files such as C++. It can be referenced by multiple source files to avoid any duplication.

## INC File Contents

INC files can include the following information.

**`Variables`** - In case of Object Oriented Programming (OOP), a class header file contains definitions of all class level variables that are accessible across the implementation source code files

**`Methods Declaration`** - All the methods declarations are included in the .h header files to be accessible across multiple implementation files.

**`Non-Inline Function Definitions`** - Header files can also contain definitions of a non-inline methods.

## Disadvantage of using INC file in PHP

PHP are server side scripts that run on server and return the results to the calling webpages. If a PHP file is referencing an INC file and the server is not configured to parse .inc files (which is very common), a user can view the php source code in the .inc file by visiting the URL directory. So, one must be careful while using INC files as include files in PHP.

## References

* [Using INC in PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)
