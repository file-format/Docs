{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM faila formāts — montāžas valodas pirmkoda faila formāts",
  "description":"Uzziniet par ASM faila formātu un API, kas var izveidot un atvērt ASM failus.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Kas ir ASM fails? ##

ASM fails ir programma, kas rakstīta zema līmeņa programmēšanas valodā, kas pazīstama kā montāžas valoda. To galvenokārt izmanto aparatūras koda rakstīšanai, piemēram, mikrokontrolleru programmēšanai. Programma ir uzrakstīta, izmantojot vienkāršu montāžas valodas sintaksi, kas ietver operatorus un operandus dažādu darbību veikšanai. ASM faili tiek rakstīti un rediģēti teksta redaktoros un tiek izpildīti, izmantojot montāžas programmu, piemēram, HLA, MASM, FASM, NASM vai GAS.

## ASM faila formāts

ASM faili sastāv no darbību secības, kuras izpilda montētājs, lai ģenerētu **objekta kodu**. Iegūtais objekta kods ir mnemonikas un adresācijas režīmu kombināciju tulkojums to skaitliskajos ekvivalentos.

### ASM faila formāta piemērs

Tālāk ir sniegts lietojumprogrammas **Hello World** piemērs x86 arhitektūrai.
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

## Atsauce Nr.

* [Assembly Language — Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Language — pamata sintakse](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


