{
  "date": "2021-02-25",
  "keywords": [
"bdf tiedosto",
"bdf tiedostomuoto",
"mikä on bdf-tiedosto",
"tiedosto",
"bdf esimerkki",
"bdf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF - Glyph Bitmap Distribution Format",
  "description": "Opi BDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BDF-tiedostoja.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-fif"
}
},
  "lastmod": "2021-02-25"
}

## Mikä on BDF-tiedosto?
BDF-tiedostot ovat ihmisen luettavissa olevassa muodossa, ja ne jaetaan yleensä ASCII-koodauksella. Tiedosto alkaa koko kirjasimen yleisillä tiedoilla, minkä jälkeen tulevat tiedot ja bittikartat yksittäisille kuvioille. Sen tiedot näkyvät yhden koon suunnan fontille. Useampaan kuin yhteen suuntaan käytettävät mittarit voivat sisältyä yhteen tiedostoon. BDF-tiedostossa jokainen kohde on tiedostossa erillisellä tekstirivillä. Välilyöntejä käytetään rivin kohteiden erottamiseen.

## BDF tiedostomuoto
BDF-shortsit Glyph Bitmap Distribution Formatille; Adoben omistama tiedostomuoto bittikarttatyyppisten fonttien tallentamiseen. Sisältö on tekstitiedoston muodossa, joka on tarkoitettu sekä tietokoneella että ihmisen luettavaksi. BDF:ää käytetään erityisesti Unix X Window -ympäristöissä. Se on korvattu laajalti PCF-kirjasinmuodolla, jonka oletetaan olevan tehokkaampi, sekä OpenType- ja TrueType-fonteilla.
### BDF-tiedostorakenne
BDF-fonttitiedosto koostuu kolmesta osasta:

- yleinen osio, joka koskee kaikkia kirjasimen kuvioita.
- osio, jossa on erillinen merkintä jokaiselle kuviolle.
- ENDFONT-lausunto.

## Esimerkki
Tässä on esimerkkifontti, joka sisältää yhden kuvion ASCII-kirjaimelle A. Sen yleiset ilmoitukset alkavat STARTFONT-rivillä ja päättyvät CHARS-riville
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Viitteet
 * [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glyph Bitmap Distribution Format (BDF) -määritys](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

