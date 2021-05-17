{
  "date" : "2019-10-11",
  "keywords" : [ "h", ".h","what is a h file","how to open h file", "extension", "file", "h file","h file format",  "h file extension","H File Example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "H - C/C++ Header File Format",
  "description":"Learn about H file format and APIs that can create and open H file.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-05-07"
}

## What is an H file?

A file saved with **h file extension** is a header file used in C/C++ files to include the declaration of variables, constants, and functions. These are referred by the [C++](/programming/cpp/) implementation files that contain the actual implementation of these functions. A .h header file can also include additional information such as Macro definitions. These header files are referenced in the C/C++ files using the `#include` directive. A new C++ project usually contains a special header file by the name stdafx.h file that is the starting point for all compilation chains and all the header files can be included in this single file. A .h file can be opened with any text editor, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ compiler and a lot other applications.

## .H File Format

A .h file is plain text file that has its own rules for defining the syntax. Header files can contain the following information.

**`Variables`** - In case of Object Oriented Programming (OOP), a class header file contains definitions of all class level variables that are accessible across the implementation source code files
**`Methods Declaration`** - All the methods declarations are included in the .h header files to be accessible across multiple implementation files.
**`Non-Inline Function Definitions`** - Header files can also contain definitions of a non-inline methods.
**`Message Maps`** - A header file can also contain message maps in case of an MFC source code implementation. In such case, the message maps are linked to the functionality implementation which is linked to UI elements such as button, checkbox, radio buttons, etc.


### Header Guards

Header files can raise to complex errors where multiple declarations are included in the same file as a result of adding other header files. This duplicate definitions raise compiler errors. This problematic situation can be avoided via a mechanism called header guard that are conditional compilation directives as shown below.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
With this header, the preprocessor checks whether the `ANY_UNIQUE_NAME_HERE` has already been defined. If the header is repeatedly included into the same file, the contents of the header will be ignored.

## H File Example

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
    }

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
    }
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
        }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## References

* [Header Filers - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
