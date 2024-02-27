{
  "date": "2021-02-25",
  "keywords": [
"ttc filen",
"ttc filformat",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC - TrueType Collection File Format",
  "description": "En TrueType Collection-fil (TTC) kombinerer flere skrifttyper til en enkelt fil. Både Apple og Microsoft brugte TTF på Mac- og Windows-operativsystemer.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-dac"
}
},
  "lastmod": "2021-02-25"
}

## Hvad er en TTC fil?
TTC er forkortet som TrueType Collection er en udvidelse af True Type-formatet. En TTC-fil kan kombinere de flere skrifttypefiler til den. Disse filer er gavnlige til at kombinere flere skrifttyper, der deler mange glyffer til fælles. Før Windows 2000 blev TTC-filerne brugt i kinesiske, japanske og koreanske versioner af Windows, men senere var support tilgængelig for alle regioner.


## Strukturen af skrifttypesamlingsfil 
En TTC-fil består af en TTC-header-tabel, tabelmapper og flere OpenType-tabeller. TTC-headeren skal findes i starten af filen. En komplet tabelmappe for hver skrifttype skal eksistere. TableDirectory-formatet skal ligne det, der eksisterede i en ikke-samlingsfil. Tabellen tæller i alle mapper i en TTC-fil, beregnes fra starten af en TTC-fil.
Tabellerne i en TTC-fil refereres gennem tabelbiblioteket for deres respektive skrifttyper. Nogle få af OpenType-tabellerne skal vises flere gange, én gang for hver skrifttype, der tilføjes i TTC. Hvorimod de andre tabeller kan deles af flere skrifttyper i TTC-filen.

### TTC Header
To versioner af TTC Header-tabellen er tilgængelige indtil videre:
- Version 1.0 bruges til TTC-filer uden digitale signaturer.
- Version 2.0 kan bruges til TTC-filer med eller uden digitale signaturer.
Her er TTC Header-tabellerne for begge versioner:

**TTC Header Version 1.0:**

|Type|Navn|Beskrivelse|
---|---|---|
|TAG|ttcTag|Font Collection ID-streng: 'ttcf' (bruges til skrifttyper med CFF- eller CFF2-konturer samt TrueType-konturer)|
|uint16|majorVersion|Større version af TTC-headeren, = 1.|
|uint16|minorVersion|Mindre version af TTC-headeren, = 0.|
|uint32|numFonts|Antal skrifttyper i TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array af forskydninger til TableDirectory for hver skrifttype fra begyndelsen af filen|

**TTC Header version 2.0:**

|Type|Navn|Beskrivelse|
---|---|---|
|TAG|ttcTag |Font Collection ID-streng: 'ttcf'|
|uint16| majorVersion |Større version af TTC-headeren, = 2.|
|uint16| minorVersion |Minorversion af TTC Header, = 0.|
|uint32| numFonts |Antal skrifttyper i TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Array af offsets til TableDirectory for hver skrifttype fra begyndelsen af filen|
|uint32| dsigTag |Tag, der angiver, at der eksisterer en DSIG-tabel, 0x44534947 ('DSIG') (null hvis ingen signatur)|
|uint32| dsigLength |Længden (i bytes) af DSIG-tabellen (nul hvis ingen signatur)|
|uint32| dsigOffset |Forskydningen (i bytes) af DSIG-tabellen fra begyndelsen af TTC-filen (null hvis ingen signatur)|

## Referencer
 * [OpenType Font File](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

