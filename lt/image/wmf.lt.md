{
  "date": "2019-10-11",
  "keywords": [
"wmf failą",
"wmf failo formatas",
"kas yra wmf failas",
"failą",
"wmf pavyzdys",
"wmf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMF – Microsoft Windows metafailo formatas",
  "description": "Sužinokite apie WMF failo formatą ir API, kurios gali kurti ir atidaryti WMF failus.",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra WMF failas?

Failai su WMF plėtiniu yra Microsoft Windows metafailas (WMF), skirtas saugoti vektorinių ir bitmap formato vaizdų duomenis. Kad būtų tiksliau, WMF priklauso grafinių failų formatų vektorinių failų formatų kategorijai, kuri nepriklauso nuo įrenginio. Windows grafinio įrenginio sąsaja (GDI) vaizdui ekrane rodyti naudoja WMF faile saugomas funkcijas. Vėliau buvo paskelbta labiau patobulinta WMF versija, žinoma kaip patobulinti meta failai (EMF), todėl formatas tapo turtingesnis. Praktiškai WMF yra panašūs į SVG.

## WMF failo formato specifikacijos ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. Failo formatas susideda iš kintamo ilgio įrašų, kuriuose yra grafikos piešimo komandų, objektų apibrėžimų ir savybių, serijos. Kadangi WMF failai yra pagrįsti komandomis, pateiktomis GDI vaizdui piešti, jie taip pat žinomi kaip skaitmeninis vaizdo įrašas, kurį galima atkurti norint atkurti tą vaizdą. Išsamias WMF failo formato specifikacijas galima rasti internete ir jas reikia naudoti kuriant programas, skirtas dirbti su WMF failais. WMF failas suskirstytas į:

* WMF antraštės įrašas

* WMF įrašas (-ai)

* WMF failo pabaigos įrašas


### WMF antraštės įrašas ###

**META_HEADER įraše** yra informacijos, apibrėžiančios metafailo charakteristikas, įskaitant:

* Metafailo tipas

* Metafailo versija

* Metafailo dydis

* Metafaile apibrėžtų objektų skaičius

* Didžiausio vieno įrašo metafaile dydis


### WMF talpinamos antraštės įrašas ###

**META_PLACEABLE įraše** yra papildomos informacijos apie vaizdą, įskaitant:

* Apribojantis stačiakampis

* Loginis vieneto dydis, skirtas mastelio keitimui

* Kontrolinė suma, skirta patvirtinimui


### WMF rekordas ###

WMF įrašai turi bendrą formatą, kuris nurodytas specifikacijų dokumente. Kiekviename WMF įraše yra ši informacija:

* Rekordo dydis

* Įrašymo funkcija

* Parametrai, jei tokių yra, įrašymo funkcijai


## Nuorodos Nr.

* [[MS-WMF]: Windows metafailo formatas](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [Windows MetaFile – Vikipedija](https://en.wikipedia.org/wiki/Windows_Metafile)


