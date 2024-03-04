{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM failo formatas – surinkimo kalbos šaltinio kodo failo formatas",
  "description":"Sužinokite apie ASM failo formatą ir API, kurios gali kurti ir atidaryti ASM failus.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Kas yra ASM failas? ##

ASM failas yra programa, parašyta žemo lygio programavimo kalba, žinoma kaip asamblėjos kalba. Jis pirmiausia naudojamas rašyti su aparatūra susijusį kodą, pavyzdžiui, programuoti mikrovaldiklius. Programa parašyta naudojant paprastą asamblėjos kalbos sintaksę, kuri apima operatorius ir operandus įvairioms operacijoms atlikti. ASM failai rašomi ir redaguojami teksto rengyklėse ir vykdomi naudojant surinkimo programą, tokią kaip HLA, MASM, FASM, NASM arba GAS.

## ASM failo formatas

ASM failus sudaro seka operacijų, kurias vykdo surinkėjas, kad sugeneruotų **objekto kodą**. Gautas objekto kodas yra mnemonikos ir adresavimo režimų derinių vertimas į jų skaitmeninius atitikmenis.

### ASM failo formato pavyzdys

Toliau pateikiamas **Hello World** programos, skirtos x86 architektūrai, pavyzdys.
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

## Nuoroda ##

* [Asamblėjos kalba – Vikipedija](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Language – pagrindinė sintaksė](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


