{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ASM-tiedostomuoto - Assembly Language lähdekoodin tiedostomuoto",
  "description":"Opi ASM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ASM-tiedostoja.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Mikä on ASM-tiedosto? ##

ASM-tiedosto on ohjelma, joka on kirjoitettu matalan tason ohjelmointikielellä, joka tunnetaan kokoonpanokielenä. Sitä käytetään ensisijaisesti laitteistoon liittyvän koodin kirjoittamiseen, kuten mikro-ohjainten ohjelmointiin. Ohjelma on kirjoitettu yksinkertaisella kokoonpanokielen syntaksilla, joka sisältää operaattorit ja operandit eri toimintojen suorittamiseksi. ASM-tiedostot kirjoitetaan ja muokataan tekstieditoreilla, ja ne suoritetaan käyttämällä kokoonpanoohjelmaa, kuten HLA, MASM, FASM, NASM tai GAS.

## ASM-tiedostomuoto

ASM-tiedostot koostuvat sarjasta toimintoja, jotka kokoaja suorittaa **objektikoodin** luomiseksi. Tuloksena oleva objektikoodi on käännös muistotekniikan ja osoitemoodien yhdistelmistä niiden numeerisiksi vastineiksi.

### Esimerkki ASM-tiedostomuodosta

Seuraavassa on esimerkki **Hello World** -sovelluksesta x86-arkkitehtuurille.
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

## Viite ##

* [Assembly Language - Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)

* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


