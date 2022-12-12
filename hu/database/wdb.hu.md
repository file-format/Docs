{
  "date" : "2021-08-24",
  "keywords" :[ "wdb fájl", "wdb fájl formátum", "mi az a wdb fájl", "fájl", "wdb példa", "wdb fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a WDB fájlformátumról és az API-król, amelyek WDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WDB – SQL Server nyomkövetési fájl",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Mi az a WDB fájl?
A .wdb kiterjesztésű fájl valójában a Microsoft Works által létrehozott adatbázisfájl, amelyet olyan funkciók végrehajtására használtak, mint az adatbázis-kezelő rendszer. A WDB fájl hasonló az Access Database ([MDB](/hu/database/mdb/)) fájlhoz, de kevésbé hatékony és nagyobb a korlátozása. A WDB fájlok nem nyithatók meg a Microsoft Access használatával. Azonban megnyithatja a WDB fájlt a Microsoft Works alkalmazásban, majd exportálhatja MDB fájlba, hogy megnyissa a WDB fájlt az MS Accessben.

## WDB fájlformátum
A Microsoft Works Database a Microsoft Works irodai programcsomag natív adatbázis-formátuma. A formátum védett természete és bizonyos korlátozások miatt. A WDB fájlok nem nyithatók meg más szoftverrel, mint a Microsoft Works. Fájlformátumban egy ismétlődő, 10 bájtos fejléc található minden ASCII-szöveglánc előtt, amely a NULL értékkel lezárt mezők értékeit képviseli. A fejléc általában **\x0f** bájttal és NULL-lal kezdődik, amit 4 adatbájt követ, NULL-lal váltakozva.

### Fájlszerkezet

A WDB fájl szerkezete az alábbiakban látható:
- **1. fejléc**: a fájl elejétől, \x25\x00\xf2-vel és 244 NULL bájttal végződve
- **2. fejléc**: \xffT - azaz \xff\x54-gyel kezdődik és 4096 bájtra terjed ki, amely oszlop-/mezőneveket és egyéb dolgokat tartalmaz, és úgy tűnik, hogy a 6144. bájtpozícióval kezdődik.
- **Mező**: az érték 10 bájtos fejléccel rendelkezik, a következő formátummal: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , 2. rész} {db 4} \x00. a 2. adatbájt a mező száma, a 3. adatbájt a rekord száma (a 3. adatbájt hozzáadása, a 2. rész, ha 256 rekord felett megy).


## Referenciák ##

* [Felhasználó:JesseW/wdb formátum](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

