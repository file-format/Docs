{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par DB-WAL faila formātu un API, kas var izveidot un atvērt DB-WAL failus.",
  "title" : "DB-WAL faila formāts — SQLite datu bāzes ierakstāms žurnālfails",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-lv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Kas ir DB-WAL fails?

Faila paplašinājums .db-wal ir saistīts ar SQLite, populāru atvērtā koda relāciju datu bāzes pārvaldības sistēmu. WAL faila formāts (saīsinājums no Write-Ahead Log) ir alternatīva tradicionālajam atcelšanas žurnālam, ko izmanto SQLite. Tas nodrošina lielāku vienlaicīguma kontroli, ļaujot vairākiem procesiem vienlaikus lasīt datu bāzi, vienlaikus nodrošinot avāriju atkopšanas iespējas. .db-wal fails tiek izmantots, lai saglabātu datubāzē veiktās izmaiņas, kas vēl nav iekļautas galvenajā datu bāzes failā (ar paplašinājumu .db).

## Vispārējs WAL formāts

WAL (Write-Ahead Log) faila formātā datu bāzē veiktās izmaiņas vispirms tiek ierakstītas WAL failā, pirms tās tiek veiktas galvenajā datu bāzes failā. Tas nodrošina vienlaicīgāku piekļuvi datu bāzei, jo vairāki procesi var nolasīt no datu bāzes, kamēr tiek veiktas izmaiņas. Turklāt WAL faila formāts nodrošina avāriju atkopšanas iespējas, ļaujot neparedzētas izslēgšanas gadījumā atjaunot datubāzi iepriekšējā stāvoklī.

## Atšķirība starp DB-WAL un WAL formātu

Gan .db-wal, gan WAL failu formāti ir saistīti ar SQLite, populāru atvērtā koda relāciju datu bāzes pārvaldības sistēmu. Tomēr starp abiem ir smalka atšķirība.

.db-wal fails būtībā ir WAL fails, taču ar citu faila paplašinājumu. .db-wal failu izmanto, lai saglabātu datubāzē veiktās izmaiņas, kas vēl nav iekļautas galvenajā datu bāzes failā (ar paplašinājumu .db), savukārt WAL faila formāts tiek izmantots, lai saglabātu datu bāzes izmaiņu ierakstīšanas žurnālu. .

Citiem vārdiem sakot, .db-wal fails ir noteikta veida WAL fails, ko SQLite datu bāzes izmanto, lai saglabātu datu bāzē veiktās izmaiņas, kas vēl nav iekļautas galvenajā datu bāzes failā. WAL faila formāts ir vispārīgs termins šāda veida faila formātam.

Tātad WAL ir vispārīgs faila formāta termins, bet .db-wal ir īpaša WAL faila formāta ieviešana, ko izmanto SQLite datu bāzes.

## Atsauces
* [WAL režīma faila formāts](https://www.sqlite.org/walformat.html)

* [Iespējamā reģistrēšana](https://www.sqlite.org/wal.html)


