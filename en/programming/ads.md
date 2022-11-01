
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ADS File - Ada Specification File Format",
  "description":"Learn about what is ADS file format with example and APIs that can create and open ADS files.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-10-30"
}

## What is an ADS file?

An ADS file is a specification file for an Ada programming project. It is similar to a class for Java, or the header and implementation pair in case of C++. The public and private specifications of the Ada package are stored in the .ads file. The, .adb file, in contrast contains the implementation, or Ada bodies. Like [C++](/programming/cpp/), Ada offers separation between specifications and implementations independent of OOP.

ADS files can be opened in any text editor such as Microsoft Notepad, Notepad++, and Atom.

## ADS File Format

ADS files are in simple plain text file format and can be opened/edited with any text editor. Ada packages can be organized into hierarchies. A child unit can be declared in the following way:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## References

 * [Ada Packages](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)
