{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over ACCDT-bestandsindelingen en API's die ACCDT-bestanden kunnen maken en openen.",
  "title" :"ACCDT - Microsoft Access 2007-sjabloondatabasebestandsindeling",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Wat is een ACCDT-bestand?

Een bestand met de extensie .accdt is een Microsoft Access-databasesjabloonbestand dat vooraf gedefinieerde database-elementen bevat. Deze elementen zijn een verzameling structuren die databasetoepassingen definiëren, zoals databaseschema's voor het opslaan van gegevens, lay-outbeschrijvingen voor weergaven van de gegevens en metagegevens die de database beschrijven. Omdat het sjabloonbestanden zijn, kunnen ACCDT-bestanden worden gebruikt om databases te maken op basis van de sjablooninstellingen die hierin beschikbaar zijn. Resulterende databasebestanden worden opgeslagen als [ACCDB](/nl/database/accdb/)-bestanden en gevuld met gegevens in tabellen. Microsoft Access 2007 en later kunnen ACCDT-bestanden openen.

## ACCDT-bestandsindeling

ACCDT-sjabloonbestanden zijn gebaseerd op de Office Open XML-specificaties en alle gegevens bevinden zich in het ZIP-pakket. Structuur- en inhoudsinformatie van de database is opgenomen in de [XML](/nl/web/xml/) bestanden en tekstbestanden en via relaties aan elkaar gekoppeld. U kunt een ACCDT-bestand hernoemen naar de extensie [.zip](/nl/compression/zip/) en compressiesoftware gebruiken om de inhoud van het ZIP-archief uit te pakken.

### Bestandsstructuur

ACCDT-bestanden zijn pakketten die een verzameling gerelateerde onderdelen bevatten. Elk **deel** slaat informatie op over de inhoud van een databasetoepassing met behulp van XML, tekst en binaire formaten, waaronder:

* Database-objecten
* Bijbehorende metadata
* Structuur van het pakket

#### Pakket

Een pakket is een [ZIP](/nl/compression/zip/)-archief dat meerdere delen bevat en voldoet aan de Open Packaging Conventions gespecificeerd in [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). ACCDT-bestanden moeten ten minste één sjabloon-metadaa-gedeelte bevatten dat het doel van een relatie zou moeten zijn. Deze sjabloonmetadata is het startgedeelte van een ACCDT-bestand.

#### Een deel

Een deel is een stroom van bytes die een bijbehorend type heeft voor het specificeren van de aard en het type inhoud dat erin is opgeslagen. Onderdelenopsomming specificeert geldige onderdelen, geldige inhoudstypen en vereiste relaties tussen alle onderdelen in een pakket.

#### Relatie

`Pakketrelatie` - waarbij doel een onderdeel is en de bron het pakket als geheel.

`Part-to-Part-relatie` - waarbij het doel een onderdeel is en de bron een onderdeel van het pakket.

`Expliciete relatie` - waarbij naar een bron wordt verwezen vanuit de inhoud van een brongedeelte door te verwijzen naar een relatie-element met de waarde van het ID-kenmerk.

'Impliciete relatie' - een relatie die niet expliciet is.

'Interne relatie' - waarbij het doelwit een onderdeel is van het pakket.

'Externe relatie' - waarbij het doel een externe bron is die niet in het pakket zit.

## Referenties ##

* [Access Template File Format](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

