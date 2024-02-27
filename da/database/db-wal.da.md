{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om DB-WAL filformat og API'er, der kan oprette og åbne DB-WAL filer.",
  "title" : "DB-WAL filformat - SQLite Database Write-Ahead Log File",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-da",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Hvad er en DB-WAL fil?

Filtypenavnet .db-wal er forbundet med SQLite, et populært open source-system til relationel databasestyring. WAL-filformatet (forkortelse for Write-Ahead Log) er et alternativ til den traditionelle rollback-journal, der bruges af SQLite. Det giver mere samtidighedskontrol, hvilket tillader flere processer at læse databasen på samme tid, mens det stadig giver mulighed for gendannelse af nedbrud. .db-wal-filen bruges til at gemme ændringer foretaget i databasen, som endnu ikke er blevet committed til hoveddatabasefilen (med .db-udvidelse).

## Generelt WAL-format

I WAL-filformatet (Write-Ahead Log) skrives ændringer, der er foretaget i databasen, først til WAL-filen, før de forpligtes til hoveddatabasefilen. Dette giver mulighed for mere samtidig adgang til databasen, da flere processer kan læse fra databasen, mens der foretages ændringer. Derudover giver WAL-filformatet mulighed for gendannelse af nedbrud, hvilket gør det muligt for databasen at blive rullet tilbage til en tidligere tilstand i tilfælde af en uventet nedlukning.

## Forskellen mellem DB-WAL og WAL format

Både .db-wal- og WAL-filformater er forbundet med SQLite, et populært open source-system til relationel databasestyring. Der er dog en subtil forskel mellem de to.

.db-wal-filen er i det væsentlige en WAL-fil, men med en anden filtypenavn. .db-wal-filen bruges til at gemme ændringer foretaget i databasen, som endnu ikke er blevet forpligtet til hoveddatabasefilen (med .db-udvidelse), mens WAL-filformatet bruges til at gemme fremskrivningsloggen for databaseændringerne .

Med andre ord er en .db-wal-fil en specifik type WAL-fil, der bruges af SQLite-databaser til at gemme ændringer foretaget i databasen, som endnu ikke er blevet forpligtet til hoveddatabasefilen. WAL-filformatet er den generelle betegnelse for denne type filformat.

Så WAL er den generelle betegnelse for filformatet, .db-wal er en specifik implementering af WAL-filformatet, der bruges af SQLite-databaser.

## Referencer
* [WAL-tilstand filformat](https://www.sqlite.org/walformat.html)

* [Write-Ahead-logning](https://www.sqlite.org/wal.html)


