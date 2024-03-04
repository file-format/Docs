{
  "date": "2019-10-11",
  "keywords": [
"tbz failą",
"tbz failo formatas",
"kas yra tbz failas",
"failą",
"tbz pavyzdys",
"tbz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TBZ – Bzip suspausto deguto archyvas",
  "description": "Sužinokite apie TBZ failo formatą ir API, kurios gali kurti ir atidaryti TBZ failus.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tb-ltz"
}
},
  "lastmod": "2021-04-05"
}

## Kas yra TBZ failas?

Failas su plėtiniu .tbz yra suglaudintas archyvas, kuris naudoja BZIP glaudinimą, kad sumažintų turinio failų dydį. TBZ failai iš tikrųjų yra UNIX [TAR](/compression/tar/) archyvuoti failai, kurie tada suglaudinami naudojant BZIP. Naujausias antrojo lygio glaudinimas yra [BZIP2](/compression/bz2/), kuris pakeitė BZIP. TBZ failo formatas tinka dideliems failams perkelti. TBZ failus galima atidaryti / išgauti naudojant tokias programas kaip 7-Zip, PeaZip ir jZip. Linux ir MacOS vartotojai taip pat gali atidaryti TBZ naudodami komandą BZIP2 iš terminalo lango.

## TBZ failo formatas

TBZ failai iš tikrųjų yra suspausti archyvai, sukurti naudojant BZIP/[BZIP2](/compression/bz2/) glaudinimą. Nėra oficialių šio failo formato specifikacijų. Tačiau neoficialus [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) rodo, kad .bz2 srautas susideda iš 4 baitų antraštės, po kurios seka nulis ar daugiau suspaustų blokų.

## Nuorodos Nr.

* [BZIP2 formato specifikacijos](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


