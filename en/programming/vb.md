{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VB - Visual Basic Code File",
  "description":"Learn about VB file format and APIs that can create and open VB files.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2019-09-10"
}

A VB file is a source code file created in Visual Basic language that was created by Microsoft for development of .NET applications. Another similar language with different syntax is C# whose files are saved with [.CS](/programming/cs/) file extension. The file format provides the low-level programming language for writing code that is compiled to generate the final output file in the form of EXE or a DLL. These can be created and compiled with Microsoft Visual Studio. Microsoft Visual Studio Express can also be used to create and update such files which is a free IDE. A simple Visual Studio project [solution](https://wiki.fileformat.com/programming/sln/) created with VB language can comprise of one or more such files. Files marked for inclusion in compilation are listed in the [CSPROJ](https://wiki.fileformat.com/programming/csproj/) file which is part of the project and tells compiler to use the marked files.

## VB File Format ##

VB files are text based file formats that can be opened in any text editor for editing. However, when opened in a supported IDE with proper syntax highlighting, the code is easy to read and arrange. A simple VB file contains:

* Namespaces declaration - For referring to a particular functionality defined by that specific namespace
* Variables declaration - To declare class level variables for the particular implementation
* Methods Declaration - To declare methods declaration for the particular functionality

## Example ##

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```

## How to open VB files? ##

Following applications can be used to open .VB files.

* Microsoft Visual Studio
* Microsoft Notepad
* Notepad++
* MonoDevelop
