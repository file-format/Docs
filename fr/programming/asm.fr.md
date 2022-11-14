{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier ASM - Format de fichier de code source du langage d'assemblage",
  "description":"En savoir plus sur le format de fichier ASM et les API qui peuvent créer et ouvrir des fichiers ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Qu'est-ce qu'un fichier ASM ? ##

Un fichier ASM est un programme écrit dans le langage de programmation de bas niveau appelé langage d'assemblage. Il est principalement utilisé pour écrire du code lié au matériel, comme pour programmer des microcontrôleurs. Le programme est écrit en utilisant une syntaxe de langage d'assemblage simple qui inclut des opérateurs et des opérandes pour effectuer différentes opérations. Les fichiers ASM sont écrits et modifiés dans des éditeurs de texte et sont exécutés à l'aide d'un programme assembleur tel que HLA, MASM, FASM, NASM ou GAS.

## Format de fichier ASM

Les fichiers ASM consistent en une séquence d'opérations exécutées par un assembleur pour générer du **code objet**. Le code objet résultant est une traduction de combinaisons de mnémoniques et de modes d'adressage en leurs équivalents numériques.

### Exemple de format de fichier ASM

Voici un exemple d'application **Hello World** pour une architecture x86.
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

## Référence ##

* [Langage d'assemblage - par Wikipedia] (https://en.wikipedia.org/wiki/Assembly_language)
* [Langage d'assemblage - Syntaxe de base] (https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

