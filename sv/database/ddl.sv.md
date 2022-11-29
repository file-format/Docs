{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DDL-filformat och API:er som kan skapa och öppna DDL-filer.",
  "title" :"DDL File Format - A Data Definition Language File",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Vad är en DDL fil?

En fil med filändelsen .ddl är en Data Definition Language-fil som används för att definiera schemat för en databas. Den innehåller satser/kommandon för att arbeta med databasstrukturer som tabeller, kolumner, poster och andra fält. Kommandon i en DDL-fil skrivs i [SQL](/sv/database/sql/) och kan utföra operationer som att skapa tabell i databasen, släppa och uppdatera. Ett databasschema ägs av dess skapade och alla CRUD-operationer kan utföras på det. Populära applikationer som kan skapa och öppna DDL-filer är Windows Text Editor, Jetbrains Intellij Idea och EclipseLink.

## DDL-kommandon

En enda DDL-fil kan innehålla flera kommandon som, på grund av korrekt syntax, kommer att köras i följd och göra ändringar i schemat som att skapa teckenuppsättningar och tabeller, ta bort tabeller, byta namn på och ändra tabeller. Följande DDL-kommandon används ofta när du arbetar med databasschema.

`CREATE` - Används för att skapa databasen eller dess objekt (som tabell, index, funktion, vyer, lagringsprocedur och triggers).

`DROP` – Används för att ta bort objekt från databasen.

`ALTER` - Används för att ändra strukturen i databasen.

`TRUNCATE` – Används för att ta bort alla poster från en tabell, inklusive alla utrymmen som tilldelats för posterna tas bort.

`KOMMENTAR` – Lägger till kommentarer till dataordboken.

`RENAME` – Byter namn på ett befintligt objekt i databasen.

## Exempel på DDL

Följande exempel visar DDL-satsen för CREATE-kommandot som skapar en tabell och definierar dess fält.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referenser ##

* [DDL av Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

