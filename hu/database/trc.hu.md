{
  "date" : "2021-08-24",
  "keywords" :[ "trc fájl", "trc fájlformátum", "mi az a trc fájl", "fájl", "trc példa", "trc fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a TRC fájlformátumról és az API-król, amelyek TRC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"TRC – SQL Server nyomkövetési fájl",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Mi az a TRC fájl?
A .trc kiterjesztésű fájl egy Miscrosoft SQL szerver adatbázis tevékenységének nyomkövetési eredményeit tartalmazza. Ezeket a fájlokat egy SQL Server Profiler szoftver hozza létre; általában Microsoft SQL Server szoftverrel csomagolják. Az adatbázis-adminisztrátorok elemezhetik az adatbázis-utasítások sorozatát, és áttekinthetik a nyomkövetési naplót, ha valamilyen hiba vagy figyelmeztetés gyanúja merül fel. Ezek a fájlok általában az MSSQL tipikus LOG mappájában találhatók, a Program Files könyvtárban Windows operációs rendszeren.

## TRC fájlformátum
A TRC fájlformátumot az SQL Server Profiler használja az MS SQL szerver által nemrég végrehajtott utasítások új nyomkövetésének automatikus létrehozásához. Az SQL Server Profiler az alapértelmezett sablont használja minden új nyomkövetéshez. A szoftver azonban számos előre definiált sablont tartalmaz bizonyos típusú események figyeléséhez. Az SQL Server Profiler is használható sablonok létrehozására, amelyek meghatározzák a nyomkövetésekbe foglalandó eseményosztályokat és adatoszlopokat.

### Előre meghatározott sablonok
Íme az SQL Server Profilerben található néhány előre definiált sablon listája:
- **SP_Counts**: Rögzíti a tárolt eljárások végrehajtási viselkedését az idő múlásával.
- **Normál**: Általános kiindulópont a nyomkövetés létrehozásához.
- **TSQL**: Rögzíti az ügyfelek által az SQL Servernek elküldött összes Transact-SQL utasítást és a kiadás idejét.
- **TSQL_Duration**: Rögzíti az ügyfelek által az SQL Servernek küldött összes Transact-SQL utasítást, azok végrehajtási idejét, és időtartam szerint csoportosítja azokat.
- **TSQL_Grouped**: Egy adott ügyféltől vagy felhasználótól érkező lekérdezések kivizsgálására használható.
- **TSQL_Locks**: a holtpontok hibaelhárítására, a zárolási időtúllépésre és az eszkalációs események zárolására használható.
- **TSQL_Replay**: Iteratív hangolás, például benchmark tesztelés végrehajtására használható.
- **TSQL_SPs**: A tárolt eljárások összetevő lépéseinek elemzésére szolgál.
- **Tuning**: Nyomkövetési kimenet létrehozására szolgál, amelyet a Database Engine Tuning Advisor munkaterhelésként használhat az adatbázisok hangolásához.
### Kövesse össze a nyomkövetést a Windows Performance Log adatokkal
Az SQL Server Profiler segítségével megnyithat egy Microsoft Windows teljesítménynaplót, kiválaszthatja a nyomkövetéssel korrelálandó számlálókat, és megjelenítheti a kiválasztott teljesítményszámlálókat a nyomkövetés mellett az MS SQL Server Profiler grafikus felületén. A kiválasztott nyomkövetési eseménnyel kapcsolatos teljesítménynapló-adatok jelzéséhez egy függőleges piros sáv az SQL Server Profiler System Monitor adatablak paneljén.


## Referenciák ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

