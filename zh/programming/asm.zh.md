{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM 文件格式 - 汇编语言源代码文件格式",
  "description":"了解 ASM 文件格式和可以创建和打开 ASM 文件的 API。",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## 什么是一 .asm 文件？ ##

ASM 文件是用称为汇编语言的低级编程语言编写的程序。它主要用于编写与硬件相关的代码，例如编程微控制器。程序是使用简单的汇编语言语法编写的，其中包括用于执行不同操作的运算符和操作数。 ASM 文件在文本编辑器中编写和编辑，并使用 HLA、MASM、FASM、NASM 或 GAS 等汇编程序执行。

## ASM 文件格式

ASM 文件由汇编程序执行以生成**目标代码**的一系列操作组成。生成的目标代码是将助记符和寻址模式的组合翻译成它们的数字等价物。

### ASM 文件格式示例

以下是 x86 架构的 **Hello World** 应用程序示例。
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

## 参考 ＃＃

* [汇编语言 - 维基百科](https://en.wikipedia.org/wiki/Assembly_language)
* [汇编语言 - 基本语法](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

