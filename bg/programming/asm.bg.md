{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM файлов формат – файлов формат на изходния код на асемблерния език",
  "description":"Научете за ASM файловия формат и API, които могат да създават и отварят ASM файлове.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Какво е ASM файл? ##

ASM файлът е програма, написана на езика за програмиране от ниско ниво, известен като асемблер. Използва се предимно за писане на код, свързан с хардуера, като например за програмиране на микроконтролери. Програмата е написана с помощта на прост синтаксис на асемблерния език, който включва оператори и операнди за извършване на различни операции. ASM файловете се пишат и редактират в текстови редактори и се изпълняват с помощта на асемблерна програма като HLA, MASM, FASM, NASM или GAS.

## ASM файлов формат

ASM файловете се състоят от поредица от операции, които се изпълняват от асемблер за генериране на **обектен код**. Полученият обектен код е превод на комбинации от мнемоника и режими на адресиране в техните цифрови еквиваленти.

### Пример за ASM файлов формат

Следва пример за приложение **Hello World** за x86 архитектура.
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

## Референция ##

* [Език за асемблиране - от Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Език за асемблиране - основен синтаксис](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

