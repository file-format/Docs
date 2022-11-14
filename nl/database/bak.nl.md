{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "extensie", "bestand", "bestandsindeling", "BAK-bestandstype", "BAK-bestandsextensie", "Databasebestandstype", "Databasebestandsformaat", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over BAK-bestandsindeling en API's die BAK-bestanden kunnen maken en openen.",
  "title" :"BAK-bestandsindeling - databaseback-upbestand",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Wat is een BAK-bestand?

Een bestand met de extensie .bak is meestal een back-upbestand dat door verschillende softwaretools wordt gebruikt om back-ups van gegevens op te slaan. Vanuit databaseperspectief wordt een BAK-bestand door Microsoft SQL Server gebruikt voor het opslaan van de inhoud van een database. Alle gegevens en bestanden die aan de database zijn gekoppeld, worden in dit bestandsformaat opgeslagen om te worden opgehaald in het geval dat de database om welke reden dan ook corrupt of ongeldig wordt. De back-upbestanden kunnen om veiligheidsredenen worden opgeslagen en geïndexeerd op andere servers. Verschillende toepassingen kunnen BAK-bestanden maken, zoals SQL Server Management Studio, Transact-SQL en Windows PowerShell.

## BAK-bestandsindeling

De interne details van een BAK-bestand zijn niet bekend, maar algemeen wordt aangenomen dat het is gebaseerd op het Microsoft Tape Format (MTF). MTF-specificaties zijn beschikbaar en er kan naar worden verwezen om de structuur van het bestand te begrijpen. Het document biedt details over MTF-opslag voor iedereen die algemene kennis heeft van opslagbeheerbewerkingen, tapedrives en bestandssystemen.

### Gegevenssets

Een dataset is een verzameling objecten die tijdens het back-uppen of herstellen van gegevens naar een opslagmedium (tape, optische schijf, enz.) zijn geschreven. Datasets bestaan uit meerdere media bij grote hoeveelheden data.

### Fundamentele elementen van MTF

Een MTF-bestand bestaat uit enkele fundamentele elementen die de bouwstenen vormen. Deze elementen zijn:

#### Descriptorblokken

Descriptorblokken (DBLK) worden gebruikt voor formaatcontrole en vormen de primaire basis van een MTF-bestand. Een enkel MTF-bestand definieert meerdere DBLK's voor elke unieke rol. Elke DBLK is een gegevensblok met variabele lengte dat is onderverdeeld in de volgende vier delen:

* `Common Block Header` - Structuur met vaste lengte die voor alle DBLK's geldt. Dit is de enige Block Header die vereist is.
* `DBLK Type Information` - Blok met vaste lengte specifiek voor het type DBLK dat wordt gedefinieerd
* `Besturingssysteemgegevens` - Specifieke gegevens die zijn gedefinieerd op basis van het type DBLK en besturingssystemen
* `DBLK-informatie' - DBLK-specifieke informatie met variabele lengte die niet kan worden opgeslagen met de DBLK-informatie met vaste lengte.

 {{< figure src="../bak.png" alt="Microsoft SQL-back-upbestandsindeling" >}}

#### Data stroom

Gegevensstromen in een MTF-bestand worden gebruikt voor gegevensinkapseling en uitlijning. Het bestaat uit een Stream Header, gevolgd door de Stream Data. Een streamheader kan slechts één type streamgegevens inkapselen.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL-back-upbestandsindeling" >}}

#### Bestandsmarkeringen

Een bestandsmarkering wordt gebruikt voor logische scheiding en snelle toegang binnen een medium. Bestandsmarkeringen worden geëmuleerd door het apparaatstuurprogramma of door gebruik te maken van het Soft Filemark Descriptor-blok in het geval dat het gebruikte apparaat geen bestandsmarkeringen biedt.

## Referenties ##

* [[MS-BCP]: bulkkopie-indeling](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

