{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File ASM - Format File Kode Sumber Bahasa Rakitan",
  "description":"Pelajari tentang format file ASM dan API yang dapat membuat dan membuka file ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Apa itu file ASM? ##

File ASM adalah program yang ditulis dalam bahasa pemrograman tingkat rendah yang dikenal sebagai bahasa rakitan. Ini terutama digunakan untuk menulis kode terkait perangkat keras seperti untuk pemrograman pengontrol mikro. Program ditulis menggunakan sintaks bahasa rakitan sederhana yang menyertakan operator dan operan untuk melakukan operasi yang berbeda. File ASM ditulis dan diedit dalam editor teks dan dijalankan menggunakan program assembler seperti HLA, MASM, FASM, NASM, atau GAS.

## Format File ASM

File ASM terdiri dari urutan operasi yang dijalankan oleh assembler untuk menghasilkan **kode objek**. Kode objek yang dihasilkan adalah terjemahan dari kombinasi mnemonik dan mode pengalamatan ke dalam ekuivalen numeriknya.

### Contoh Format File ASM

Berikut adalah contoh aplikasi **Hello World** untuk arsitektur x86.
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

## Referensi ##

* [Bahasa Assembly - oleh Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Bahasa Assembly - Sintaks Dasar](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

