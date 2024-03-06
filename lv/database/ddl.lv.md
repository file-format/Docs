{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DDL failu formātu un API, kas var izveidot un atvērt DDL failus.",
  "title": "DDL faila formāts — datu definīcijas valodas fails",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-lvl"
}
},
  "lastmod": "2020-11-11"
}

## Kas ir DDL fails?

Fails ar paplašinājumu .ddl ir datu definīcijas valodas fails, ko izmanto, lai definētu datu bāzes shēmu. Tajā ir priekšraksti/komandas darbam ar datu bāzes struktūrām, piemēram, tabulām, kolonnām, ierakstiem un citiem laukiem. Komandas DDL failā ir rakstītas [SQL](/database/sql/) un var veikt tādas darbības kā tabulas izveide datu bāzē, nomešana un atjaunināšana. Datu bāzes shēma pieder tās izveidotajai shēmai, un tajā var veikt visas CRUD darbības. Populāras lietojumprogrammas, ar kurām var izveidot un atvērt DDL failus, ir Windows teksta redaktors, Jetbrains Intellij Idea un EclipseLink.

## DDL komandas

Vienā DDL failā var būt vairākas komandas, kas, pateicoties pareizai sintaksei, tiks izpildītas secīgi un veiks izmaiņas shēmā, piemēram, veidos rakstzīmju kopas un tabulas, atmetīs tabulas, pārdēvējot un mainot tabulas. Strādājot ar datu bāzes shēmu, parasti tiek izmantotas šādas DDL komandas.

`CREATE` — izmanto, lai izveidotu datu bāzi vai tās objektus (piemēram, tabulu, indeksu, funkciju, skatus, krātuves procedūru un trigerus).

`DROP` — izmanto objektu dzēšanai no datu bāzes.

ALTER — izmanto, lai mainītu datu bāzes struktūru.

TRUNCATE — izmanto, lai no tabulas noņemtu visus ierakstus, tostarp tiek noņemtas visas ierakstiem atvēlētās atstarpes.

`COMMENT` — pievieno komentārus datu vārdnīcai.

`PĀRNAME` — pārdēvē esošu objektu datu bāzē.

## DDL piemērs

Nākamajā piemērā parādīts DDL priekšraksts komandai CREATE, kas izveido tabulu un definē tās laukus.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Atsauces Nr.

* [DDL by Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)


