{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASM Dosya Biçimi - Assembly Dili Kaynak Kodu Dosya Biçimi",
  "description":"ASM dosya formatı ve ASM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Bir ASM dosyası nedir? ##

Bir ASM dosyası, montaj dili olarak bilinen düşük seviyeli programlama dilinde yazılmış bir programdır. Öncelikle, mikro denetleyicileri programlamak gibi donanımla ilgili kod yazmak için kullanılır. Program, farklı işlemleri gerçekleştirmek için operatörler ve işlenenler içeren basit birleştirme dili sözdizimi kullanılarak yazılmıştır. ASM dosyaları metin editörlerinde yazılır ve düzenlenir ve HLA, MASM, FASM, NASM veya GAS gibi bir birleştirici program kullanılarak yürütülür.

## ASM Dosya Biçimi

ASM dosyaları, **nesne kodu** oluşturmak için bir derleyici tarafından yürütülen bir dizi işlemden oluşur. Ortaya çıkan nesne kodu, anımsatıcıların ve adresleme modlarının kombinasyonlarının sayısal eşdeğerlerine çevrilmesidir.

### ASM Dosya Biçimi Örneği

Aşağıda bir x86 mimarisi için **Merhaba Dünya** uygulamasının bir örneği bulunmaktadır.
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

## Referans ##

* [Assembly Language - Wikipedia'dan](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

