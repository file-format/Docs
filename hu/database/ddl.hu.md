{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DDL fájlformátumról és az API-król, amelyek DDL fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DDL fájlformátum – adatdefiníciós nyelvi fájl",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Mi az a DDL fájl?

A .ddl kiterjesztésű fájl egy Data Definition Language fájl, amely egy adatbázis sémájának meghatározására szolgál. Utasításokat/parancsokat tartalmaz az adatbázis-struktúrákkal, például táblákkal, oszlopokkal, rekordokkal és egyéb mezőkkel való munkához. A DDL-fájlok parancsai [SQL]-ben (/hu/database/sql/) vannak írva, és olyan műveleteket hajthatnak végre, mint például táblázat létrehozása az adatbázisban, eldobás és frissítés. Az adatbázisséma a létrehozott adatbázis séma tulajdonosa, és az összes CRUD-művelet végrehajtható rajta. A DDL-fájlok létrehozására és megnyitására alkalmas népszerű alkalmazások a Windows Text Editor, a Jetbrains Intellij Idea és az EclipseLink.

## DDL parancsok

Egyetlen DDL fájl több parancsot is tartalmazhat, amelyek a helyes szintaxis miatt sorban futnak le, és módosítják a sémát, például karakterkészleteket és táblákat hoznak létre, táblákat dobnak el, táblákat neveznek át és módosítanak. A következő DDL-parancsok gyakran használatosak az adatbázissémával végzett munka során.

`CREATE` - Az adatbázis vagy annak objektumai (például tábla, index, függvény, nézetek, tárolási eljárás és triggerek) létrehozására szolgál.

`DROP` – Objektumok törlésére szolgál az adatbázisból.

`ALTER` - Az adatbázis szerkezetének megváltoztatására szolgál.

"TRUNCATE" – A tábla összes rekordjának eltávolítására szolgál, beleértve a rekordokhoz lefoglalt összes szóközt is.

MEGJEGYZÉS – Megjegyzések hozzáadása az adatszótárhoz.

`RENAME` – Átnevez egy meglévő objektumot az adatbázisban.

## DDL példa

A következő példa a CREATE parancs DDL utasítását mutatja be, amely létrehoz egy táblát és meghatározza a mezőit.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referenciák ##

* [DDL by Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

