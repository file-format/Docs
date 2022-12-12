{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku ASM - format pliku kodu źródłowego języka asemblera",
  "description":"Poznaj format pliku ASM i interfejsy API, które mogą tworzyć i otwierać pliki ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Czym jest plik ASM? ##

Plik ASM to program napisany w języku programowania niskiego poziomu znanym jako język asemblera. Jest używany głównie do pisania kodu związanego ze sprzętem, takiego jak programowanie mikrokontrolerów. Program jest napisany przy użyciu prostej składni asemblera, która zawiera operatory i operandy do wykonywania różnych operacji. Pliki ASM są zapisywane i edytowane w edytorach tekstu i są wykonywane przy użyciu programu asemblera, takiego jak HLA, MASM, FASM, NASM lub GAS.

## Format pliku ASM

Pliki ASM składają się z sekwencji operacji wykonywanych przez asembler w celu wygenerowania **kodu wynikowego**. Wynikowy kod obiektowy jest translacją kombinacji mnemoników i trybów adresowania na ich odpowiedniki numeryczne.

### Przykład formatu pliku ASM

Poniżej przedstawiono przykład aplikacji **Hello World** dla architektury x86.
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

## Odniesienie ##

* [Assembly Language – Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Język asemblera - podstawowa składnia](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

