{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType Collection-bestandsindeling",
  "description":"Een TrueType Collection-bestand (TTC) combineert meerdere lettertypen in één bestand. Zowel Apple als Microsoft gebruikten TTF op Mac- en Windows-besturingssystemen.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Wat is een TTC-bestand?
De TTC wordt afgekort als TrueType Collection is een uitbreiding van het True Type-formaat. Een TTC-bestand kan de meerdere lettertypebestanden erin combineren. Deze bestanden zijn handig voor het combineren van meerdere lettertypen die veel glyphs gemeen hebben. Vóór Windows 2000 werden de TTC-bestanden gebruikt in Chinese, Japanse en Koreaanse versies van Windows, maar later was de ondersteuning beschikbaar voor alle regio's.


## De structuur van het lettertypeverzamelingsbestand
Een TTC-bestand bestaat uit een TTC Header-tabel, Table Directories en meerdere OpenType-tabellen. De TTC-header moet aan het begin van het bestand worden gevonden. Voor elk lettertype moet een volledige tabeldirectory aanwezig zijn. De TableDirectory-indeling moet vergelijkbaar zijn met die van een niet-verzamelingsbestand. De tabeltellingen in alle mappen binnen een TTC-bestand worden berekend vanaf het begin van een TTC-bestand.
Er wordt naar de tabellen in een TTC-bestand verwezen via de tabeldirectory van hun respectievelijke lettertypen. Een paar van de OpenType-tabellen moeten meerdere keren verschijnen, één keer voor elk lettertype dat in de TTC is toegevoegd. Terwijl de andere tabellen kunnen worden gedeeld door meerdere lettertypen in het TTC-bestand.

### TTC-koptekst
Er zijn tot nu toe twee versies van de TTC Header-tabel beschikbaar:
- Versie 1.0 wordt gebruikt voor TTC-bestanden zonder digitale handtekeningen.
- Versie 2.0 kan worden gebruikt voor TTC-bestanden met of zonder digitale handtekeningen.
Hier zijn de TTC Header-tabellen van beide versies:

**TTC-headerversie 1.0:**

|Type|Naam|Beschrijving|
---|---|---|
|TAG|ttcTag|Lettertypeverzameling ID-tekenreeks: 'ttcf' (gebruikt voor lettertypen met CFF- of CFF2-contouren en TrueType-contouren)|
|uint16|majorVersion|Hoofdversie van de TTC-header, = 1.|
|uint16|minorVersion|Minor-versie van de TTC-header, = 0.|
|uint32|numFonts|Aantal lettertypen in TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array van verschuivingen naar de TableDirectory voor elk lettertype vanaf het begin van het bestand|

**TTC-headerversie 2.0:**

|Type|Naam|Beschrijving|
---|---|---|
|TAG|ttcTag |Lettertypeverzameling ID-tekenreeks: 'ttcf'|
|uint16| majorVersion |Hoofdversie van de TTC-header, = 2.|
|uint16| minorVersion |Minor versie van de TTC Header, = 0.|
|uint32| numFonts |Aantal lettertypen in TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Array van verschuivingen naar de TableDirectory voor elk lettertype vanaf het begin van het bestand|
|uint32| dsigTag |Tag die aangeeft dat er een DSIG-tabel bestaat, 0x44534947 ('DSIG') (null indien geen handtekening)|
|uint32| dsigLength |De lengte (in bytes) van de DSIG-tabel (null indien geen handtekening)|
|uint32| dsigOffset |De offset (in bytes) van de DSIG-tabel vanaf het begin van het TTC-bestand (null indien geen handtekening)|

## Referenties
* [Het OpenType-lettertypebestand](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

