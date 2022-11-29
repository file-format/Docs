{
  "date" : "2020-08-20",
  "keywords" :[ "woff fil", "woff filformat", "vad är en woff fil", "fil", "woff exempel", "woff filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open File Format",
  "description":"En WOFF-fil är ett öppet teckensnitt skapat i Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Vad är WOFF fil?

En fil med filtillägget .woff är en webbteckensnittsfil baserad på Web Open Font Format (WOFF). Den har formatspecifika komprimerade behållare baserade på antingen TrueType (.TTF) eller OpenType (.OTT) teckensnittstyper. WOFF introducerades med syftet att skilja webbteckensnitt från teckensnittsfiler som används i skrivbordsapplikationer. Dessutom har formatet som mål att minska fördröjningen av teckensnittsöverföring från server till klientdator över nätverket. Flera verktyg finns tillgängliga som kan konvertera WOFF-filer till TTF och andra typsnittsfilformat.

## **WOFF filformat**

WOFF-teckensnittsformat komprimerar teckensnittsdatatabeller för tabellbaserade sfnt-strukturer som används i olika teckensnittstyper som TrueType, OpenType och Open Font Format. Det är som en behållare för dessa teckensnittstyper och har även utrymme att inkludera teckensnittets metadata och privat användningsdata som ska inkluderas i behållaren. Konverterare använder sfnt-filerna till en WOFF-formaterad fil och användaragenter återställer den kodade filen för användning med webbdokumentet. Det bör noteras att de återställda teckensnittsdata exakt matchar det inmatade teckensnittsformatet ur alla aspekter.

WOFF-filverktyg innehåller ofta ytterligare funktioner som glyfunderinställningar, validering eller tillägg av teckensnittsfunktioner, men det är inte nödvändigt. Både skaparen och användaragenten måste se till att giltigheten hos de underliggande teckensnittsdata bevaras.

### WOFF-filstruktur

WOFF-filstrukturen liknar den för sfnt-teckensnitt. Den är baserad på en tabellkatalog som innehåller längder och förskjutningar till varje teckensnittsdatatabell. Alla tabeller följs efter denna första information. Filen innehåller teckensnittsdatabas som är desamma som i de ursprungliga typsnitten. Ordningen på tabellerna är också densamma men alla kan vara komprimerade. WOFF-tabellkatalogen ersätter dock den ursprungliga tabellkatalogen.

En WOFF-fil består av följande:

* WOFFHeader - Filhuvud med grundläggande teckensnittstyp och version, tillsammans med förskjutningar till metadata och privata datablock.
* TableDirectory - Katalog över teckensnittstabeller, som anger originalstorlek, komprimerad storlek och plats för varje tabell i WOFF-filen.
* FontTables - Teckensnittsdatatabellerna från indata sfnt-teckensnittet, komprimerade för att minska bandbreddskraven.
* ExtendedMetadata - Ett valfritt block av utökad metadata, representerad i XML-format och komprimerad för lagring i WOFF-filen.
* PrivateData- Ett valfritt block med privata data för teckensnittsdesignern, gjuteriet eller säljaren att använda.

### WOFF Header
WOFF-huvudet består av en identifierande signatur som indikerar typen av data som ingår i filen. WOFF-huvudet tillsammans med dess fält är som följer.

|Typ|Fältnamn|Beskrivning|
---|---|---|
|UInt32|signatur |0x774F4646 'wOFF' |
|UInt32| flavor |"sfnt-versionen" av inmatningsteckensnittet.|
|UInt32| length |Total storlek på WOFF-filen.|
|UInt16| numTables |Antal poster i katalogen över teckensnittstabeller.|
|UInt16| reserverad |Reserverad; inställd på noll.|
|UInt32| totalSfntSize |Total storlek som behövs för okomprimerade teckensnittsdata, inklusive sfnt-huvudet, katalogen och teckensnittstabellerna (inklusive utfyllnad).|
|UInt16| majorVersion |Större version av WOFF-filen.|
|UInt16| minorVersion |Mindre version av WOFF-filen.|
|UInt32| metaOffset |Offset till metadatablock, från början av WOFF-fil.|
|UInt32| metaLength |Längd på komprimerat metadatablock.|
|UInt32| metaOrigLength |Okomprimerad storlek på metadatablock.|
|UInt32| privOffset |Offset till privat datablock, från början av WOFF-fil.|
|UInt32| privLength |Längd på privat datablock.|


## **Referenser**
* [w3 WOFF-filformat](https://www.w3.org/TR/WOFF/)

