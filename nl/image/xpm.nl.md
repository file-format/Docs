{
  "date" : "2019-10-11",
  "keywords" :[ "xpm-bestand", "xpm-bestandsindeling", "wat is een xpm-bestand", "bestand", "xpm-voorbeeld", "xpm-bestandsextensie", "extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap-bestandsindeling",
  "description":"Meer informatie over XPM-bestandsindeling en API's die XPM-bestanden kunnen maken en openen.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een XPM-bestand?

Een bestand met de extensie .xpm is een afbeeldingsbestandsindeling die werd gebruikt door het X Windows-systeem. Het ondersteunt transparante pixels en richt zich meestal op het maken van pictogram-pixmaps. Het ondersteunt monochrome, gra-scale en kleuren pixmap-gegevens. Deze zijn ontworpen om met de hand te kunnen worden bewerkt en kunnen worden opgenomen in de [C](/nl/programming/c/)-code. Voor dit doel zijn XPM-bestanden in platte tekstbestandsindeling en volgen ze de C-programmeertaalsyntaxis. XPM-bestanden kunnen worden geopend met een verscheidenheid aan toepassingen voor het bekijken van afbeeldingen, zoals:
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView en Canvas X.

## XPM-bestandsindeling

Het XPM-bestandsformaat gebruikt de C-syntaxis om deze te integreren in C- en C++-programma's. Het bestaat uit de volgende zes verschillende secties.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

De secties zijn eigenlijk een reeks strings als volgt.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Hieronder volgen de details van elke sectie.

`<Values> ` - Deze sectie is een tekenreeks die vier of zes gehele getallen bevat met grondtal 10 en die overeenkomen met:

* pixmap breedte en hoogte
* aantal kleuren
* aantal karakters per pixel
* optionele hotspot-coördinaten en XPMEXT-tag

`<Colors> ` - Deze sectie bevat net zoveel tekenreeksen als er kleuren zijn. Elke string is als volgt:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Deze sectie bestaat uit<height> snaren en<width> \*<chars_per_pixel> karakters. Elk<chars_per_pixel> lengte string moet een van de eerder gedefinieerde groepen zijn in de<Colors> sectie.

`<Extension> ` - Het extensiegedeelte moet worden gelabeld, als het niet leeg is, in de<Values> sectie. Het kan bestaan uit meerdere<Extension> onderafdelingen die van de volgende twee typen kunnen zijn:

* een op zichzelf staande snaar die als volgt is samengesteld: XPMEXT<extension-name><extension-data>
* of een blok bestaande uit meerdere strings:XPMEXT<extension-name><related extension-data composed of several strings>

## Referenties

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM-handleiding](http://www.xfree86.org/current/xpm.pdf)

