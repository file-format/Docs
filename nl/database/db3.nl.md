{
  "date" : "2019-12-12",
  "keywords" :[ "DB3", "DB3-bestandsindeling", "DB3-bestand", "SQLite", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden" ] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DB3-bestandsindelingen en API's die DB3-bestanden kunnen maken en openen.",
  "title" :"DB3-bestandsindeling",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Wat is een DB3-bestand?
Het DB3-bestand is een databasebestand gemaakt door de SQLite-software, een lichtgewicht, op zichzelf staand databaseprogramma dat databases maakt met gewone bestanden; bevat de database-anatomie en gegevensrecords; vaak gebruikt voor het ophalen of opslaan van gestructureerde gegevens met behulp van SQL. Deze bestanden kunnen worden gebruikt op slimme apparaten of waar het bijhouden van gegevens of ander gegevensbeheer vereist is, maar in een omgeving met weinig ruimte.


## DB3-bestandsindeling
Het DB3-bestandsformaat is gekoppeld aan RDBMS (Relational Database Management System) SQLite, een populaire keuze voor embedded databases. Er is geen specifieke bestandsextensie gedefinieerd in een SQLite_3 in de specificatie, het kan extensies gebruiken zoals [.dbf](/nl/database/dbf/) en [.sqlite](/nl/database/sqlite/).

### De database-secificatie
Gewoonlijk SQLite, versie 3 gerelateerde db-bestandsindeling kan worden beschouwd als de DB3-bestandsindeling die sinds juni 2004 wordt gebruikt als de openbaar gedocumenteerde native indeling voor de SQLite-database-engine. De DB3-bestandsindeling is een platformonafhankelijke, overdraagbare tussen big-endian en little-endian-architecturen of 32-bits en 64-bits systemen. Deze eigenschappen maken DB3 een populaire keuze als bestandsformaat voor toepassingen. Het hoofdbestand van de SQLite_3-database (DB3) bestaat uit een of meer pagina's. Alle formaten van alle pagina's zijn gelijk in dezelfde database. De paginagrootte in bytes is een macht van twee tussen 512 en 65536.



## Referenties ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite, versie 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)

