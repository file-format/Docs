{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM-Dateiformat - Assemblersprachen-Quellcode-Dateiformat",
  "description":"Erfahren Sie mehr über das ASM-Dateiformat und APIs, die ASM-Dateien erstellen und öffnen können.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
"Bezeichner": "Programmierung-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Was ist eine ASM-Datei? ##

Eine ASM-Datei ist ein Programm, das in einer einfachen Programmiersprache geschrieben ist, die als Assemblersprache bekannt ist. Es wird hauptsächlich zum Schreiben von hardwarebezogenem Code verwendet, z. B. zum Programmieren von Mikrocontrollern. Das Programm ist unter Verwendung einer einfachen Assemblersprachen-Syntax geschrieben, die Operatoren und Operanden enthält, um verschiedene Operationen auszuführen. ASM-Dateien werden in Texteditoren geschrieben und bearbeitet und mit einem Assembler-Programm wie HLA, MASM, FASM, NASM oder GAS ausgeführt.

## ASM-Dateiformat

ASM-Dateien bestehen aus einer Folge von Operationen, die von einem Assembler ausgeführt werden, um **Objektcode** zu generieren. Der resultierende Objektcode ist eine Übersetzung von Kombinationen von Mnemonik- und Adressierungsmodi in ihre numerischen Äquivalente.

### Beispiel für ein ASM-Dateiformat

Im Folgenden sehen Sie ein Beispiel für eine **Hello World**-Anwendung für eine x86-Architektur.
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

## Bezug ##

* [Assembly Language - von Wikipedia] (https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly-Sprache – grundlegende Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

