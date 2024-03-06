{
  "date": "2021-02-25",
  "keywords": [
"ttc failu",
"ttc faila formātā",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC — TrueType kolekcijas faila formāts",
  "description": "TrueType kolekcijas (TTC) fails apvieno vairākus fontus vienā failā. Gan Apple, gan Microsoft izmantoja TTF operētājsistēmās Mac un Windows.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-lvc"
}
},
  "lastmod": "2021-02-25"
}

## Kas ir TTC fails?
TTC ir saīsināts kā TrueType kolekcija ir True Type formāta paplašinājums. TTC failā var apvienot vairākus fontu failus. Šie faili ir noderīgi, lai apvienotu vairākus fontus, kuriem ir daudz kopīgu glifu. Pirms Windows 2000 TTC faili tika izmantoti ķīniešu, japāņu un korejiešu Windows versijās, bet vēlāk atbalsts bija pieejams visos reģionos.


## Fontu kolekcijas faila struktūra 
TTC fails sastāv no TTC galvenes tabulas, tabulu direktorijiem un vairākām OpenType tabulām. TTC galvene ir jāatrod faila sākumā. Katram fontam ir jābūt pilnam tabulas direktorijam. TableDirectory formātam ir jābūt līdzīgam failam, kas nav apkopots. Tabulu skaits visos TTC faila direktorijos tiek aprēķināts no TTC faila sākuma.
Uz TTC faila tabulām ir atsauces, izmantojot to attiecīgo fontu tabulu direktoriju. Dažām OpenType tabulām ir jāparādās vairākas reizes, vienu reizi katram fontam, kas pievienots TTC. Savukārt pārējās tabulas TTC failā var koplietot ar vairākiem fontiem.

### TTC galvene
Līdz šim ir pieejamas divas TTC galvenes tabulas versijas:
- Versija 1.0 tiek izmantota TTC failiem bez ciparparakstiem.
- Versiju 2.0 var izmantot TTC failiem ar ciparparakstiem vai bez tiem.
Šeit ir abu versiju TTC galvenes tabulas:

**TTC galvenes versija 1.0:**

|Tips|Nosaukums|Apraksts|
---|---|---|
|TAG|ttcTag|Fontu kolekcijas ID virkne: ttcf (izmanto fontiem ar CFF vai CFF2 kontūrām, kā arī TrueType kontūrām)|
|uint16|majorVersion|TTC galvenes galvenā versija, = 1.|
|uint16|minorVersion|Neliela TTC galvenes versija, = 0.|
|uint32|numFonts|Fontu skaits TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Nobīdes uz TableDirectory katram fontam no faila sākuma|

**TTC galvenes versija 2.0:**

|Tips|Nosaukums|Apraksts|
---|---|---|
|TAG|ttcTag |Fontu kolekcijas ID virkne: 'ttcf'|
|uint16| majorVersion |TTC galvenes galvenā versija, = 2.|
|uint16| minorVersion |Neliela TTC galvenes versija, = 0.|
|uint32| numFonts |Fontu skaits TTC|
|Nobīde32| tableDirectoryOffsets[numFonts] |Nobīdes uz TableDirectory katram fontam no faila sākuma|
|uint32| dsigTag |Tags, kas norāda, ka pastāv DSIG tabula, 0x44534947 ('DSIG') (nulle, ja nav paraksta)|
|uint32| dsigLength |DSIG tabulas garums (baitos) (nulle, ja nav paraksta)|
|uint32| dsigOffset |DSIG tabulas nobīde (baitos) no TTC faila sākuma (nulle, ja nav paraksta)|

## Atsauces
 * [OpenType fonta fails](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

