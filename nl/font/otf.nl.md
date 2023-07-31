{
  "date" : "2020-08-20",
  "keywords" :[ "otf-bestand", "otf-bestandsindeling", "wat is een otf-bestand", "bestand", "otf-voorbeeld", "otf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType-lettertypebestandsindeling",
  "description":"Meer informatie over OTF-bestandsindelingen en API's die OTF-bestanden kunnen maken en openen.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Wat is een OTF-bestand?

Een bestand met de extensie .otf verwijst naar het OpenType-lettertypeformaat. OTF-lettertypeindeling is beter schaalbaar en breidt de bestaande functies van [TTF](/nl/font/ttf/)-indelingen voor digitale typografie uit. OTF is ontwikkeld door Microsoft en Adobe en combineert de functies van PostScript- en TrueType-lettertypen. Dit maakt het OTF-formaat geschikt voor meerderheidsschrijfsystemen en daarom wordt het uniform gebruikt op grote computerplatforms. De lettertype-indeling OpenType wordt ondersteund door Mac OS X en Windows 2000 en later.

## Korte geschiedenis

De eis van OpenType-lettertypen is ontstaan als een vereiste voor een expressiever lettertype-formaat dat fijne typografie aankan. Bovendien was het bedoeld om te voldoen aan de eisen van complex gedrag van veel van 's werelds schrijfsystemen. Microsoft probeerde begin jaren negentig een licentie te verkrijgen voor de geavanceerde typografietechnologie van Apple, bekend als GX Typography. Dit ging niet goed en als gevolg daarvan begon Microsoft in 1994 met het verbeteren van zijn eigen TrueType-lettertypetechnologie. De wijzigingen omvatten ook de introductie van een geschikter lettertypeformaat dat ook voldoet aan de kenmerken van Adobe's Type 1 (PostScript) lettertypeformaten.

Adobe, in 1996, sloot zich aan bij Microsoft in zijn pogingen om zowel Apple's TrueType als zijn eigen Type 1-lettertypeformaten te vervangen. Dit resulteerde in een combinatie van beide onderliggende lettertypeformaten om de beperkingen te overwinnen en nieuwe extensies toe te voegen. Deze nieuwe technologie werd in hetzelfde jaar geïntroduceerd onder de naam **OpenType**.

## Specificaties OTF-bestandsindeling

OTF-specificaties zijn openbaar beschikbaar door Microsoft en kunnen worden geraadpleegd vanuit het perspectief van de ontwikkelaar. Net als TTF gebruikt het dezelfde 'sfnt'-containerstructuur en is het compatibel met de TrueType-specificaties. Gegevens in een OpenType-lettertypebestand worden voor verschillende doeleinden gebruikt, zoals het berekenen van de tekstlay-out, het definiëren van glyphs als TrueType- of Compact Font Format (CFF)-contouren, het leveren van monochromatische of kleurenbitmaps of SVG-documenten als alternatieve glyph-beschrijvingen en metagegevensinformatie.

### OTF-gegevenstypen
OTF-bestanden gebruiken de volgende gegevenstypen die allemaal in Big Endian staan.

|Gegevenstype| Beschrijving|
---|---|
|uint8| 8-bits geheel getal zonder teken.|
|int8| 8-bits geheel getal met teken.|
|uint16| 16-bits geheel getal zonder teken.|
|int16| 16-bits geheel getal met teken.|
|uint24| 24-bit geheel getal zonder teken.|
|uint32| 32-bits geheel getal zonder teken.|
|int32| 32-bits geheel getal met teken.|
|Vast| 32-bits getekende vaste-kommagetal (16.16)|
|FWORD| int16 die een hoeveelheid beschrijft in lettertype-ontwerpeenheden.|
|UFWORD| uint16 die een hoeveelheid beschrijft in lettertype-ontwerpeenheden.|
|F2DOT14| 16-bits vast getal met teken met de lage 14 bits breuk (2.14).|
|LANGDATUM| Datum en tijd weergegeven in aantal seconden sinds 12.00 uur middernacht, 1 januari 1904, UTC. De waarde wordt weergegeven als een 64-bits geheel getal met teken.|
|Tag| Array van vier uint8's (lengte = 32 bits) die worden gebruikt om een tabel, ontwerpvariatie-as, script, taalsysteem, kenmerk of baseline te identificeren |
|Offset16| Korte offset naar een tabel, hetzelfde als uint16, NULL offset = 0x0000|
|Offset32| Lange offset naar een tabel, hetzelfde als uint32, NULL offset = 0x00000000|
|Versie16Dot16| Verpakte 32-bits waarde met grote en kleine versienummers. (Zie Tabel Versienummers.)|

### OTF Tabellen Directory

Een OTF-bestand begint met een tabeldirectory. Deze map is de verzameling op het hoogste niveau van de tabellen in het lettertypebestand. Afhankelijk van het aantal lettertypen in een bestand, kan de tabeldirectory zich op een andere locatie in het bestand bevinden. Als het lettertypebestand bijvoorbeeld slechts één lettertype heeft, begint de tabeldirectory bij byte 0 van het bestand. In het geval van meerdere verzamelingen van OpenType-lettertypen,
het begin van de tabeldirectory wordt aangegeven in de TTCHeader.

|Type |Naam |Beschrijving|
---|---|---|
|uint32 |sfntVersie| 0x00010000 of 0x4F54544F ('OTTO')|
|uint16| numTables |Aantal tabellen.|
|uint16| searchRange |Maximale macht van 2 kleiner dan of gelijk aan numTables, maal 16 ((2\**floor(log2(numTables))) * 16, waarbij "**" een exponentiatie-operator is).|
|uint16 |entrySelector Log2 van het maximale vermogen van 2 kleiner dan of gelijk aan numTables (log2(searchRange/16), wat gelijk is aan floor(log2(numTables))).|
|uint16 |rangeShift |numTables maal 16, minus searchRange ((numTables * 16) - searchRange).|
|tabelRecord| tableRecords[numTables] |Table records array—één voor elke tabel op het hoogste niveau in het lettertype|


### Tafelrecord

Voor elke tabel op het hoogste niveau in het lettertype is er een tabelrecord die uit de volgende velden bestaat.

|Type| Naam| Beschrijving|
---|---|---|
|Tag| tableTag| Tabel-ID.|
|uint32| controlesom| Controlesom voor deze tabel.|
|Offset32| compenseren| Offset vanaf het begin van het lettertypebestand.|
|uint32| lengte Lengte van deze tafel.|

Elke tabel in het OpenType-lettertypebestand wordt weergegeven door namen die bekend staan als tabeltags. Het is een must dat alle records in de array in oplopende volgorde op tag worden gesorteerd.

## Referenties
* [OpenType-lettertypespecificaties door Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType-overzicht](https://learn.microsoft.com/en-us/typography/truetype/)

