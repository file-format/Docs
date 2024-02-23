{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2-bestand - Web Open Font Format 2.0-bestand",
  "description": "Lees meer over wat een WOFF2-bestand is en welke API's een WOFF2-bestand kunnen maken en openen.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-nl2"
}
},
  "lastmod": "2023-01-10"
}

## Wat is een WOFF2-bestand?

WOFF2 is een lettertypebestandsindeling die een meer gecomprimeerde versie is van de Web Open Font Format (WOFF). Het is ontwikkeld als een manier om de bestandsgrootte van weblettertypen te verkleinen, waardoor ze sneller kunnen laden en minder bandbreedte gebruiken. WOFF2 gebruikt een compressie-algoritme genaamd Brotli om de lettertypegegevens te comprimeren, wat kan resulteren in bestandsgroottes die aanzienlijk kleiner zijn dan equivalente [WOFF](/font/woff/) lettertypen. Dit formaat wordt ondersteund door de meeste moderne webbrowsers, waaronder Chrome, Firefox, Safari, Opera en Edge (versie 14 en hoger).

## WOFF2-bestandsindeling - Meer informatie

De interne bestandsstructuur van een WOFF2-lettertypebestand bestaat uit verschillende delen, waaronder een header, metagegevens, een tabelmap en de lettertypegegevens zelf.

 1. De header bevat informatie over het algehele formaat van het bestand, inclusief het versienummer en het aantal tabellen dat in het bestand aanwezig is.

 1. Het gedeelte Metagegevens bevat informatie zoals de naam van het lettertype, copyright en andere lettertypegerelateerde informatie.

 1. De tabelmap bevat informatie over de verschillende tabellen waaruit het lettertype bestaat, inclusief hun locatie in het bestand en hun lengte.

 1. De lettertypegegevens zelf zijn onderverdeeld in verschillende tabellen, die elk specifieke informatie over het lettertype bevatten, zoals de tekens en de bijbehorende tekens. Deze tabellen kunnen het volgende omvatten:

 * De 'glyf'-tabel bevat de daadwerkelijke lettertypecontouren, inclusief de vorm en grootte van elk teken.
 * De 'head'-tabel bevat algemene informatie over het lettertype, zoals het versienummer, de ontwerpgrootte, enzovoort.
 * De 'hmtx'-tabel bevat informatie over de statistieken van het lettertype, inclusief de breedte en positie van de tekens.
 * Elke tabel wordt gecomprimeerd en opgeslagen in WOFF2-bestandsindeling nadat het coderingsproces is voltooid.

De algehele structuur is ontworpen om snelle parsering en decodering mogelijk te maken, zodat webbrowsers het lettertype snel en efficiënt op een website kunnen laden en weergeven.

### WOFF2-kopbal
De WOFF-header bestaat uit een identificerende handtekening die aangeeft welk soort gegevens in het bestand zijn opgenomen. De WOFF-header en zijn velden zijn als volgt.

|Type|Veldnaam|Beschrijving|
---|---|---|
|UInt32|handtekening |0x774F4632 'wOF2' |
|UInt32| smaak |De sfnt-versie van het invoerlettertype.|
|UInt32| lengte |Totale grootte van het WOFF-bestand.|
|UInt16| numTables |Aantal vermeldingen in de directory met lettertypetabellen.|
|UInt16| gereserveerd |Gereserveerd; op nul gezet.|
|UInt32| totalSfntSize |Totale grootte die nodig is voor de niet-gecomprimeerde lettertypegegevens, inclusief de sfnt-header, map en lettertypetabellen (inclusief opvulling).|
|UInt32| totalComPRESSSize Totale lengte van het gecomprimeerde gegevensblok.|
|UInt16| majorVersion |Belangrijke versie van het WOFF-bestand.|
|UInt16| minorVersion |Kleine versie van het WOFF-bestand.|
|UInt32| metaOffset |Offset naar metadatablok, vanaf het begin van het WOFF-bestand.|
|UInt32| metaLength |Lengte van gecomprimeerd metadatablok.|
|UInt32| metaOrigLength |Ongecomprimeerde grootte van metadatablok.|
|UInt32| privOffset |Offset naar privégegevensblok, vanaf het begin van het WOFF-bestand.|
|UInt32| privLength |Lengte van privégegevensblok.|


## Referenties
 * [w3 WOFF2-bestandsindeling](https://www.w3.org/TR/WOFF2/)

