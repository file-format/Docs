{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM-filformat - Assembly Language Kildekode-filformat",
  "description":"Lær om ASM-filformat og API'er, der kan oprette og åbne ASM-filer.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Hvad er en ASM fil? ##

En ASM-fil er et program skrevet i lavniveauprogrammeringssproget kendt som assemblersprog. Det bruges primært til at skrive hardwarerelateret kode, såsom til programmering af mikrocontrollere. Programmet er skrevet ved hjælp af simpel assemblersprogsyntaks, der inkluderer operatører og operander til at udføre forskellige operationer. ASM-filer skrives og redigeres i teksteditorer og udføres ved hjælp af et assembler-program såsom HLA, MASM, FASM, NASM eller GAS.

## ASM filformat

ASM-filer består af en sekvens af operationer, der udføres af en assembler for at generere **objektkode**. Den resulterende objektkode er en oversættelse af kombinationer af mnemonics og adresseringstilstande til deres numeriske ækvivalenter.

### Eksempel på ASM-filformat

Følgende er et eksempel på **Hello World**-applikationen til en x86-arkitektur.
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

* [Assembly Language - af Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


