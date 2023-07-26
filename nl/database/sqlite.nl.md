{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over SQLITE-bestandsindeling en API's die SQLITE-bestanden kunnen maken en openen.",
  "title" :"SQLite-bestandsindeling",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Wat is een SQLite-bestand?

Een bestand met de extensie .sqlite is een lichtgewicht SQL-databasebestand dat is gemaakt met de software [SQLite](https://www.sqlite.org/index.html). Het is een database in een bestand zelf en implementeert een op zichzelf staande, complete, zeer betrouwbare [SQL](/nl/database/sql/) database-engine. SQLite-databasebestanden kunnen worden gebruikt om rijke inhoud tussen systemen te delen door deze bestanden eenvoudig via het netwerk uit te wisselen. Bijna alle mobiele telefoons en computers gebruiken SQLite voor het opslaan en delen van gegevens, en is de keuze van het bestandsformaat voor platformonafhankelijke toepassingen. Vanwege het compacte gebruik en de eenvoudige bruikbaarheid, wordt het gebundeld in andere toepassingen geleverd. SQLite-bindingen bestaan voor programmeertalen zoals C, [C#](/nl/programming/cs/), [C++](/nl/programming/cpp/), [Java](/nl/programming/java/), [PHP](/nl/programming/php/), en vele anderen.

## SQLite-bestandsindeling

SQLite is in werkelijkheid een C-Language-bibliotheek die het SQLite RDBMS implementeert met behulp van het SQLite-bestandsformaat. Met de evolutie van nieuwe apparaten elke dag, is het bestandsformaat achterwaarts compatibel gehouden om oudere apparaten te accommoderen. Het SQLite-bestandsformaat wordt gezien als een archiefformaat voor de lange termijn voor de gegevens.

### Het databasebestand

Een SQLite-database wordt volledig onderhouden via twee bestanden.
* Hoofddatabasebestand - Bevat de volledige status van de SQLite-database
* Rollback Journal - Slaat aanvullende informatie op in een tweede bestand en wordt gebruikt tijdens het uitvoeren van transacties. Als SQLite zich in de WAL-modus bevindt, wordt een logbestand voor de schrijfkop bijgehouden.

#### Journaalbestand

Dit bestand is bedoeld om alle informatie bij te houden voor het geval de laatste transactie niet kon worden voltooid, bijvoorbeeld bij een computercrash. Dit bestand wordt gebruikt om het databasebestand in een consistente staat te herstellen.

#### Pagina's

Het belangrijkste SQLite-databasebestand bestaat uit een of meer pagina's. Elke pagina in de hoofddatabase heeft op elk moment een enkelvoudig gebruik, namelijk een van de volgende:

* De lock-byte-pagina
* Een vrije lijstpagina
* Een vrije lijst stampagina
* Een freelist-bladpagina
* Een b-tree-pagina
* Een tafel b-tree interieurpagina
* Een tabel b-boom blad pagina
* Een index b-tree interieurpagina
* Een index b-tree bladpagina
* Een payload-overlooppagina
* Een aanwijzerkaartpagina

De grootte van SQLite-databasebestanden kan variëren van enkele kilobytes tot enkele gigabytes.

### SQLite-koptekst

De SQLite-databasekop bevindt zich in de eerste 100 bytes van het databasebestand. Elk geldig SQLite-databasebestand begint met 16 bytes (in hex): 53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Details van de headervelden zijn zoals in de volgende tabel.

|Offset|Grootte|Beschrijving|
---|---|---|
|0|16|De koptekst: "SQLite formaat 3\000"|
|16|2|De grootte van de databasepagina in bytes. Moet een macht van twee zijn tussen 512 en 32768, of de waarde 1 staat voor een paginagrootte van 65536.|
|18|1|Bestandsformaat schrijfversie. 1 voor erfenis; 2 voor WAL.|
|19|1|Bestandsformaat gelezen versie. 1 voor erfenis; 2 voor WAL.|
|20|1|Bytes ongebruikte "gereserveerde" ruimte aan het einde van elke pagina. Meestal 0.|
|21|1|Maximum ingebed laadvermogen. Moet 64 zijn.|
|22|1|Minimaal ingebed laadvermogen. Moet 32 zijn.|
|23|1|Bladladingsfractie. Moet 32 zijn.|
|24|4|Teller voor bestandswijzigingen.|
|28|4|Grootte van het databasebestand in pagina's. De "in-header databasegrootte".|
|32|4|Paginanummer van de eerste vrije lijst-stampagina.|
|36|4|Totaal aantal freelist-pagina's.|
|40|4|De schemacookie.|
|44|4|Het schemaformaatnummer. Ondersteunde schema-indelingen zijn 1, 2, 3 en 4.|
|48|4|Standaard paginacachegrootte.|
|52|4|Het paginanummer van de grootste root-b-tree-pagina in auto-vacuüm- of incrementeel-vacuümmodus, of anders nul.|
|56|4|De tekstcodering van de database. Een waarde van 1 betekent UTF-8. Een waarde van 2 betekent UTF-16le. Een waarde van 3 betekent UTF-16be.|
|60|4|De "gebruikersversie" zoals gelezen en ingesteld door de user_version pragma.|
|64|4|Waar (niet-nul) voor incrementele vacuümmodus. Onwaar (nul) anders.|
|68|4|De "Applicatie-ID" ingesteld door PRAGMA application_id.|
|72|20|Gereserveerd voor uitbreiding. Moet nul zijn.|
|92|4|Het versie-geldig-voor-nummer.|
|96|4|SQLITE_VERSION_NUMBER|

## Referenties ##

* [SQLite-bestandsindeling - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - C taalspecificaties](https://www.sqlite.org/c3ref/intro.html)

