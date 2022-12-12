{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ASM - Format de fișier cod sursă limbaj de asamblare",
  "description":"Aflați despre formatul de fișier ASM și despre API-urile care pot crea și deschide fișiere ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Ce este un fișier ASM? ##

Un fișier ASM este un program scris în limbajul de programare de nivel scăzut cunoscut sub numele de limbaj de asamblare. Este folosit în principal pentru scrierea codurilor legate de hardware, cum ar fi pentru programarea micro-controlerelor. Programul este scris folosind o sintaxă simplă a limbajului de asamblare care include operatori și operanzi pentru a efectua diferite operații. Fișierele ASM sunt scrise și editate în editori de text și sunt executate folosind un program de asamblare precum HLA, MASM, FASM, NASM sau GAS.

## Format de fișier ASM

Fișierele ASM constau dintr-o secvență de operații care sunt executate de un asamblator pentru a genera **cod obiect**. Codul obiect rezultat este o traducere a combinațiilor de mnemonici și moduri de adresare în echivalentele lor numerice.

### Exemplu de format de fișier ASM

Urmează un exemplu de aplicație **Hello World** pentru o arhitectură x86.
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

## Referință ##

* [Limba de asamblare - de la Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Limbajul de asamblare - Sintaxă de bază](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

