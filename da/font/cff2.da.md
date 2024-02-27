{
  "date": "2020-08-20",
  "keywords": [
"cff2 fil",
"cff2 filformat",
"hvad er en cff2 fil",
"fil",
"cff2 eksempel",
"cff2 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 - Kompakt skrifttypefilformat version 2",
  "description": "Lær om CFF2-filformat og API'er til at oprette og åbne CFF2-filer.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-da2"
}
},
  "lastmod": "2020-10-21"
}

## Hvad er en CFF2 fil?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. Det kan ikke bruges som et selvstændigt program og afhænger af data i andre OpenType-tabeller.

## CFF2 filformat

[CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) indeholder detaljer om internt datalayout, datatyper, tabeller og anden intern information om filformatet. Det kan henvises til udviklerens reference. Nogle af detaljerne om disse er som følger.

### Datalayout

De binære data i CFF2-filformatet er logisk organiseret som et antal separate datastrukturer. Layoutet i de binære data er som vist i følgende tabel.

|Indgang |Kommentarer|
---|---|
|Overskrift |Fast placering|
|Top DICT| Fast placering|
|Global Subr INDEX| Fast placering|
|Variation |Butik|
|FDSælg |Vis kun, hvis der er mere end én Font DICT i Font DICT INDEX.|
|Skrifttype DICT INDEX ||
|Array of Font DICT| Inkluderet i Font DICT INDEX.|
|Privat DICT| En pr. skrifttype DICT.|

Kun de tre første strukturer er baseret på faste placeringer. Resterende nås via offsets, og deres bestilling kan ændres.

### Datatyper

CFF2-filformatet bruger følgende datatyper.

|Navn |Område |Beskrivelse|
---|---|---|
|uint8 |0 til 255 |8-bit usigneret nummer|
|uint16 |0 til 65535| 16-bit usigneret nummer|
|uint32 |0 til 4294967295| 32-bit usigneret nummer|
|Offset |varierer| 1, 2, 3 eller 4 byte offsets (specificeret af OffSize-feltet i en indekstabel)|
|OffSize |1 til 4| 1-byte usigneret tal angiver størrelsen af et eller flere forskydningsfelter|

Den gemmer alle multi-byte numeriske data og offset felter i big-endian byte rækkefølge. CFF2-formatet er fri for udfyldningsbytes, da det ikke overholder nogen tilpasningsrestriktioner.

### DICT-data

CFF2-filer indeholder skrifttypeordbogsdataene som nøgle-værdi-par i et kompakt tokeniseret format. Ordbogsnøgler er kodet som 1 eller 2 byte-operatorer, og ordbogsværdier er kodet som numeriske operander i variabel størrelse. Der er tre strukturer, der bruger DICT-dataformatet: `Top DICT`, `Font DICT` og `Privat DICT`. Et antal heltalsoperandtyper af varierende størrelse er defineret og kodet som vist i følgende tabel (første byte af operand er b0, anden er b1, og så videre).

|Størrelse |b0 interval |Værdiinterval |Værdiberegning|
---|---|---|---|
|1 |32 til 246| -107 til +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 til +32767| b1 << 8 | b2|
|5 |29| -(2^31) til +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Header

De binære data begynder med en header med formatet vist i tabel nedenfor.

|Typ |Navn |Beskrivelse|
---|---|---|
|uint8| majorVersion| Formater større version. Indstil til 2.|
|uint8| minorVersion| Formater mindre version. Indstil til nul.|
|uint8| headerStørrelse| Overskriftsstørrelse (bytes).|
|uint16| topDictLength| Længde af Top DICT-struktur i bytes.|

## Referencer

 * [CFF2-filformat](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

