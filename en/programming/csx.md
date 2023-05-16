{
  "date": "2023-05-15",
  "keywords": [
    "csx file",
    "what is a csx file",
    "what does csx file contain",
    "what is the format of csx file",
    "file",
    "csx file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CSX File Format - Visual C# Script",
  "description": "Learn about CSX format and APIs that can create and open CSX files.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
    }
  },
  "lastmod": "2023-05-15"
}

## What is a CSX file?

Visual C# Script (also known as CSX) is a file format used by Roslyn scripting engine in Microsoft's .NET ecosystem. CSX files contain C# code that can be executed directly without the need for separate compilation step.

CSX format is specific to Microsoft ecosystem and not a widely used file format in general programming. CSX files are often used in scenarios where quick prototyping or scripting functionality is required. They allow you to write C# code and execute it in more lightweight manner compared to creating a full-fledged compiled application.

To execute CSX files, you can use tools like .NET Interactive Notebooks, which provide an interactive environment for running C# code. Visual Studio Code with the C# extension and .NET Core SDK can also be used to work with CSX files.

## What does CSX file contain?

A CSX (C# Script) file contains C# code that can be executed directly. It can include any valid C# code such as variable declarations, functions, classes and other programming constructs.

Here is an example of what CSX file might contain:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
    }
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX files can also include import statements, external library references and other C# language features to support the code's functionality. The code is interpreted and executed on-the-fly without need for compilation making it suitable for scripting and quick prototyping tasks.

## What is the format of CSX file?

The CSX (C# Script) format follows simple text-based format. It typically has file extension .csx to differentiate it from regular C# source code files (.cs).

CSX files can be edited using any text editor or integrated development environment (IDE) that supports C# syntax highlighting. Once CSX file is ready, it can be executed using tools like .NET Interactive Notebooks, the .NET Core command-line interface (CLI), or an IDE with C# scripting support.

## References
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)
