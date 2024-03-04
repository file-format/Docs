{
  "date": "2021-09-06",
  "keywords": [
"btr",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Btrieve duomenų bazė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie BTR failo formatą ir API, kurios gali kurti ir atidaryti BTR failus.",
  "title": "BTR – Btrieve duomenų bazės failas",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bt-ltr"
}
},
  "lastmod": "2021-09-06"
}

## Kas yra BTR failas?

Failas su plėtiniu .btr yra duomenų bazės failas, sukurtas naudojant [Btrieve](https://www.actian.com/) operacijų duomenų bazės programą. Skirtingai nuo reliacinių duomenų bazių valdymo sistemų (RBMS), Btrieve yra pagrįsta indeksuotos nuoseklios prieigos metodu (ISAM), kuris yra duomenų saugojimo būdas greitai gauti. BTR failas saugo įrašų rinkinį ir yra naudojamas ataskaitoms generuoti pagal reikalavimus. BTR failus galima atidaryti naudojant Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility ir Legend Software BTRIEVE Viewer.

## BTR failo struktūra – daugiau informacijos

Vidinė duomenų struktūra ir kiekvieno baito lygiavimas BTR failo struktūroje nėra viešai prieinamas. Tačiau Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * GNU C/C++
 * Micro Focus COBOL
 * Microsoft Visual Basic
 * Microsoft Visual C++
 * Watcom C/C++

Duomenų gavimas iš BTR failo priklauso nuo su juo susieto DDF failo. Be DDF nebus lengva gauti informaciją iš tokio failo.

## Nuorodos

* [Btrieve – Vikipedija](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

