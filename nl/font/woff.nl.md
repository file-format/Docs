{
  "date" : "2020-08-20",
  "keywords" :[ "woff-bestand", "woff-bestandsformaat", "wat is een woff-bestand", "bestand", "woff-voorbeeld", "woff-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open Bestandsformaat",
  "description":"Een WOFF-bestand is een open lettertype-indeling die is gemaakt in de Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Wat is een WOFF-bestand?

Een bestand met de extensie .woff is een weblettertypebestand gebaseerd op de Web Open Font Format (WOFF). Het heeft een formaatspecifieke gecomprimeerde container op basis van TrueType (.TTF) of OpenType (.OTT) lettertypen. WOFF is geïntroduceerd met het doel om weblettertypen te onderscheiden van lettertypebestanden die in desktoptoepassingen worden gebruikt. Bovendien is de indeling bedoeld om de latentie van lettertypen te verminderen die via het netwerk van de server naar de computer van de klant worden overgebracht. Er zijn verschillende tools beschikbaar die WOFF-bestanden kunnen converteren naar TTF en andere bestandsindelingen voor lettertypen.

## **WOFF-bestandsindeling**

WOFF-lettertypeformaat comprimeert lettertypegegevenstabellen van op tabellen gebaseerde sfnt-structuren die worden gebruikt in verschillende lettertypen, zoals TrueType, OpenType en Open Font Format. Het is als een container voor deze lettertypen en heeft ook de ruimte om de metadata van het lettertype en privé-gebruiksgegevens op te nemen in de container. Converters gebruiken de sfnt-bestanden in een WOFF-geformatteerd bestand en user agents herstellen het gecodeerde bestand voor gebruik met het webdocument. Opgemerkt moet worden dat de herstelde lettertypegegevens in alle opzichten exact overeenkomen met het invoerlettertypeformaat.

WOFF-bestand Hulpprogramma's bevatten vaak extra functies, zoals glyph-subsetting, validatie of toevoegingen van lettertypen, maar dat is niet nodig. Zowel de maker als de gebruikersagent moeten ervoor zorgen dat de geldigheid van de onderliggende lettertypegegevens behouden blijft.

### WOFF-bestandsstructuur

De WOFF-bestandsstructuur is vergelijkbaar met die van sfnt-lettertypen. Het is gebaseerd op een tabeldirectory die de lengtes en offsets van elke fontgegevenstabellen bevat. Alle tabellen worden gevolgd na deze eerste informatie. Het bestand bevat lettertypedatabases die hetzelfde zijn als in de originele lettertypen. De volgorde van de tabellen is ook hetzelfde, maar elk kan worden gecomprimeerd. WOFF-tabeldirectory vervangt echter de oorspronkelijke tabeldirectory.

Een WOFF-bestand bestaat uit het volgende:

* WOFFHeader - Bestandskop met basislettertype en -versie, samen met verschuivingen naar metadata en privégegevensblokken.
* TableDirectory - Directory met lettertypetabellen, die de oorspronkelijke grootte, gecomprimeerde grootte en locatie van elke tabel in het WOFF-bestand aangeeft.
* FontTables - De lettertypegegevenstabellen van het invoer-sfnt-lettertype, gecomprimeerd om de bandbreedtevereisten te verminderen.
* ExtendedMetadata - Een optioneel blok uitgebreide metadata, weergegeven in XML-formaat en gecomprimeerd voor opslag in het WOFF-bestand.
* PrivateData- Een optioneel blok met privégegevens dat de fontontwerper, gieterij of leverancier kan gebruiken.

### WOFF-koptekst
De WOFF-header bestaat uit een identificerende handtekening die het soort gegevens in het bestand aangeeft. De WOFF-header samen met de velden is als volgt.

|Type|Veldnaam|Beschrijving|
---|---|---|
|UInt32|handtekening |0x774F4646 'wOFF' |
|UInt32| flavour |De "sfnt-versie" van het invoerlettertype.|
|UInt32| lengte |Totale grootte van het WOFF-bestand.|
|UInt16| numTables |Aantal vermeldingen in directory van lettertypetabellen.|
|UInt16| gereserveerd |Gereserveerd; ingesteld op nul.|
|UInt32| totalSfntSize |Totale grootte die nodig is voor de niet-gecomprimeerde lettertypegegevens, inclusief de sfnt-koptekst, directory en lettertypetabellen (inclusief opvulling).|
|UInt16| majorVersion |Hoofdversie van het WOFF-bestand.|
|UInt16| minorVersion |Minor-versie van het WOFF-bestand.|
|UInt32| metaOffset |Offset naar metadatablok, vanaf het begin van het WOFF-bestand.|
|UInt32| metaLength |Lengte van gecomprimeerd metadatablok.|
|UInt32| metaOrigLength |Ongecomprimeerde grootte van metadatablok.|
|UInt32| privOffset |Verschuiving naar privégegevensblok, vanaf het begin van het WOFF-bestand.|
|UInt32| privLength |Lengte van privégegevensblok.|


## **Referenties**
* [w3 WOFF-bestandsindeling](https://www.w3.org/TR/WOFF/)

