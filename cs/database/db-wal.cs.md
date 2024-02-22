{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souborů DB-WAL a rozhraních API, která mohou vytvářet a otevírat soubory DB-WAL.",
  "title" : "Formát souboru DB-WAL - SQLite Database Write-Ahead Log File",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-cs",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Co je soubor DB-WAL?

Přípona souboru .db-wal je spojena s SQLite, populárním open-source systémem pro správu relačních databází. Formát souboru WAL (zkratka pro Write-Ahead Log) je alternativou k tradičnímu rollback žurnálu používanému SQLite. Poskytuje větší kontrolu souběžnosti, umožňuje více procesům číst databázi současně, přičemž stále poskytuje možnosti obnovy po havárii. Soubor .db-wal se používá k ukládání změn provedených v databázi, které ještě nebyly potvrzeny do hlavního databázového souboru (s příponou .db).

## Obecný formát WAL

Ve formátu souboru WAL (Write-Ahead Log) jsou změny provedené v databázi nejprve zapsány do souboru WAL, než jsou potvrzeny do hlavního databázového souboru. To umožňuje více souběžný přístup k databázi, protože během provádění změn může z databáze číst více procesů. Formát souboru WAL navíc poskytuje možnosti obnovení po havárii, což umožňuje vrátit databázi zpět do předchozího stavu v případě neočekávaného vypnutí.

## Rozdíl mezi formátem DB-WAL a WAL

Oba formáty souborů .db-wal a WAL jsou spojeny s SQLite, populárním open-source systémem pro správu relačních databází. Mezi nimi je však jemný rozdíl.

Soubor .db-wal je v podstatě soubor WAL, ale s jinou příponou. Soubor .db-wal se používá k ukládání změn provedených v databázi, které ještě nebyly potvrzeny do hlavního databázového souboru (s příponou .db), zatímco formát souboru WAL se používá k ukládání protokolu o změnách databáze napřed. .

Jinými slovy, soubor .db-wal je specifický typ souboru WAL, který používají databáze SQLite k ukládání změn provedených v databázi, které ještě nebyly potvrzeny do hlavního databázového souboru. Formát souboru WAL je obecný termín pro tento typ formátu souboru.

Takže WAL je obecný termín pro formát souboru, .db-wal je specifická implementace formátu souboru WAL používaného databázemi SQLite.

## Reference
* [Formát souboru v režimu WAL](https://www.sqlite.org/walformat.html)

* [Zápis dopředu](https://www.sqlite.org/wal.html)


