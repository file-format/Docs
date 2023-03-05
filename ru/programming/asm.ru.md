{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла ASM - формат файла исходного кода языка ассемблера",
  "description":"Узнайте о формате файла ASM и API-интерфейсах, которые могут создавать и открывать файлы ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## .ASM вариант № ##

Файл ASM представляет собой программу, написанную на языке программирования низкого уровня, известном как язык ассемблера. Он в основном используется для написания кода, связанного с аппаратным обеспечением, например, для программирования микроконтроллеров. Программа написана с использованием простого синтаксиса языка ассемблера, который включает операторы и операнды для выполнения различных операций. Файлы ASM записываются и редактируются в текстовых редакторах и выполняются с использованием программы на ассемблере, такой как HLA, MASM, FASM, NASM или GAS.

## Формат файла ASM

Файлы ASM состоят из последовательности операций, выполняемых ассемблером для создания **объектного кода**. Результирующий объектный код представляет собой перевод комбинаций мнемоник и режимов адресации в их числовые эквиваленты.

### Пример формата файла ASM

Ниже приведен пример приложения **Hello World** для архитектуры x86.
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

## Ссылка ##

* [Язык ассемблера - по Википедии](https://en.wikipedia.org/wiki/Assembly_language)
* [Язык ассемблера — базовый синтаксис](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

