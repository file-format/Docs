{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "M - Matlab Source Code File",
  "description":"Learn about Matlab .m Source Code file and APIs that can create and open MF files.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}

# M - Matlab Source Code Files

## What is an  M (Matlab) file?

A file with .m extension is a source code file used by Matlab, a programming and numeric computation platform used for analysis, algorithms development, and simulation modelling. Like other programming file formats, an M file contains source code that executes Matlab commands to plot graphs, run simulations, and other mathematical operations. A single Matlab simulation can span over multiple such .m files that can classify the application in scripts, classes, functions, or declarations. Matlab M files can be opened with any text editor.

## Matlab M File Format - More Information

Matlab .m files are text files that contain programming code in Matlab programming language. These can be opened and edited in any text editor, and saved back to be executed in Matlab software. Matlab itself contains a Live Editor that is used for creating scripts that is a combination of code, output, and formatted text.

### Matlab Function Files

Like other programming languages, you can create a .m file that only contains the definition of a function which performs a specific task only. Such files are also saved with .m extension and implements the functionality related to that function only.

### .M File Example

The following is a Matlab function file example that calculates the time taken for an object dropped from height h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

To call this function from Matlab editor or from another .m file, the following code can be used.
```C++
TimeToGround(100)
```

## References

 * [Matlab - Supported File Formats](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Using Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C Implementation File

## What is an M (Objective-C) file?

An M file is also referred to as implementation file that contains source code of a class written in Objective-C language, a programming language used to write software applications for OS X and iOS. Objective-C is the main programming language that is used by Apple's main APIs, Cocoa and Cocoa Touch, for these platforms. A single software application developed in this language may contain multiple .m files, containing the implementation of the program classes. These can be opened using Apple XCode, jEdit, and other common text editors.

## Objective-C M File Format - More Information

The M files are written in plain text format using the programming syntax of Objective-C. Every method of a class must be defined with all its necessary code in these implementation files. These implementation M files can import one or more .h header files as per requirements. The import statement tells the compiler where to find the header file that belongs to this implementation file. The import statement is written as follow.

```C++
#import "network.h"
```

Each M file implementation then starts with the `@implementation` directive, followed the by the implementation class file name. This is then followed by all the methods implementation that are declared in the header file.

### M File Format Example

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## References
 * [About Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)
