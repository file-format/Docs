{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ASM - Formát souboru zdrojového kódu jazyka assembler",
  "description":"Další informace o formátu souborů ASM a rozhraních API, která mohou vytvářet a otevírat soubory ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Co je soubor ASM? ##

Soubor ASM je program napsaný v nízkoúrovňovém programovacím jazyce známém jako jazyk symbolických instrukcí. Primárně se používá pro psaní kódu souvisejícího s hardwarem, například pro programování mikrokontrolérů. Program je napsán pomocí jednoduché syntaxe assembleru, který obsahuje operátory a operandy pro provádění různých operací. Soubory ASM se zapisují a upravují v textových editorech a spouštějí se pomocí programu assembler, jako je HLA, MASM, FASM, NASM nebo GAS.

## Formát souboru ASM

Soubory ASM se skládají ze sekvence operací, které jsou prováděny assemblerem za účelem generování **objektového kódu**. Výsledný objektový kód je překladem kombinací mnemotechnických pomůcek a režimů adresování do jejich číselných ekvivalentů.

### Příklad formátu souboru ASM

Následuje příklad aplikace **Hello World** pro architekturu x86.
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

## reference ##

* [Assembly Language – podle Wikipedie](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language – základní syntaxe](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

