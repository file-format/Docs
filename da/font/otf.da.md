{
  "date": "2020-08-20",
  "keywords": [
"otf fil",
"otf filformat",
"hvad er en otf-fil",
"fil",
"andet eksempel",
"otf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF - TrueType Font File Format",
  "description": "Lær om OTF-filformat og API'er, der kan oprette og åbne OTF-filer.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-daf"
}
},
  "lastmod": "2020-09-21"
}

## Hvad er OTF fil?

En fil med filtypenavnet .otf refererer til OpenType-skrifttypeformatet. OTF-skrifttypeformatet er mere skalerbart og udvider de eksisterende funktioner i [TTF](/font/ttf/)-formater til digital typografi. OTF er udviklet af Microsoft og Adobe og kombinerer funktionerne i PostScript- og TrueType-skrifttypeformater. Dette gør OTF-format til at rumme flertalsskrivesystemer, og det er derfor, det bruges ensartet på større computerplatforme. OpenType-skrifttypeformatet understøttes af Mac OS X og Windows 2000 og nyere.

## Kort historie

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Ændringerne inkluderede også for at introducere et mere passende skrifttypeformat, der også opfylder funktionerne i Adobes Type 1 (PostScript) skrifttypeformater.

Adobe sluttede sig i 1996 til Microsoft i deres bestræbelser på at afløse både Apples TrueType og dets egne Type 1-skrifttypeformater. Dette resulterede i en kombination af begge underliggende skrifttypeformater for at overvinde begrænsningerne og tilføje nye udvidelser. Denne nye teknologi blev introduceret samme år med navnet **OpenType**.

## OTF-filformatspecifikationer

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF-datatyper
OTF-filer bruger følgende datatyper, som alle er i Big Endian.

|Datatype| Beskrivelse|
---|---|
|uint8| 8-bit usigneret heltal.|
|int8| 8-bit fortegnet heltal.|
|uint16| 16-bit heltal uden fortegn.|
|int16| 16-bit fortegnet heltal.|
|uint24| 24-bit usigneret heltal.|
|uint32| 32-bit heltal uden fortegn.|
|int32| 32-bit fortegnet heltal.|
|Fixet| 32-bit underskrevet fastpunktnummer (16.16)|
|FWORD| int16, der beskriver en mængde i skrifttypedesignenheder.|
|UFWORD| uint16, der beskriver en mængde i skrifttypedesignenheder.|
|F2DOT14| 16-bit fortegnet fast tal med de lave 14 bits brøk (2.14).|
|LONGDATETIME| Dato og klokkeslæt repræsenteret i antal sekunder siden 12:00 midnat, 1. januar 1904, UTC. Værdien er repræsenteret som et 64-bit heltal med fortegn.|
|Tag| Array af fire uint8s (længde = 32 bit) bruges til at identificere en tabel, designvariationsakse, script, sprogsystem, feature eller baseline|
|Offset16| Kort offset til en tabel, samme som uint16, NULL offset = 0x0000|
|Offset32| Lang offset til en tabel, samme som uint32, NULL offset = 0x00000000|
|Version16Punkt16| Pakket 32-bit værdi med større og mindre versionsnumre. (Se tabelversionsnumre.)|

### OTF-tabeller Directory

En OTF-fil starter med en tabelmappe. Denne mappe er samlingen på øverste niveau af tabellerne i skrifttypefilen. Afhængigt af antallet af skrifttyper i en fil, kan tabelbiblioteket være placeret på en anden placering i filen. For eksempel, hvis skrifttypefilen kun har én skrifttype, starter tabelbiblioteket ved filens byte 0. I tilfælde af flere OpenType-skrifttyper,
tabelbibliotekets begyndelse er angivet i TTCHeader.

|Typ |Navn |Beskrivelse|
---|---|---|
|uint32 |sfntVersion| 0x00010000 eller 0x4F54544F ('OTTO')|
|uint16| numTables |Antal tabeller.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, hvor ** er en eksponentieringsoperator).|
|uint16 |entrySelector Log2 af den maksimale effekt på 2 mindre end eller lig med numTables (log2(searchRange/16), som er lig med floor(log2(antalTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[antalTables] |Tabelposter-array – en for hver tabel på øverste niveau i skrifttypen|


### Tabel Record

For hver tabel på øverste niveau i skrifttypen er der en tabelpost, som består af følgende felter.

|Type| Navn| Beskrivelse|
---|---|---|
|Tag| tabelTag| Tabelidentifikator.|
|uint32| kontrolsum| Kontrolsum for denne tabel.|
|Offset32| offset| Forskydning fra begyndelsen af skrifttypefil.|
|uint32| længde Længde af denne tabel.|

Hver tabel i OpenType-skrifttypefilen er repræsenteret af navne kendt som tabelmærker. Det er et must for alle poster i arrayet at blive sorteret i stigende rækkefølge efter tag.

## Referencer
 * [OpenType Font Specifications fra Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType Oversigt](https://learn.microsoft.com/en-us/typography/truetype/)

