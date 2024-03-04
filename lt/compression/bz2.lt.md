{
  "date": "2019-10-11",
  "keywords": [
"bz2 failą",
"bz2 failo formatas",
"kas yra bz2 failas",
"failą",
"bz2 pavyzdys",
"bz2 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 – suspausto failo formatas",
  "description": "Sužinokite, kas yra BZ2 failas ir API, kurios gali kurti ir atidaryti BZ2 failus.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-lt2"
}
},
  "lastmod": "2020-09-05"
}

## Kas yra BZ2 failas?

BZ2 yra suspausti failai, sukurti naudojant [BZIP2](http://www.bzip.org/) atvirojo kodo glaudinimo metodą, dažniausiai UNIX arba Linux sistemoje. Jis naudojamas vieno failo suspaudimui ir nėra skirtas kelių failų archyvavimui. Tai skiriasi nuo TAR failo formato tose pačiose platformose, kurios suarchyvuoja kelis failus į vieną failą, bet nesuglaudina. Failus, suspaustus kaip BZ2, galima išspausti tokiomis programomis kaip [WinZip](https://www.winzip.com/win/en/). BZIP2 naudoja Run-Length Encoding (RLE) arba [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) glaudinimo algoritmą, kad pasiektų aukštą glaudinimo lygį.

## BZ2 failo formatas

Nėra oficialių šio failo formato specifikacijų. Tačiau neoficialus [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) rodo, kad .bz2 srautas susideda iš 4 baitų antraštės, po kurios seka nulis ar daugiau suspaustų blokų. Iš karto po jo rodomas srauto pabaigos žymeklis, kuriame yra 32 bitų CRC, skirtas visam apdoroto teksto srautui. Tarp suspaustų blokų nėra paminkštinimo ir visi blokai yra suderinti bitais.

## Išpakuokite / išskleiskite BZ2 failą

Galite išpakuoti BZ2 failą Windows ir Mac OS naudodami programinę įrangą, pvz., WinZip. Linux terminale ši komanda.

```
bzip2 -d filename.bz2
```

## Nuorodos

* [BZIP2 formato specifikacijos](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


