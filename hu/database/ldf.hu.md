{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "kiterjesztés", "fájl", "fájlformátum", "adatbázis fájltípus", "adatbázisfájl formátum", "adatbázis fájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az LDF fájlformátumról és az LDF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"LDF - SQL Server főadatbázis fájlformátum",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az LDF fájl?

Az .ldf kiterjesztésű fájl egy naplófájl, amelyet a Microsoft SQL Server tart fenn, amely egy relációs adatbázis-kezelő rendszer (RDBMS). Az elsődleges adatbázisfájlokon ([MDF](/hu/database/mdf/)) végrehajtott összes tranzakció (például beillesztés, frissítés, törlés) az LDF fájlban rögzítésre kerül. Az LDF fájlok minden adatbázis kritikus összetevői. Rendszerhiba esetén a naplófájl segítségével állítja vissza az adatbázist egy konzisztens állapotba. A tranzakciós naplófájl mérete megnőhet, ha a tranzakciók nincsenek teljesen lekötve. Az LDF fájlok Microsoft SQL Server szoftveralkalmazással nyithatók meg.

## LDF fájlban rögzített műveletek

Egy SQL naplófájl a következő műveleteket rögzíti:

* Minden tranzakció eleje és vége.

* Minden adatmódosítás (beszúrás, frissítés vagy törlés). Ez magában foglalja a rendszerben tárolt eljárások vagy az adatdefiníciós nyelv (DDL) utasításai által végrehajtott változtatásokat is bármely táblában, beleértve a rendszertáblázatokat is.

* Minden kiterjedés és oldalkiosztás vagy felosztás.

* Táblázat vagy index létrehozása vagy eldobása.

## LDF fájl formátum

Az LDF fájl SQL Server tranzakciós rekordokból áll, amelyek naplórekordok karakterláncaként vannak elrendezve. Minden naplórekordnak van egy naplósorszáma (LSN), amely magasabb, mint az előző rekord LSN-je. A karakterláncok egymás után vannak összefűzve a fájlban. A modern nagy sebességű számítógépeknek köszönhetően olyan rekordokat lehet beilleszteni, ahol az LSN2 az LSN1 előtt található a naplófájlban. Mivel a műveletek soros formában vannak rögzítve, az LSN2 által leírt változás az LSN1 naplórekord után történt. Egy adott tranzakció rekordjai visszafelé kapcsolódnak a használt mutatók segítségével, amelyek felgyorsítják a tranzakció visszaállítását.
 

## Hivatkozások

* [Adatbázisfájlok és fájlcsoportok](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Tranzakciónapló architektúra és -kezelési útmutató](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- szerver-ver15)

