{
  "date": "2019-10-11",
  "keywords": [
    "c++",
    "file",
    "extension",
    "file format",
    "C++",
    "Programming Language"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "CPP - C++ Source Code File",
  "description": "Learn about CPP file format and APIs that can create and open CPP files.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cpp"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a C++ file?

Files with CPP file extension are source code files for applications written in C++ programming language. A single C++ project may contain more than one CPP files as application source code. Such a project consists of different file types, of which the CPP files are known as implementation files as they contain all the definitions of the methods declared in the header (.h) file. The C++ project as a whole results in an executable application when compiled as a whole.

## CPP File Structure

A CPP file structure is simple as compared to the header files. The main purpose of such an implementation file is to split the interface from the implementation. This results in declarations of all the member functions in a header file and their details inside the CPP file. A CPP implementation file can be used as a simple file for writing an application or as a class implementation.

### Independent Implementation

A CPP file when used as an independent application can contain all the implementations inside it without the requirement of methods declaration in header file. Such an implementation consists of all methods defined in the implementation file where the entry of the application is governed by a main method that takes optional user input as arguments. It can also include any libraries from the C++ Standard Library to be used by any declared methods in the file.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Class Implementation

In Object Oriented Programming (OOP), a CPP file is used as a class definition. In such case, all the class data members and member functions are declared inside the header file. Each header file can in turn have reference to standar library methods as well. The class definition CPP file refers to the header file in an include statement at the start of the file. Mostly, software developers include comments at the start of such a class implementation file that provide information about the actual contents of the file, author's details and the implementation date. In such cases, the header implementation files must have the same names. An example of such a header and implementation file is as follow.

### Header File

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP Implementation File

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## References

* [Class Implementation - By Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)
