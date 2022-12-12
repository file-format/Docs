{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу ASM - формат файлу вихідного коду мови асемблера",
  "description":"Дізнайтеся про формат файлу ASM та API, які можуть створювати та відкривати файли ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Що таке файл ASM? ##

Файл ASM — це програма, написана мовою програмування низького рівня, відомою як мова асемблера. Він в основному використовується для написання коду, пов’язаного з апаратним забезпеченням, наприклад для програмування мікроконтролерів. Програма написана з використанням простого синтаксису мови асемблера, який включає оператори та операнди для виконання різних операцій. Файли ASM пишуться та редагуються в текстових редакторах і виконуються за допомогою програми асемблера, наприклад HLA, MASM, FASM, NASM або GAS.

## Формат файлу ASM

Файли ASM складаються з послідовності операцій, які виконує асемблер для створення **об’єктного коду**. Результуючий об'єктний код є перекладом комбінацій мнемотехніки та режимів адресації в їхні числові еквіваленти.

### Приклад формату файлу ASM

Нижче наведено приклад програми **Hello World** для архітектури x86.
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

## Посилання ##

* [Мова складання - Вікіпедія](https://en.wikipedia.org/wiki/Assembly_language)
* [Мова складання – базовий синтаксис](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

