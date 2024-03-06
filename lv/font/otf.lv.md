{
  "date": "2020-08-20",
  "keywords": [
"otf failu",
"otf faila formātā",
"kas ir otf fails",
"failu",
"otf piemērs",
"otf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF — TrueType fonta faila formāts",
  "description": "Uzziniet par OTF failu formātu un API, kas var izveidot un atvērt OTF failus.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-lvf"
}
},
  "lastmod": "2020-09-21"
}

## Kas ir OTF fails?

Fails ar paplašinājumu .otf attiecas uz OpenType fonta formātu. OTF fontu formāts ir vairāk mērogojams un paplašina esošās [TTF](/font/ttf/) formātu funkcijas digitālajai tipogrāfijai. Microsoft un Adobe izstrādātais OTF apvieno PostScript un TrueType fontu formātu funkcijas. Tas padara OTF formātu, lai pielāgotos lielākajai daļai rakstīšanas sistēmu, un tāpēc tas tiek vienmērīgi izmantots lielākajās datoru platformās. OpenType fonta formātu atbalsta Mac OS X un Windows 2000 un jaunākas versijas.

## Īsa vēsture

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Modifikācijas ietvēra arī piemērotāku fonta formātu ieviešanu, kas atbilst arī Adobe Type 1 (PostScript) fontu formātu funkcijām.

Adobe 1996. gadā pievienojās Microsoft centieniem aizstāt gan Apple TrueType, gan savus Type 1 fontu formātus. Tā rezultātā tika apvienoti abi pamatā esošie fontu formāti, lai pārvarētu ierobežojumus un pievienotu jaunus paplašinājumus. Šī jaunā tehnoloģija tika ieviesta tajā pašā gadā ar nosaukumu **OpenType**.

## OTF faila formāta specifikācijas

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF datu tipi
OTF faili izmanto šādus datu tipus, kas visi ir Big Endian.

|Datu tips| Apraksts|
---|---|
|uint8| 8 bitu neparakstīts vesels skaitlis.|
|int8| 8 bitu vesels skaitlis.|
|uint16| 16 bitu neparakstīts vesels skaitlis.|
|int16| 16 bitu vesels skaitlis.|
|uint24| 24 bitu neparakstīts vesels skaitlis.|
|uint32| 32 bitu neparakstīts vesels skaitlis.|
|int32| 32 bitu vesels skaitlis.|
|Fiksēts| 32 bitu zīme fiksēta punkta numurs (16.16)|
|FWORD| int16, kas apraksta daudzumu fontu noformējuma vienībās.|
|UFWORD| uint16, kas apraksta daudzumu fontu noformējuma vienībās.|
|F2DOT14| Fiksēts skaitlis ar 16 bitu zīmi ar zemo 14 bitu daļu (2.14).|
|LONGDATETIME| Datums un laiks, kas attēlots sekunžu skaitā kopš 12:00 pusnakts, 1904. gada 1. janvāris, UTC. Vērtība tiek attēlota kā 64 bitu vesels skaitlis ar zīmi.|
|Taga| Četru uint8 masīvs (garums = 32 biti), ko izmanto, lai identificētu tabulu, dizaina variantu asi, skriptu, valodas sistēmu, līdzekli vai bāzes līniju|
|Nobīde16| Īsā nobīde pret tabulu, tāpat kā uint16, NULL nobīde = 0x0000|
|Nobīde32| Garā nobīde pret tabulu, tāpat kā uint32, NULL nobīde = 0x00000000|
|Versija16Punkts16| 32 bitu vērtība ar galveno un mazāko versiju numuriem. (Skatiet tabulas versiju numurus.)|

### OTF tabulu direktorijs

OTF fails sākas ar tabulas direktoriju. Šis direktorijs ir augstākā līmeņa tabulu kolekcija fonta failā. Atkarībā no fontu skaita failā tabulas direktorijs var atrasties dažādās faila vietās. Piemēram, ja fonta failā ir tikai viens fonts, tabulas direktorijs sākas ar faila 0. baitu. Vairāku OpenType fontu kolekcijas gadījumā
tabulas direktorija sākums ir norādīts TTCHader.

|Tips |Vārds |Apraksts|
---|---|---|
|uint32 |sfntVersion| 0x00010000 vai 0x4F54544F ('OTTO')|
|uint16| numTables |Tabulu skaits.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, kur **” ir eksponēšanas operators).|
|uint16 |entrySelector Log2 ar maksimālo jaudu 2, kas ir mazāka vai vienāda ar numTables (log2(searchRange/16), kas ir vienāds ar floor(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - meklēšanas diapazons).|
|tableRecord| tableRecords[numTables] |Tabulas ierakstu masīvs — viens katrai fonta augstākā līmeņa tabulai|


### Tabulas ieraksts

Katrai fonta augstākā līmeņa tabulai ir tabulas ieraksts, kas sastāv no šādiem laukiem.

|Tips| Vārds| Apraksts|
---|---|---|
|Taga| tableTag| Tabulas identifikators.|
|uint32| kontrolsumma| Kontrolsumma šai tabulai.|
|Nobīde32| nobīde| Nobīde no fonta faila sākuma.|
|uint32| garums Šīs tabulas garums.|

Katra OpenType fonta faila tabula ir attēlota ar nosaukumiem, kas pazīstami kā tabulas tagi. Ir obligāti, lai visi masīva ieraksti tiktu sakārtoti augošā secībā pēc atzīmes.

## Atsauces
 * [OpenType fontu specifikācijas no Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType pārskats](https://learn.microsoft.com/en-us/typography/truetype/)

