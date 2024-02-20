{
  "date": "2021-07-25",
  "keywords": [
    "man",
    "file",
    "extension",
    "type",
    "format",
    "Unix Manual"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix Manual",
  "description": "Learn about FODT file format and APIs that can create and open MAN files.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-man"
    }
  },
  "lastmod": "2021-07-25"
}

## What is a MAN file?

A file with .man extension  stands for man page which is a Unix programming user's manual in software documentation form. It is used by the `Man` utility, included in Unix, that is used to view the documentation. The software documentation contains information in sections and pages that can be retrieved using the Man utility from command terminal by issuing commands. Being available in the computer as soft copy of documentation, it doesn't require any printed copy or internet connection to access it.

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

## Example - How to Read MAN Pages?

Here is an example how to retrieve informatino about MkDir command using the Man command.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## References

* [OpenDocument Technical Specifications - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux manual page](https://man7.org/linux/man-pages/man1/man.1.html)
