{
  "date": "2023-06-08",
  "keywords": [
    "hpp file",
    "what is a hpp file",
    "what does hpp file contain",
    "hpp file example",
    "what is the format of hpp file",
    "file",
    "hpp file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "HPP File Format - C++ Header File",
  "description": "Learn about HPP format and APIs that can create and open HPP files.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
    }
  },
  "lastmod": "2023-06-08"
}

## What is a HPP file?

The ".hpp" file format is commonly used for header files in C++ programming language. Header files typically contain declarations and definitions of functions, classes, variables and constants that are used by other source code files in C++ project.

The purpose of using header files is to provide a way to share common code across multiple source code files without duplicating code itself. When C++ source file needs to access declarations or definitions from header file, it includes the header file using preprocessor directive `#include`.

The ".hpp" file extension is often used to indicate that a file is a C++ header file. It is not a requirement to use this specific extension for header files, and you may also come across header files with ".h" or other extensions. The choice of extension is largely a matter of convention and personal preference.

When a C++ source file includes header file using `#include`, the compiler effectively combines content of header file with source file before compiling it as a unit. This allows the source file to access declarations and definitions in header file, providing the necessary information for compiler to perform type checking and code generation.

## What does HPP file contain?

Here are some common contents you may find in ".hpp" file:

- **Function declarations:** Header files often include function declarations without their actual implementations. These declarations provide information about function's name, return type and parameters, allowing other source code files to use function without needing to know implementation details.
- **Class declarations:** Header files can contain class declarations, including class name, member variables, member functions and access specifiers. By including class declaration in header file, other source code files can create objects of that class and access its members.
- **Constant declarations:** Header files can define constants, such as global variables or enum values that are meant to be shared across multiple source code files. These constants can be accessed by including header file in other source files, allowing them to use the defined constants.
- **Type definitions:** Header files may contain type definitions using "typedef" keyword or type aliases using "using" keyword. These definitions create new names for existing types, making code more readable and maintainable.
- **Inline function definitions:** In some cases, header files may contain inline function definitions. Inline functions are small functions that are expanded at call site rather than being called as separate function. Including inline function definition in header file allows compiler to replace function call with function body directly, potentially improving performance.

## HPP File Example

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## What is the format of HPP file?

HPP is a plain text file but follows the general rules and syntax of C++ programming language. Here is a breakdown of general format and structure of ".hpp" file:

- **Header guards:** Typically, a ".hpp" file begins with header guards to prevent multiple inclusions of same file. This is achieved using preprocessor directives like `#ifndef`, `#define` and `#endif`. The header guard ensures that contents of file are included only once during the compilation process.
- **Include statements:** After header guards, you can include other necessary header files using `#include` directive. These may include standard library headers or other custom headers required by your code.
- **Declarations and Definitions:** The primary content of ".hpp" file is the declarations and, in some cases, definitions of classes, functions, constants, type aliases and other elements. For example, you may declare classes using `class` keyword, functions using their return type, name, and parameter list, and constants using `const` keyword followed by their type and name.
- **Inline Function Definitions:** In certain cases, you may include inline function definitions directly in ".hpp" file. Inline functions are usually defined inside class body, meaning the function definition is included alongside its declaration. This can be done by prefixing function definition with `inline` keyword.
- **Namespace Declarations:** If you're using namespaces in your code, you can declare them within ".hpp" file. This is done using `namespace` keyword followed by namespace name and enclosing the relevant code within namespace block.

## References
* [Header files (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
