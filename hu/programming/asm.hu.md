{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM fájlformátum – Assembly Language Forráskód fájlformátum",
  "description":"További információ az ASM fájlformátumról és az API-król, amelyek ASM fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Mi az ASM fájl? ##

Az ASM-fájl egy alacsony szintű programozási nyelven, úgynevezett assembly nyelven írt program. Elsősorban hardverhez kapcsolódó kódok írására használják, például mikrovezérlők programozására. A program egyszerű assembly nyelvi szintaxissal készült, amely operátorokat és operandusokat tartalmaz a különböző műveletek végrehajtásához. Az ASM-fájlokat szövegszerkesztőkkel írják és szerkesztik, és olyan assembler programokkal hajtják végre, mint a HLA, MASM, FASM, NASM vagy GAS.

## ASM fájlformátum

Az ASM fájlok műveletek sorozatából állnak, amelyeket egy assembler hajt végre az **objektumkód** létrehozásához. Az eredményül kapott objektumkód a mnemonikák és a címzési módok kombinációinak numerikus megfelelőire való fordítása.

### ASM fájlformátum példa

Az alábbiakban egy példa látható a **Hello World** alkalmazásra x86 architektúrához.
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

## Hivatkozási szám

* [Assembly Language – Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

