{
  "date": "2020-08-20",
  "keywords": [
"fnt failą",
"fnt failo formatas",
"kas yra fnt failas",
"failą",
"fnt pavyzdys",
"fnt failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FNT – „Windows“ šrifto failas",
  "description": "Sužinokite apie FNT failo formatą ir API, kurios gali kurti ir atidaryti FNT failus.",
  "linktitle": "FNT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fn-ltt"
}
},
  "lastmod": "2020-10-30"
}

## Kas yra FNT failas?

Failas su plėtiniu .fnt yra šrifto failas, kuriame saugoma bendroji šrifto informacija Windows operacinėse sistemose. FNT failus dažniausiai pakeitė TrueType (.TTF) ir OpenType (.OTF) failų formatai, o nuo šiol tai yra pasenęs šrifto failo formatas. Šiuose failuose galima saugoti vieną vertintojo arba vektorinį šriftą. Visos įrenginių tvarkyklės palaiko Windows 2.x šriftus. Tačiau ne visos įrenginių tvarkyklės
palaiko Windows 3.0 versiją.

## FNT failo formatas

FNT failai gali saugoti vieną rastrinį arba vektorinį šriftą. Vektorinius formatus dažniau naudoja GDI, palyginti su rastrais, kur kiekvienos chartijos glifas apibrėžiamas naudojant mažą bitų schemą. Akivaizdi priežastis, kodėl .fnt pakeičiama .ttf ir .otf, yra jos rastrinis formatas.

### Šrifto failo antraštė
Rastrinių ir vektorinių šriftų failų pradžia yra įprasta, o vėliau pateikiama skirtinga kiekvieno failo tipo informacija. Windows 3.0 šrifto failo antraštėje yra šeši nauji toliau nurodyti laukai, kurie nustatomi į nulį, kad būtų užtikrintas suderinamumas su būsimomis Windows versijomis.

 * dVėliavos
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserved1

Norėdami gauti išsamios informacijos apie Windows 3.0 ir 2.0 antraštes, apsilankykite [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Nuorodos
 * [Šrifto failo formatas](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [Kaip įdiegti arba pašalinti šriftą sistemoje Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8- 7613-c76f-88d043b334b8)

