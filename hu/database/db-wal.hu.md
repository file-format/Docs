{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Ismerje meg a DB-WAL fájlformátumot és az API-kat, amelyek DB-WAL fájlokat hozhatnak létre és nyithatnak meg.",
  "title" : "DB-WAL fájlformátum – SQLite Database előreírási naplófájl",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-hu",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Mi az a DB-WAL fájl?

A .db-wal fájlkiterjesztés az SQLite-hoz, egy népszerű nyílt forráskódú relációs adatbázis-kezelő rendszerhez kapcsolódik. A WAL fájlformátum (a Write-Ahead Log rövidítése) az SQLite által használt hagyományos visszagörgetési napló alternatívája. Több párhuzamossági vezérlést biztosít, lehetővé téve több folyamat egyidejű olvasását az adatbázisban, miközben továbbra is biztosít összeomlás-helyreállítási lehetőségeket. A .db-wal fájl az adatbázisban végrehajtott módosítások tárolására szolgál, amelyek még nincsenek véglegesítve a fő adatbázisfájlban (.db kiterjesztéssel).

## Általános WAL formátum

A WAL (Write-Ahead Log) fájlformátumban az adatbázisban végrehajtott módosítások először a WAL-fájlba íródnak, mielőtt véglegesítésre kerülnek a fő adatbázisfájlban. Ez lehetővé teszi az adatbázishoz való egyidejű hozzáférést, mivel a változtatások végrehajtása közben több folyamat is olvashat az adatbázisból. Ezenkívül a WAL fájlformátum összeomlás-helyreállítási lehetőségeket is biztosít, lehetővé téve az adatbázis visszaállítását egy korábbi állapotba váratlan leállás esetén.

## Különbség a DB-WAL és a WAL formátum között

Mind a .db-wal, mind a WAL fájlformátum az SQLite-hoz, egy népszerű nyílt forráskódú relációs adatbázis-kezelő rendszerhez kapcsolódik. Van azonban egy finom különbség a kettő között.

A .db-wal fájl lényegében egy WAL-fájl, de más fájlkiterjesztéssel. A .db-wal fájl az adatbázisban végrehajtott módosítások tárolására szolgál, amelyek még nincsenek véglegesítve a fő adatbázisfájlban (.db kiterjesztéssel), míg a WAL fájlformátum az adatbázis-változások előreírási naplójának tárolására szolgál. .

Más szavakkal, a .db-wal fájl egy meghatározott típusú WAL-fájl, amelyet az SQLite-adatbázisok használnak az adatbázisban végrehajtott olyan módosítások tárolására, amelyeket még nem rögzítettek a fő adatbázisfájlban. A WAL fájlformátum az ilyen típusú fájlformátumok általános kifejezése.

Tehát a WAL a fájlformátum általános kifejezése, a .db-wal pedig az SQLite adatbázisok által használt WAL fájlformátum speciális megvalósítása.

## Hivatkozások
* [WAL-módú fájlformátum](https://www.sqlite.org/walformat.html)

* [Előre írásos naplózás](https://www.sqlite.org/wal.html)


