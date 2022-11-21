{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM File Format - Assembly Language Source Code File Format",
  "description":"Saiba mais sobre o formato de arquivo ASM e APIs que podem criar e abrir arquivos ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## O que é um arquivo ASM? ##

Um arquivo ASM é um programa escrito na linguagem de programação de baixo nível conhecida como linguagem assembly. É usado principalmente para escrever código relacionado a hardware, como para programar microcontroladores. O programa é escrito usando a sintaxe simples da linguagem assembly que inclui operadores e operandos para realizar diferentes operações. Os arquivos ASM são escritos e editados em editores de texto e executados usando um programa montador como HLA, MASM, FASM, NASM ou GAS.

## Formato de arquivo ASM

Os arquivos ASM consistem em uma sequência de operações que são executadas por um montador para gerar **código objeto**. O código objeto resultante é uma tradução de combinações de mnemônicos e modos de endereçamento em seus equivalentes numéricos.

### Exemplo de formato de arquivo ASM

Veja a seguir um exemplo de aplicativo **Hello World** para uma arquitetura x86.
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

## Referência ##

* [Assembly Language - pela Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

