{
  "date": "2021-06-29",
  "keywords": [
    "com file",
    "what is a com file",
    "file",
    "com example",
    "com file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about COM file format and APIs that can create and open COM files.",
  "title": "COM - DOS Command File Format",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-com"
    }
  },
  "lastmod": "2021-06-29"
}

## What is a COM file?
The COM files are simply used for executing a set of commands or instructions. A COM file consists of an executable program which is capable of being run from Windows or MS-DOS. Likewise an EXE file, the COM file is also saved in binary format but it is different than EXE file because it has no header or metadata and also it has the maximum size of 64KB approximately. When the COM file runs first time on a 32-bit system, it prompts to install the NT Virtual DOS Machine (NTVDM) component. The COM file can be run on the 64-bit version of Microsoft Windows with a virtual machine that supports the MS-DOS environment.

## COM file format
The COM file format is a binary executable format used in Microsoft Windows or MS-DOS. Its structure consists of just a set of instructions; it has no header and contains no standard metadata. It stores all of its data and code in one segment only and its binary has maximum 64KB in size. This file format doesn't relocate itself when try to re-run. So the operating system loads it at a pre-set address. Moreover, it is possible to make a COM file to execute under both operating systems in the form of a **fat binary**. There is not any actual compatibility at the instruction level. The instructions at the entry point are selected to be equal in functionality but different in both operating systems, and make program running, jump to the section of the operating system in use. It is basically two different programs with the same procedure in a single file, preceded by code selecting the one to use.
### COM file example
When executing a COM file, the instructions are read from the first byte and are followed consecutively until the last instructions are found. Here is an ASM code example:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## References 

* [COM file - by Wikipewdia](https://en.wikipedia.org/wiki/COM_file)
