{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MAN - Unix Manual",
  "description":"Learn about FODT file format and APIs that can create and open MAN files.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
    }
  },
  "lastmod" : "2021-07-25"
}

## What is a MAN file?

A file with .man extension (stands for man page) is a Unix programming user's manual in software documentation. It is used by the `Man` utility, included in Unix, that is used to view the documentation. The software documentation contains information in sections and pages that can be retrieved using the Man utility from command terminal by issuing commands. Being available in the computer as soft copy of documentation, it doesn't require any printed copy or internet connection to access it.

## Unix Manual Man File Format - More Information

Man pages are stored in plain text format and can be created and opened in any text editor for viewing or editing. In UNIX, information from the Man pages is retrieved by issuing commands from terminal that includes reference to section and page numbers from the manual.

### Sections and Pages

Unix man is the system's manual where each page argument to the command refers to the name of a program, utility or function. the command, if provided with section information, will search for the page in that specific section. However, the default behaviour is to search for the page in all sections and display the first page irrespective of if it exists in multiple sections.

### Section Numbers

Following is the information about the section numbers of the manual followed by the types of pages they contain.

|Section Number|Type of pages|
---|---|
|1|Executable programs or shell commands|
|2|System calls (functions provided by the kernel)|
|3|Library calls (functions within program libraries)|
|4|Special files (usually found in /dev)|
|5|File formats and conventions, e.g. /etc/passwd|
|6|Games|
|7|Miscellaneous (including macro packages and conventions), e.g. man(7), groff(7)|
|8|System administration commands (usually only for root)|
|9|Kernel routines [Non standard]|

## References

* [OpenDocument Technical Specifications - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux manual page](https://man7.org/linux/man-pages/man1/man.1.html)
