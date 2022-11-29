{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM-filformat - Assembly Language Source Code File Format",
  "description":"Läs mer om ASM-filformat och API:er som kan skapa och öppna ASM-filer.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Vad är ASM fil? ##

En ASM-fil är ett program skrivet i det lågnivåprogrammeringsspråk som kallas assemblerspråk. Den används främst för att skriva hårdvarurelaterade kod som för programmering av mikrokontroller. Programmet är skrivet med en enkel syntax för assemblerspråk som inkluderar operatorer och operander för att utföra olika operationer. ASM-filer skrivs och redigeras i textredigerare och körs med hjälp av ett assemblerprogram som HLA, MASM, FASM, NASM eller GAS.

## ASM filformat

ASM-filer består av en sekvens av operationer som exekveras av en assembler för att generera **objektkod**. Den resulterande objektkoden är en översättning av kombinationer av mnemonics och adresseringslägen till deras numeriska motsvarigheter.

### Exempel på ASM-filformat

Följande är ett exempel på **Hello World**-applikation för en x86-arkitektur.
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

## Referens ##

* [Assembly Language - av Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

