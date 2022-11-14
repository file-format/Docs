{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file ASM - Formato file codice sorgente linguaggio assembly",
  "description":"Scopri il formato di file ASM e le API che possono creare e aprire file ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Che cos'è un file ASM? ##

Un file ASM è un programma scritto nel linguaggio di programmazione di basso livello noto come linguaggio assembly. Viene utilizzato principalmente per la scrittura di codice relativo all'hardware, ad esempio per la programmazione di microcontrollori. Il programma è scritto utilizzando una semplice sintassi del linguaggio assembly che include operatori e operandi per eseguire diverse operazioni. I file ASM vengono scritti e modificati in editor di testo e vengono eseguiti utilizzando un programma assembler come HLA, MASM, FASM, NASM o GAS.

## Formato file ASM

I file ASM sono costituiti da una sequenza di operazioni eseguite da un assemblatore per generare **codice oggetto**. Il codice oggetto risultante è una traduzione di combinazioni di mnemonici e modalità di indirizzamento nei loro equivalenti numerici.

### Esempio di formato file ASM

Di seguito è riportato un esempio di applicazione **Hello World** per un'architettura x86.
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

## Riferimento ##

* [linguaggio Assembly - di Wikipedia](https://en.wikipedia.org/wiki/lingua_Assembly)
* [linguaggio assembly - sintassi di base](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

