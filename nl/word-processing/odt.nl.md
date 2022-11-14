{
  "date" : "2019-10-11",
  "keywords" :[ "odt-bestand", "odt-bestandsindeling", "wat is een odt-bestand", "bestand", "odt-voorbeeld", "odt-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - OpenDocument-tekstbestand",
  "description":"Meer informatie over ODT-bestandsindeling en API's die ODT-bestanden kunnen maken en openen.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ODT-bestand?

ODT-bestanden zijn typen documenten die zijn gemaakt met tekstverwerkingsprogramma's die zijn gebaseerd op de OpenDocument Text File-indeling. Deze zijn gemaakt met tekstverwerkingsprogramma's zoals gratis OpenOffice Writer en kunnen inhoud bevatten zoals tekst, afbeeldingen, objecten en stijlen. Het ODT-bestand is voor de tekstverwerker van Writer wat de [DOCX](/nl/tekstverwerking/docx/) is voor Microsoft Word. Verschillende toepassingen, waaronder Google Docs en de webgebaseerde tekstverwerker van Google die bij Google Drive worden geleverd, kunnen de ODT-bestanden openen voor bewerking. Microsoft Word kan ook ODT-bestanden openen en opslaan in andere formaten zoals [DOC](/nl/tekstverwerking/doc/) en DOCX.

## Korte geschiedenis ##

De specificaties van het ODP-bestandsformaat zijn gebaseerd op de standaard die is ontwikkeld als ODF-specificaties. Deze specificaties zijn in het verleden geëvolueerd in de vorm van drie versies die als volgt zijn ontwikkeld en gepubliceerd door OASIS:

**2005** Versie 1.0 werd gepubliceerd in mei 2005

**2007:** Versie 1.1 is gepubliceerd in februari 2007

**2011:** Versie 1.2 is gepubliceerd in september 2011

Er waren vrij kleine veranderingen in de overgang van ODF 1.0 naar 1.1-versies. De [ODF 1.2-versie](https://www.oasis-open.org/standards#opendocumentv1.2) is de nieuwste versie voor ODF-specificaties en moet door ontwikkelaars worden geraadpleegd voor de ontwikkeling van toepassingen die verband houden met het lezen/schrijven van ODS.

## Specificaties bestandsindeling ##

OpenDocument-indeling ondersteunt documentweergave als een enkel XML-document en als een verzameling van verschillende subdocumenten binnen een pakket als [ZIP](/nl/Compression/ZIP/)-archief. Elk van de bestanden uit het ZIP-archief slaat een deel van het volledige document op. Elk subdocument slaat een bepaald aspect van het document op. Een subdocument bevat bijvoorbeeld de stijlinformatie en een ander subdocument bevat de inhoud van het document. Een typisch ODF-document heeft de volgende onderdelen:

* content.xml – Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
* styles.xml – Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
* meta.xml – Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
* settings.xml – Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

Daarnaast kunnen in een pakket vele andere subdocumenten zijn, zoals documentminiaturen, afbeeldingen, enz. Documentbestanden zijn de subset van ODF-bestanden waar de inhoud (bladen) wordt opgeslagen in //content.xml// subdocument.

## Referenties ##

* [OpenDocument - Door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

