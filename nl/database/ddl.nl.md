{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DDL-bestandsindelingen en API's die DDL-bestanden kunnen maken en openen.",
  "title" :"DDL-bestandsindeling - een taalbestand voor gegevensdefinitie",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Wat is een DDL-bestand?

Een bestand met de extensie .ddl is een Data Definition Language-bestand dat wordt gebruikt om het schema van een database te definiëren. Het bevat instructies/opdrachten voor het werken met databasestructuren zoals tabellen, kolommen, records en andere velden. Commando's in een DDL-bestand zijn geschreven in [SQL](/nl/database/sql/) en kunnen bewerkingen uitvoeren zoals het maken van een tabel in de database, neerzetten en bijwerken. Een databaseschema is eigendom van het gemaakte en alle CRUD-bewerkingen kunnen erop worden uitgevoerd. Populaire toepassingen die DDL-bestanden kunnen maken en openen zijn Windows Text Editor, Jetbrains Intellij Idea en EclipseLink.

## DDL-opdrachten

Een enkel DDL-bestand kan verschillende opdrachten bevatten die, dankzij de correcte syntaxis, in volgorde worden uitgevoerd en wijzigingen in het schema aanbrengen, zoals het maken van tekensets en tabellen, het verwijderen van tabellen, het hernoemen en wijzigen van tabellen. De volgende DDL-opdrachten worden vaak gebruikt bij het werken met databaseschema's.

`CREATE` - Wordt gebruikt om de database of zijn objecten te maken (zoals tabel, index, functie, views, winkelprocedure en triggers).

`DROP` – Wordt gebruikt om objecten uit de database te verwijderen.

`ALTER` - Wordt gebruikt om de structuur van de database te wijzigen.

`TRUNCATE` – Wordt gebruikt om alle records uit een tabel te verwijderen, inclusief alle spaties die aan de records zijn toegewezen.

`COMMENT` – Voegt opmerkingen toe aan de datadictionary.

`RENAME` – Hernoemt een bestaand object in de database.

## DDL-voorbeeld

Het volgende voorbeeld toont de DDL-instructie voor de opdracht CREATE waarmee een tabel wordt gemaakt en de velden worden gedefinieerd.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referenties ##

* [DDL door Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

