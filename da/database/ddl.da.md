{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DDL-filformat og API'er, der kan oprette og åbne DDL-filer.",
  "title": "DDL-filformat - En sprogfil med datadefinition",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-dal"
}
},
  "lastmod": "2020-11-11"
}

## Hvad er en DDL fil?

En fil med filtypen .ddl er en Data Definition Language-fil, der bruges til at definere skemaet for en database. Den indeholder sætninger/kommandoer til at arbejde med databasestrukturer såsom tabeller, kolonner, poster og andre felter. Kommandoer i en DDL-fil er skrevet i [SQL](/database/sql/) og kan udføre operationer såsom oprettelse af tabel i database, drop og opdatering. Et databaseskema ejes af dets oprettede, og alle CRUD-operationer kan udføres på det. Populære programmer, der kan oprette og åbne DDL-filer, er Windows Text Editor, Jetbrains Intellij Idea og EclipseLink.

## DDL kommandoer

En enkelt DDL-fil kan indeholde flere kommandoer, der på grund af korrekt syntaks vil køre i rækkefølge og foretage ændringer i skemaet, såsom oprettelse af tegnsæt og tabeller, droppe tabeller, omdøbe og ændre tabeller. Følgende DDL-kommandoer bruges ofte, mens du arbejder med databaseskema.

`CREATE` - Bruges til at oprette databasen eller dens objekter (som tabel, indeks, funktion, visninger, lagerprocedure og triggere).

`DROP` – Bruges til at slette objekter fra databasen.

`ALTER` - Bruges til at ændre strukturen i databasen.

`TRUNCATE` – Bruges til at fjerne alle poster fra en tabel, inklusive alle pladser, der er allokeret til posterne, fjernes.

`KOMMENTAR` – Tilføjer kommentarer til dataordbogen.

`RENAME` – Omdøber et eksisterende objekt i databasen.

## DDL eksempel

Følgende eksempel viser DDL-sætning for CREATE-kommandoen, som opretter en tabel og definerer dens felter.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referencer ##

* [DDL af Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)


