{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM-bestandsindeling - assembleertaal broncodebestandsindeling",
  "description":"Meer informatie over ASM-bestandsindeling en API's die ASM-bestanden kunnen maken en openen.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Wat is een ASM-bestand? ##

Een ASM-bestand is een programma dat is geschreven in de programmeertaal op laag niveau die bekend staat als assembleertaal. Het wordt voornamelijk gebruikt voor het schrijven van hardwaregerelateerde code, zoals voor het programmeren van microcontrollers. Het programma is geschreven met behulp van een eenvoudige syntaxis in assembler die operators en operanden bevat om verschillende bewerkingen uit te voeren. ASM-bestanden worden geschreven en bewerkt in teksteditors en worden uitgevoerd met behulp van een assembler-programma zoals HLA, MASM, FASM, NASM of GAS.

## ASM-bestandsindeling

ASM-bestanden bestaan uit een reeks bewerkingen die door een assembler worden uitgevoerd om **objectcode** te genereren. De resulterende objectcode is een vertaling van combinaties van geheugensteuntjes en adresseringsmodi in hun numerieke equivalenten.

### Voorbeeld van ASM-bestandsindeling

Hieronder volgt een voorbeeld van een **Hello World**-toepassing voor een x86-architectuur.
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

## Referentie ##

* [Assembly Language - door Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

