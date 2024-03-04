{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie DB-WAL failo formatą ir API, kurios gali kurti ir atidaryti DB-WAL failus.",
  "title" : "DB-WAL failo formatas – SQLite duomenų bazės įrašymo į priekį žurnalo failas",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-lt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Kas yra DB-WAL failas?

Failo plėtinys .db-wal yra susijęs su SQLite – populiaria atvirojo kodo reliacinių duomenų bazių valdymo sistema. WAL failo formatas (sutrumpintas Write-Ahead Log) yra alternatyva tradiciniam atšaukimo žurnalui, kurį naudoja SQLite. Tai suteikia daugiau lygiagretumo valdymo, leidžiant keliems procesams vienu metu skaityti duomenų bazę, kartu suteikiant gedimų atkūrimo galimybes. .db-wal failas naudojamas duomenų bazės pakeitimams, kurie dar nebuvo priskirti pagrindiniam duomenų bazės failui (su plėtiniu .db), saugoti.

## Bendras WAL formatas

WAL (Write-Ahead Log) failo formatu duomenų bazėje atlikti pakeitimai pirmiausia įrašomi į WAL failą prieš įtraukiant juos į pagrindinį duomenų bazės failą. Tai leidžia vienu metu pasiekti duomenų bazę, nes keli procesai gali nuskaityti iš duomenų bazės, kol atliekami pakeitimai. Be to, WAL failo formatas suteikia gedimų atkūrimo galimybes, todėl netikėto išjungimo atveju duomenų bazė gali būti grąžinta į ankstesnę būseną.

## Skirtumas tarp DB-WAL ir WAL formatų

Tiek .db-wal, tiek WAL failų formatai yra susieti su SQLite – populiaria atvirojo kodo reliacinių duomenų bazių valdymo sistema. Tačiau tarp jų yra subtilus skirtumas.

.db-wal failas iš esmės yra WAL failas, bet su kitu failo plėtiniu. .db-wal failas naudojamas duomenų bazės pakeitimams, kurie dar neįtraukti į pagrindinį duomenų bazės failą (su plėtiniu .db), saugoti, o WAL failo formatas naudojamas duomenų bazės pakeitimų įrašymo į priekį žurnalui saugoti. .

Kitaip tariant, .db-wal failas yra konkretus WAL failo tipas, kurį SQLite duomenų bazės naudoja duomenų bazės pakeitimams, kurie dar nebuvo priskirti pagrindiniam duomenų bazės failui, saugoti. WAL failo formatas yra bendras šio tipo failo formato terminas.

Taigi, WAL yra bendras failo formato terminas, .db-wal yra specifinis WAL failo formato, naudojamo SQLite duomenų bazėse, įgyvendinimas.

## Nuorodos
* [WAL režimo failo formatas](https://www.sqlite.org/walformat.html)

* [Priešį rašymo registravimas](https://www.sqlite.org/wal.html)


