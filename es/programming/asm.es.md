{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ASM - Formato de archivo de código fuente de lenguaje ensamblador",
  "description":"Obtenga información sobre el formato de archivo ASM y las API que pueden crear y abrir archivos ASM",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## ¿Qué es un archivo ASM? ##

Un archivo ASM es un programa escrito en el lenguaje de programación de bajo nivel conocido como lenguaje ensamblador. Se utiliza principalmente para escribir código relacionado con el hardware, como para programar microcontroladores. El programa está escrito utilizando una sintaxis de lenguaje ensamblador simple que incluye operadores y operandos para llevar a cabo diferentes operaciones. Los archivos ASM se escriben y editan en editores de texto y se ejecutan mediante un programa ensamblador como HLA, MASM, FASM, NASM o GAS.

## Formato de archivo ASM

Los archivos ASM constan de una secuencia de operaciones que ejecuta un ensamblador para generar **código de objeto**. El código objeto resultante es una traducción de combinaciones de mnemónicos y modos de direccionamiento a sus equivalentes numéricos.

### Ejemplo de formato de archivo ASM

A continuación se muestra un ejemplo de la aplicación **Hello World** para una arquitectura x86.
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

## Referencia ##

* [Lenguaje ensamblador - por Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Lenguaje ensamblador: sintaxis básica] (https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

