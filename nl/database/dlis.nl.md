{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Leer meer over de DLIS-bestandsindeling en API's waarmee DLIS-bestanden kunnen worden gemaakt en geopend.",
  "title" : "DLIS-bestandsindeling - Wellloggegevensbestand",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-nl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Wat is een DLIS-bestand?

Het .dlis-bestandsformaat is een standaard bestandsformaat voor de opslag en uitwisseling van boorputgegevens in de olie- en gasindustrie. Het formaat is ontwikkeld door de commissie Logging Industry Data Standard (LIDS) en staat voor 'Digital Log Information Standard'. Het formaat is ontworpen om putloggegevens op te slaan op een manier die gemakkelijk te lezen, schrijven en uit te wisselen is tussen verschillende systemen.

DLIS-bestanden bevatten een reeks logische records die de putloggegevens en de kenmerken ervan beschrijven, zoals het type loggegevens (bijvoorbeeld soortelijke weerstand, gammastraling), de meeteenheden en de locatie van de gegevens in de put. De daadwerkelijke loggegevens worden opgeslagen in afzonderlijke binaire bestanden en er wordt naar verwezen door de logische records in het DLIS-bestand.

## Korte informatie over putloggegevens

Putloggegevens zijn een registratie van metingen die op verschillende diepten in een put zijn uitgevoerd, meestal tijdens het boorproces of nadat de put is geboord. Deze metingen kunnen verschillende fysische, chemische en/of geofysische eigenschappen van het gesteente en de vloeistoffen in de put omvatten. Enkele voorbeelden van putloggegevens zijn:

- Elektrische weerstand: een maatstaf voor het vermogen van gesteente om weerstand te bieden aan de stroom van elektrische stroom
- Gammastraling: een maatstaf voor de natuurlijke radioactiviteit van het gesteente
- Porositeit: een maatstaf voor de hoeveelheid open ruimtes of poriën in het gesteente
- Sonisch: een maatstaf voor de tijd die een geluidsgolf nodig heeft om door de rots te reizen
- Dichtheid: een maat voor de massa van een gesteente per volume-eenheid
- Lithologie: een maat voor het gesteentetype of de formatie

Putloggegevens worden voor verschillende doeleinden in de olie- en gasindustrie gebruikt, zoals:

- Identificatie van de locatie en kwaliteit van koolwaterstofhoudende formaties
- Het evalueren van het productiepotentieel van een put
- Plannen en bewaken van de voltooiing en stimulering van een put
- Het monitoren van het putgedrag in de loop van de tijd

## Relatie met PPDM

PPDM (Professional Petroleum Data Management) is een standaard voor gegevensbeheer in de olie- en gasindustrie die een gemeenschappelijk gegevensmodel biedt voor het beheer van put- en productiegegevens. Het PPDM-gegevensmodel definieert een set standaardgegevensobjecten en relaties die kunnen worden gebruikt voor het organiseren en beheren van putloggegevens, inclusief DLIS-gegevens.

Het PPDM-gegevensmodel omvat gegevensobjecten voor put- en productiegegevens, zoals putten, putkoppen, putlogboeken en productiegegevens. Het omvat ook relaties tussen deze dataobjecten, zoals de relatie tussen een put en de bijbehorende putlogboeken.

Het PPDM-datamodel biedt een consistente, industriestandaard manier om putloggegevens, inclusief DLIS-gegevens, te organiseren en beheren. Het stelt verschillende organisaties in staat gegevens te delen en uit te wisselen met behulp van een gemeenschappelijk datamodel, waardoor de data-interoperabiliteit wordt verbeterd en de kosten voor data-integratie worden verlaagd.

Door het PPDM-datamodel en DLIS-data samen te gebruiken, is het mogelijk om putloggegevens op te slaan en te beheren op een manier die consistent is met industriestandaarden en gemakkelijk toegankelijk is voor andere systemen en applicaties.


