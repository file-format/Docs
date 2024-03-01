{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDE File -  What is an MDE file and how to open it?",
  "description":"Learn about MDE file format and APIs that can create and open MDE files.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

## What is an MDE file?

An .MDE file is a compiled version of an Access database (.mdb or .accdb). When you compile an Access database into an .MDE file, it is no longer editable using the standard Access design tools. The primary purpose of creating an .MDE file is to distribute a database application without exposing the original source code.

## MDE File Format

An MDE file is created by compiling the VBA code, forms, reports and other objects. This results in creation of MDE binary file format. The resulting .MDE file can be distributed to users who can run the application but cannot modify the design or view the original code. MDE file is actually the compiled version of a [.MDA file](/database/mda/). Distributing .MDE files can help protect intellectual property by preventing users from accessing or modifying the source code. It can also enhance performance as the code is compiled and optimized.

## References

* [Access Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
