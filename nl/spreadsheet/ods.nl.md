{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "bestand", "extensie", "bestandsindeling", "OpenDocument Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een ODS-bestand is en API's die ze kunnen maken en openen.",
  "title" :"Wat is een ODS-bestand?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een ODS-bestand?

Bestanden met de extensie .ods staan voor OpenDocument Spreadsheet Document-indeling die door de gebruiker kan worden bewerkt. Gegevens worden in het ODF-bestand opgeslagen in rijen en kolommen. Het is een op XML gebaseerd formaat en is een van de verschillende subtypes in de Open Document Formats (ODF)-familie. Het formaat wordt gespecificeerd als onderdeel van de ODF 1.2-specificaties die zijn gepubliceerd en onderhouden door OASIS. Een aantal toepassingen op Windows en andere besturingssystemen kunnen ODS-bestanden openen voor bewerking en manipulatie, waaronder Microsoft Excel, NeoOffice en LibreOffice. ODS-bestanden kunnen ook worden geconverteerd naar andere spreadsheetformaten, zoals [XLS](/nl/spreadsheet/xls/), [XLSX](/nl/spreadsheet/xlsx/) en andere door verschillende toepassingen.

## Korte geschiedenis ##

De specificaties van het ODS-bestandsformaat zijn gebaseerd op de standaard die is ontwikkeld als ODF-specificaties. Deze specificaties zijn in het verleden geëvolueerd in de vorm van drie versies die als volgt zijn ontwikkeld en gepubliceerd door OASIS:

`2005`- Versie 1.0 werd gepubliceerd in mei 2005

`2007` - Versie 1.1 is gepubliceerd in februari 2007

`2011` - Versie 1.2 is gepubliceerd in september 2011

Er waren vrij kleine veranderingen in de overgang van ODF 1.0 naar 1.1-versies. De [ODF 1.2-versie](https://www.oasis-open.org/standards#opendocumentv1.2) is de nieuwste versie voor ODF-specificaties en moet door ontwikkelaars worden geraadpleegd voor de ontwikkeling van toepassingen die verband houden met het lezen/schrijven van ODS.

## ODS-bestandsindeling ##

OpenDocument-indeling ondersteunt documentweergave als een enkel XML-document en als een verzameling van verschillende subdocumenten binnen een pakket als [ZIP](/nl/compression/zip/)-archief. Elk van de bestanden uit het ZIP-archief slaat een deel van het volledige document op. Elk subdocument slaat een bepaald aspect van het document op. Een subdocument bevat bijvoorbeeld de stijlinformatie en een ander subdocument bevat de inhoud van het document. Een typisch ODF-document heeft de volgende onderdelen:

* `content.xml` – Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
* `styles.xml` – Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
* `meta.xml` – Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
* `settings.xml` – Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

Naast deze kunnen in een pakket veel andere subdocumenten zijn, zoals documentminiaturen, afbeeldingen, enz.

Spreadsheet-documentbestanden zijn de subset van ODF-bestanden waarin de inhoud (bladen) wordt opgeslagen in het subdocument content.xml.

## Referenties ##

* [OpenDocument - Door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

