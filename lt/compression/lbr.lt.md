{
  "date": "2021-04-08",
  "keywords": [
"mst failą",
"mst failo formatas",
"kas yra mst failas",
"failą",
"mst pavyzdys",
"mst failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LBR – LU bibliotekos archyvo failo formatas",
  "description": "Sužinokite apie LBR failo formatą ir API, kurios gali kurti ir atidaryti LBR failus.",
  "linktitle": "LBR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lb-ltr"
}
},
  "lastmod": "2021-04-19"
}

## Kas yra LBR failas?

Failas su plėtiniu .lbr yra archyvinis failas, sukurtas naudojant LU programą ir naudojamas CP/M ir DOS operacinėse sistemose devintajame dešimtmetyje. Jis nebenaudojamas ir buvo pakeistas šiuolaikiniais archyvavimo failų formatais. Formatas nesuglaudina narių failų ir veikia kaip jų talpyklos archyvas. Archyvavimo funkcija dažniausiai buvo naudojama archyvuotų failų perkėlimui internetu. Kadangi LBR nesiūlė glaudinimo, buvo naudojamos kitos priemonės, pvz., SQ arba CRUNCH, kad būtų suspausti narių failai iš anksto arba archyvuojant susidariusį archyvinį failą po archyvavimo, siekiant sumažinti jo dydį.

## LBR failo formatas

LBR file format was designed by Gary P. Novosielski and has no technical details available publicly. LBR files start with a 0x00 byte, followed by 11 spaces (0x20), then two 0x00 bytes, then two bytes that are not both 0x00. Kadangi yra konteinerio failo formatas, jį galima išgauti naudojant LU.COM ir NULU.COM.

## Nuorodos

* [LBR – Vikipedija](https://en.wikipedia.org/wiki/LBR_(file_format))


