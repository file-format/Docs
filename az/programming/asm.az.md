{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM Fayl Format - Assembly Language Source Code File Format",
  "description":"ASM faylları yarada və aça bilən ASM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-az",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## ASM faylı nədir? ##

ASM faylı montaj dili kimi tanınan aşağı səviyyəli proqramlaşdırma dilində yazılmış proqramdır. O, ilk növbədə mikro nəzarətçilərin proqramlaşdırılması kimi hardware ilə əlaqəli kodun yazılması üçün istifadə olunur. Proqram müxtəlif əməliyyatları yerinə yetirmək üçün operatorları və operandları ehtiva edən sadə montaj dili sintaksisindən istifadə etməklə yazılmışdır. ASM faylları mətn redaktorlarında yazılır və redaktə edilir və HLA, MASM, FASM, NASM və ya GAS kimi assembler proqramından istifadə etməklə yerinə yetirilir.

## ASM fayl formatı

ASM faylları **obyekt kodu** yaratmaq üçün assembler tərəfindən yerinə yetirilən əməliyyatlar ardıcıllığından ibarətdir. Nəticə obyekt kodu mnemonika və ünvanlama rejimlərinin birləşmələrinin onların ədədi ekvivalentlərinə tərcüməsidir.

### ASM Fayl Formatının Nümunəsi

Aşağıda x86 arxitekturası üçün **Salam Dünya** tətbiqinin nümunəsi verilmişdir.
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

## İstinad ##

* [Assembly Dili - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Dili - Əsas Sintaksis](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


