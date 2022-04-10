{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Make File - Xcode Makefile Script File",
  "description":"Learn about XCode MakeFile Format and APIs that can create and open MakeFile files.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2020-09-10"
}


## What is a MAKE file?

A MAKE file is an XCode script file that organize compilation of code. It is used to compile and link programs from multiple source code files. This help decide which parts of a large application are required to be recompiled when the application needs to be updated. Make files use a series of instructions to run depending on what files have changed.

## MAKE File Format Example

The following contents is executed using the Make utility and outputs is as followed.

```
hello:
	echo "hello world"
```
**Make Output**

```
$ make
echo "hello world"
hello world
```

## References
 * [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
 * [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)
