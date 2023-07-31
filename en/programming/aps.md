{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "APS - Visual C++ Resource File",
  "description":"Learn about APS file format with APS example and APIs that can create and open APS files.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-22"
}

## What is an APS file format?
An APS File is created by Visual C++, a software development application by Microsoft. It saves the binary representation of a resource incorporated with the project and it allows the application to load resources more rapidly. You can easily find these files with .aps file extension. In fact, the resource editors do not directly read the resource.h files that's why the resource compiler compiles them into .aps files that are consumed by the resource editors.

## APS file format
The APS file format is just a compile step and only stores symbolic data. The non-symbolic information such as commenting is discarded during the compile process. For example, when you Save, the resource editor overwrites the resource script file and the resource.h file. Any changes to the resources themselves remain incorporated in the resource script file, but comments will always be lost once the resource script file is overwritten.


## References

 * [Resource Files (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 
