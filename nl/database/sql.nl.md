{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over SQL-bestandsindeling en API's die SQL-bestanden kunnen maken en openen.",
  "title" :"SQL-bestandsindeling - een gestructureerd gegevensbestand in querytaal",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Wat is een SQL-bestand?

Een bestand met de extensie .sql is een Structured Query Language (SQL)-bestand dat code bevat om met relationele databases te werken. Het wordt gebruikt om SQL-instructies te schrijven voor CRUD-bewerkingen (Create, Read, Update en Delete) op databases. SQL-bestanden komen vaak voor bij het werken met zowel desktop- als webgebaseerde databases. Er zijn verschillende alternatieven voor SQL, zoals Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL en verschillende andere. SQL-bestanden kunnen worden geopend door query-editors van Microsoft SQL Server, MySQL en andere platte-teksteditors zoals Kladblok op Windows OS.

## Korte geschiedenis

* Ontwikkeld en geïntroduceerd door Donal D. Chamberlin en Raymond F. Boyce bij IBM in het begin van de jaren zeventig
* Gebruikt om gegevens op te slaan en op te halen uit IBM's oorspronkelijke quasi-relationele databasebeheersysteem, System R
* Begonnen in commerciële producten op basis van hun System R-prototype, waaronder System/38, SQL/DS en DB2, die respectievelijk in 1979, 1981 en 1983 in de handel verkrijgbaar waren.
* Officieel aangenomen door ANSI- en ISO-standaardgroepen als standaard "Database Language SQL" voor relationele databasebeheersystemen (RDBMS) in 1986

## SQL-bestandsindeling

SQL-bestanden zijn in platte tekst en kunnen uit verschillende taalelementen bestaan. Meerdere instructies kunnen aan een enkel SQL-bestand worden toegevoegd als hun uitvoering mogelijk is zonder van elkaar afhankelijk te zijn. Deze SQL-commando's kunnen worden uitgevoerd door query-editors voor het uitvoeren van CRUD-bewerkingen.

### SQL-taalelementen

SQL-taalelementen zijn zoals hieronder vermeld.

|Element|Beschrijving|
---|---|
|Clausules| Bestanddelen van statements en queries.|
|Uitdrukkingen| Kan zowel scalaire waarden als tabellen produceren die bestaan uit kolommen en rijen met gegevens|
|Predikaten| Geef voorwaarden op die kunnen worden geëvalueerd tot driewaardige SQL-logica (3VL) (waar/onwaar/onbekend) of Booleaanse waarheidswaarden en die worden gebruikt om de effecten van instructies en query's te beperken of om de programmastroom te wijzigen.|
|Query's| Haal de gegevens op op basis van specifieke criteria. Dit is een belangrijk element van SQL.|
|Statementen| Kan een blijvend effect hebben op schema's en gegevens, of kan transacties, programmastroom, verbindingen, sessies of diagnostiek beheersen.|

### SQL-voorbeeld
De volgende SQL-instructie maakt een tabel met de naam **DATA**, gevolgd door aanvullende `INSERT'-opdrachten om records in deze tabel in te voegen.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referenties ##

* [SQL door Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [SQL-syntaxis](https://en.wikipedia.org/wiki/SQL_syntaxis)

