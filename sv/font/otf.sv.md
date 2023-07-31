{
  "date" : "2020-08-20",
  "keywords" :[ "otf-fil", "otf-filformat", "vad är en otf-fil", "fil", "otf-exempel", "otf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType Font File Format",
  "description":"Läs mer om OTF-filformat och API:er som kan skapa och öppna OTF-filer.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Vad är OTF fil?

En fil med filtillägget .otf hänvisar till OpenType-teckensnittsformat. OTF-teckensnittsformatet är mer skalbart och utökar de befintliga funktionerna i [TTF](/sv/font/ttf/)-format för digital typografi. OTF, som utvecklats av Microsoft och Adobe, kombinerar funktionerna i PostScript- och TrueType-teckensnittsformaten. Detta gör att OTF-formatet passar majoritetsskrivsystem och det är därför det används enhetligt på stora datorplattformar. Teckensnittsformatet OpenType stöds av Mac OS X och Windows 2000 och senare.

## Kortfattad bakgrund

Kravet på OpenType-teckensnitt uppstod som ett krav på ett mer uttrycksfullt teckensnittsformat som kunde hantera fin typografi. Dessutom syftade det till att möta kraven på komplext beteende hos många av världens skriftsystem. Microsoft försökte licensiera Apples avancerade typografiteknik, känd som GX Typography, i början av 1990-talet. Detta gick inte bra och som ett resultat började Microsoft förbättra sin egen TrueType-teckensnittsteknologi 1994. Ändringarna inkluderade också för att introducera ett mer lämpligt teckensnittsformat som även uppfyller funktionerna i Adobes typ 1 (PostScript) teckensnittsformat.

Adobe anslöt sig 1996 till Microsoft i dess ansträngningar att ersätta både Apples TrueType och dess egna typ 1-teckensnittsformat. Detta resulterade i en kombination av båda underliggande teckensnittsformaten för att övervinna begränsningarna och lägga till nya tillägg. Denna nya teknik introducerades samma år med namnet **OpenType**.

## OTF-filformatspecifikationer

OTF-specifikationer är tillgängliga för allmänheten av Microsoft och kan refereras till från utvecklarens perspektiv. Liksom TTF använder den samma 'sfnt'-behållarestruktur och är kompatibel med TrueType-specifikationerna. Data inuti en OpenType-teckensnittsfil används för olika ändamål som att beräkna textlayouten, definiera glyfer som TrueType eller Compact Font Format (CFF) konturer, tillhandahålla monokromatiska eller färgbitmappar eller SVG-dokument som alternativa glyfbeskrivningar och metadatainformation.

### OTF-datatyper
OTF-filer använder följande datatyper som alla finns i Big Endian.

|Datatyp| Beskrivning|
---|---|
|uint8| 8-bitars heltal utan tecken.|
|int8| 8-bitars signerat heltal.|
|uint16| 16-bitars heltal utan tecken.|
|int16| 16-bitars signerat heltal.|
|uint24| 24-bitars osignerat heltal.|
|uint32| 32-bitars heltal utan tecken.|
|int32| 32-bitars signerat heltal.|
|Fastad| 32-bitars signerat fastpunktsnummer (16.16)|
|FWORD| int16 som beskriver en kvantitet i teckensnittsdesignenheter.|
|UFWORD| uint16 som beskriver en kvantitet i teckensnittsdesignenheter.|
|F2DOT14| 16-bitars signerat fast nummer med de låga 14 bitarna av bråk (2.14).|
|LONGDATETIME| Datum och tid representerade i antal sekunder sedan 12:00 midnatt, 1 januari 1904, UTC. Värdet representeras som ett 64-bitars heltal med tecken.|
|Tagg| Array med fyra uint8s (längd = 32 bitar) som används för att identifiera en tabell, designvariationsaxel, skript, språksystem, funktion eller baslinje|
|Offset16| Kort offset till en tabell, samma som uint16, NULL offset = 0x0000|
|Offset32| Lång offset till en tabell, samma som uint32, NULL offset = 0x00000000|
|Version16Punkt16| Packat 32-bitars värde med större och mindre versionsnummer. (Se tabellversionsnummer.)|

### OTF-tabellkatalog

En OTF-fil börjar med en tabellkatalog. Den här katalogen är toppnivåsamlingen av tabellerna i teckensnittsfilen. Beroende på antalet teckensnitt i en fil kan tabellkatalogen finnas på olika platser i filen. Till exempel, om teckensnittsfilen bara har ett teckensnitt, börjar tabellkatalogen vid byte 0 i filen. Om du samlar flera OpenType-teckensnitt,
tabellkatalogens början indikeras i TTCHeader.

|Typ |Namn |Beskrivning|
---|---|---|
|uint32 |sfntVersion| 0x00010000 eller 0x4F54544F ('OTTO')|
|uint16| numTables |Antal tabeller.|
|uint16| searchRange |Maximal potens av 2 mindre än eller lika med numTables, gånger 16 ((2\**floor(log2(antalTables))) * 16, där "**" är en exponentieringsoperator).|
|uint16 |entrySelector Log2 av den maximala effekten av 2 mindre än eller lika med numTables (log2(searchRange/16), vilket är lika med floor(log2(antalTables))).|
|uint16 |rangeShift |antalTables gånger 16, minus searchRange ((antalTables * 16) - searchRange).|
|tabellRecord| tableRecords[antalTables] |Tabellpostarray—en för varje toppnivåtabell i typsnittet|


### Tabellpost

För varje toppnivåtabell i typsnittet finns det en tabellpost som består av följande fält.

|Skriv| Namn| Beskrivning|
---|---|---|
|Tagg| tableTag| Tabellidentifierare.|
|uint32| kontrollsumma| Kontrollsumma för denna tabell.|
|Offset32| offset| Offset från början av teckensnittsfil.|
|uint32| längd Längd på denna tabell.|

Varje tabell i OpenType-teckensnittsfilen representeras av namn som kallas tabelltaggar. Det är ett måste för alla poster i arrayen att sorteras i stigande ordning efter tagg.

## Referenser
* [OpenType Font Specifications by Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType-översikt](https://learn.microsoft.com/en-us/typography/truetype/)

