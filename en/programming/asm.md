{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ASM File Format - Assembly Language Source Code File Format",
  "description":"Learn about ASM file format and APIs that can create and open ASM files.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-04-03"
}

## What is an ASM file? ##

An ASM file is a program written in the low level programming language known as assembly language. It is primarily used for writing hardware related code such as for programming micro-controllers. Program is written using simple assembly language syntax that includes operators and operands to carry out different operations. ASM files are written and edited in text editors and are executed using an assembler program such as HLA, MASM, FASM, NASM, or GAS.

## ASM File Format

ASM files consist of a sequence of operations that are executed by an assembler to generate **object code**. The resultant object code is a translation of combinations of mnemonics and addressing modes into their numerical equivalents.

### ASM File Format Example

Following is an example of **Hello World** application for an x86 architecture.
```
global  go
extern  _ExitProcess@4
extern  _GetStdHandle@4
extern  _WriteConsoleA@20

section .data
msg:    db      'Hello, World', 10
handle: db      0
written:
db      0

section .text
go:
; handle = GetStdHandle(-11)
push    dword -11
call    _GetStdHandle@4
mov     [handle], eax

; WriteConsole(handle, &msg[0], 13, &written, 0)
push    dword 0
push    written
push    dword 13
push    msg
push    dword [handle]
call    _WriteConsoleA@20

; ExitProcess(0)
push    dword 0
call    _ExitProcess@4
```

## Reference ##

* [Assembly Language - by Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)
