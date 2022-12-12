{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf fájl", "mi az sdf fájl", "hogyan lehet megnyitni egy sdf fájlt", "kiterjesztés", "fájl", "sdf fájl formátum", "adatbázis fájl típusa", "adatbázis fájl formátuma", "Adatbázis fájlok" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az SDF fájlformátumról és az SDF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"SDF - SQL Server Compact Database File",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Mi az SDF fájl?
Az .sdf kiterjesztésű fájl tartalmazza a Microsoft SQL Server Compact (SQL CE) adatbázist, amely kompakt relációs adatbázisként is ismert; a Microsoft által a mobileszközökre és asztali számítógépekre készült alkalmazásokhoz. Támogatja a 32 és 64 bites operációs rendszert, és az adatbázis teljes tartalma egyetlen SDF fájlban található, és több mint 4 GB lemezterületet foglalhat el. Biztonsági okokból egy .sdf fájl 128 bites titkosítással is titkosítható. Az SQL CE futási környezet párhuzamos többfelhasználós hozzáférést állít be az .sdf fájlhoz. Az SDF fájl másolható a **QuickOnce** segítségével, vagy egyszerűen átmásolható a célhelyre a rendszer telepítéséhez.

## SDF fájl formátum
Az SDF fájl egy adatbázist tartalmaz, amelyet általában kompakt relációs adatbázisnak neveznek. Az SDF fájl tartalmazza az adatbázissal kapcsolatos összes információt, az SQL Server Compact pedig egy könnyű és ingyenes adatbázismotor, amely az .sdf fájlok kezelésére szolgál. Az .sdf fájl mérete nem haladhatja meg a 4 GB-os korlátot. Az SDF-fájlok nem tárolják a tárolt eljárásokról, triggerekről vagy nézetekről szóló információkat. Az SQL CE-adatbázist használó alkalmazásoknak nem kell megadniuk az SDF-fájl elérési útját az ADO.NET kapcsolati karakterláncban, ehelyett az |DataDirectory|\database_name.sdf néven említhető, amely meghatározza az alkalmazás összeállítási jegyzékében definiált adatkönyvtárat
Az .sdf elnevezési konvenció nem kötelező, és bármilyen kiterjesztéssel menthető a fájl. A jelszó beállítása az adatbázisfájlhoz nem kötelező lépés. Az adatbázis tömörítéséhez vagy javításához a fájlt el kell menteni a **tömörített/javított adatbázis** opcióval.

## Hivatkozások

* [SQL Server Compact – Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Az SQL Server Compact használata ASP.NET webalkalmazásokhoz](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


