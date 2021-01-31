{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CS - CSharp Code File",
  "description":"Learn about CS file format and APIs that can create and open CS files.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a CS file?

Files with .CS extension are source code files for C# programming language. Introduced by Microsoft for use with the .NET Framework, the file format provides the low-level programming language for writing code that is compiled to generate the final output file in the form of EXE or a DLL. These can be created and compiled with Microsoft Visual Studio. Microsoft Visual Studio Express can also be used to create and update such files which is a free IDE. CS files are used for application development that can range from simple desktop applications to more complex programs. A simple Visual Studio project [solution](/programming/sln/) created with C# language can comprise of one or more such files. Files marked for inclusion in compilation are listed in the [CSPROJ](/programming/csproj/) file which is part of the project and tells compiler to use the marked files.

## CS File Format ##

CS files are text based file formats that can be opened in any text editor for editing. However, when opened in a supported IDE with proper syntax highlighting, the code is easy to read and arrange. A simple CS file contains:

* Namespaces declaration - For referring to a particular functionality defined by that specific namespace
* Variables declaration - To declare class level variables for the particular implementation
* Methods Declaration - To declare methods declaration for the particular functionality

### Syntax ###

* Semicolons are used to denote the end of a statement.
* Curly brackets are used to group statements. Statements are commonly grouped into methods (functions), methods into classes, and classes into namespaces.
* Variables are assigned using an equals sign, but compared using two consecutive equals signs.
* Square brackets are used with arrays, both to declare them and to get a value at a given index in one of them.

### Example ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
    }
}
```

## How to open CS files? ##

Following applications can be used to open .CS files.

* Microsoft Visual Studio
* Microsoft Notepad
* Notepad++
* MonoDevelop
