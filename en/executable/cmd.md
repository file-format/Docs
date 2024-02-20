{
  "date": "2021-07-12",
  "keywords": [
    "cmd file",
    "what is a cmd file",
    "file",
    "cmd example",
    "cmd file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about CMD file format and APIs that can create and open CMD files.",
  "title": "CMD - Windows Command File Format",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cmd"
    }
  },
  "lastmod": "2021-07-12"
}

## What is a CMD file?
A CMD file consists of a script containing one or multiple commands in the form of plain text that are run in order to execute various tasks. It is similar to a [BAT](/executable/bat/) file, which is also generally used to store a batch of executable commands. The CMD files are widely used in the Microsoft Windows operating system. These files were introduced in the almost in 90's but still used in the latest Windows operating system. These files are generally written to execute more than one command in a sequence.

## CMD file format
CMD is a file format used by CP/M-style executable programs. It is generally comparable with [COM](/executable/com/) in CP/M-80 and [EXE](/executable/exe/) in DOS. A CMD file contains  1 to 8 groups of code or data and a 128-byte header. Each group can be up to 1 mb in size. CMD files can also contain relocation information and Resident System Extensions (RSXs) in its later versions. The CMD is a newcomer as compared with [BAT](/executable/bat/) file; used for MS-DOS before the release of windows In MS-DOS. Although, you can still save files with .bat extension today, many people use the .cmd extension to save their executable scripts.

### CMD format Specification

The start of the header contains the list of the groups present in the file along with their types. Each type can be used one time at most. These types are:

- Code
- Data
- Extra
- Stack
- User 1
- User 2
- User 3
- User 4
- Shared Code 

Likewise Program Segment Prefix in DOS, the first 256 bytes of the data group are zero. They will be populated by CP/M-86 with the zero page. If there is no data group, then the first 256 bytes of the code group will be used instead.
## CMD file example
Following is an example of a CMD script to show systems information.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## References 

* [How to Write a CMD Script](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD file (CP/M) - by Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))
