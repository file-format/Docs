{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2-fil - Web Open Font Format 2.0-fil",
  "description": "Lär dig om vad som är en WOFF2-fil och API:er som kan skapa och öppna WOFF2-fil.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-sv2"
}
},
  "lastmod": "2023-01-10"
}

## Vad är WOFF2 fil?

WOFF2 är ett typsnittsfilformat som är en mer komprimerad version av Web Open Font Format (WOFF). Det utvecklades som ett sätt att minska filstorleken på webbteckensnitt, så att de kan laddas snabbare och använda mindre bandbredd. WOFF2 använder en komprimeringsalgoritm som heter Brotli för att komprimera teckensnittsdata, vilket kan resultera i filstorlekar som är betydligt mindre än motsvarande [WOFF](/font/woff/) teckensnitt. Detta format stöds av de flesta moderna webbläsare inklusive Chrome, Firefox, Safari, Opera och Edge (version 14 och framåt).

## WOFF2 filformat - Mer information

Den interna filstrukturen för en WOFF2-teckensnittsfil består av flera olika delar, inklusive en rubrik, metadata, en tabellkatalog och själva teckensnittsdatan.

 1. Rubriken innehåller information om filens övergripande format, inklusive versionsnumret och antalet tabeller som finns i filen.

 1. Metadatasektionen innehåller information som typsnittsnamn, upphovsrätt och annan typsnittsrelaterad information.

 1. Tabellkatalogen innehåller information om de olika tabellerna som utgör typsnittet, inklusive deras plats i filen och deras längd.

 1. Själva teckensnittsdatan är uppdelad i flera olika tabeller, som var och en innehåller specifik information om typsnittet, såsom dess tecken och deras motsvarande glyfer. Dessa tabeller kan innehålla:

 * Tabellen glyf innehåller de faktiska teckensnittskonturerna, inklusive formen och storleken på varje tecken.
 * Tabellen huvud innehåller allmän information om typsnittet, såsom dess versionsnummer, designstorlek och så vidare.
 * Tabellen 'hmtx' innehåller information om teckensnittets mått, inklusive tecknens bredd och position.
 * Varje tabell komprimeras och lagras i WOFF2-filformat efter att den slutfört kodningsprocessen.

Strukturen överlag är utformad för att möjliggöra snabb analys och avkodning, så att webbläsare snabbt och effektivt kan ladda och visa teckensnittet på en webbplats.

### WOFF2 Header
WOFF-huvudet består av en identifierande signatur som indikerar typen av data som ingår i filen. WOFF-huvudet tillsammans med dess fält är som följer.

|Typ|Fältnamn|Beskrivning|
---|---|---|
|UInt32|signatur |0x774F4632 'wOF2' |
|UInt32| flavor |sfnt-versionen av inmatningsteckensnittet.|
|UInt32| length |Total storlek på WOFF-filen.|
|UInt16| numTables |Antal poster i katalogen över teckensnittstabeller.|
|UInt16| reserverad |Reserverad; inställd på noll.|
|UInt32| totalSfntSize |Total storlek som behövs för okomprimerade teckensnittsdata, inklusive sfnt-huvudet, katalogen och teckensnittstabellerna (inklusive utfyllnad).|
|UInt32| totalCompressedSize Total längd av det komprimerade datablocket.|
|UInt16| majorVersion |Större version av WOFF-filen.|
|UInt16| minorVersion |Mindre version av WOFF-filen.|
|UInt32| metaOffset |Offset till metadatablock, från början av WOFF-fil.|
|UInt32| metaLength |Längd på komprimerat metadatablock.|
|UInt32| metaOrigLength |Okomprimerad storlek på metadatablock.|
|UInt32| privOffset |Offset till privat datablock, från början av WOFF-fil.|
|UInt32| privLength |Längd på privat datablock.|


## Referenser
 * [w3 WOFF2 filformat](https://www.w3.org/TR/WOFF2/)

