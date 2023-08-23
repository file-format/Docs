{
  "date" : "2019-10-11",
  "keywords" :[ "odp-bestand", "odp-bestandsindeling", "wat is een odp-bestand", "bestand", "odp-voorbeeld", "odp-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice-presentatiebestandsindeling",
  "description":"Meer informatie over ODP-bestandsindeling en API's die ODP-bestanden kunnen maken en openen.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ODP-bestand?

Bestanden met de extensie .odp vertegenwoordigen de bestandsindeling voor presentaties die door OpenOffice.org in de OASISOpen-standaard wordt gebruikt. Een presentatiebestand is een verzameling dia's waarbij elke dia kan bestaan uit tekst, afbeeldingen, opmaak, animaties en andere media. Deze dia's worden aan het publiek gepresenteerd in de vorm van diavoorstellingen met aangepaste presentatie-instellingen. ODP-bestanden kunnen worden geopend door toepassingen die voldoen aan het OpenDocument-formaat (zoals OpenOffice of StarOffice).

## Korte geschiedenis

De specificaties van het ODP-bestandsformaat zijn gebaseerd op de standaard die is ontwikkeld als ODF-specificaties. Deze specificaties zijn in het verleden geëvolueerd in de vorm van drie versies die als volgt zijn ontwikkeld en gepubliceerd door OASIS:

`2005` - Versie 1.0 werd gepubliceerd in mei 2005
`2007` - Versie 1.1 is gepubliceerd in februari 2007
`2011` - Versie 1.2 is gepubliceerd in september 2011

Er waren vrij kleine veranderingen in de overgang van ODF 1.0 naar 1.1-versies. De [ODF 1.2-versie](https://www.oasis-open.org/standards#opendocumentv1.2) is de nieuwste versie voor ODF-specificaties en moet door ontwikkelaars worden geraadpleegd voor de ontwikkeling van toepassingen die verband houden met het lezen/schrijven van ODS.

## Specificaties bestandsindeling

OpenDocument-indeling ondersteunt documentweergave als een enkel XML-document, evenals een verzameling van verschillende subdocumenten binnen een pakket als [ZIP](https://docs.fileformat.com/compression/zip/)-archief. Elk van de bestanden uit het ZIP-archief slaat een deel van het volledige document op. Elk subdocument slaat een bepaald aspect van het document op. Een subdocument bevat bijvoorbeeld de stijlinformatie en een ander subdocument bevat de inhoud van het document. Een typisch ODF-document heeft de volgende onderdelen:

* `content.xml` – Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
* `styles.xml` – Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
* `meta.xml` – Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
* `settings.xml` – Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

Naast deze kunnen in een pakket veel andere subdocumenten zijn, zoals documentminiaturen, afbeeldingen, enz.

Spreadsheet-documentbestanden zijn de subset van ODF-bestanden waarin de inhoud (bladen) wordt opgeslagen in het subdocument content.xml.

## Referenties

* [OpenDocument - Door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

