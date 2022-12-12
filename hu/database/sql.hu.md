{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az SQL fájlformátumról és az SQL-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"SQL fájlformátum – strukturált lekérdezési nyelvi adatfájl",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Mi az SQL fájl?

Az .sql kiterjesztésű fájl egy strukturált lekérdezési nyelv (SQL) fájl, amely kódot tartalmaz a relációs adatbázisokkal való együttműködéshez. SQL utasítások írására szolgál az adatbázisokon a CRUD (Create, Read, Update és Delete) műveletekhez. Az SQL-fájlok gyakoriak az asztali és a webalapú adatbázisok használatakor. Az SQL-nek számos alternatívája létezik, például a Java Persistence Query Language (JPQL), a LINQ, a HTSQL, a 4D QL és még sok más. Az SQL-fájlok megnyithatók a Microsoft SQL Server, a MySQL lekérdezésszerkesztőivel és más egyszerű szövegszerkesztőkkel, például a Windows operációs rendszer Jegyzettömbjével.

## Rövid története

* Donal D. Chamberlin és Raymond F. Boyce fejlesztette ki és vezette be az IBM-nél az 1970-es évek elején
* Adatok tárolására és lekérésére szolgál az IBM eredeti kvázi-relációs adatbázis-kezelő rendszeréből, a System R-ből
* Kereskedelmi termékekben kezdték használni a System R prototípuson, beleértve a System/38-at, SQL/DS-t és DB2-t, amelyek 1979-ben, 1981-ben és 1983-ban voltak kereskedelmi forgalomban.
* 1986-ra hivatalosan az ANSI és ISO szabványcsoportok szabványos "adatbázisnyelvi SQL"-ként fogadták el a relációs adatbázis-kezelő rendszerek (RDBMS) számára.

## SQL fájlformátum

Az SQL-fájlok egyszerű szöveges formátumúak, és több nyelvi elemet is tartalmazhatnak. Egyetlen SQL-fájlhoz több utasítás is hozzáadható, ha végrehajtásuk egymástól való függés nélkül lehetséges. Ezeket az SQL parancsokat lekérdezésszerkesztők hajthatják végre a CRUD műveletek végrehajtásához.

### SQL nyelvi elemek

Az SQL nyelvi elemek az alábbiak szerint vannak felsorolva.

|Elem|Leírás|
---|---|
|Záradékok| Az utasítások és lekérdezések alkotóelemei.|
|Kifejezések| Akár skaláris értékeket, akár oszlopokból és adatsorokból álló táblázatokat készíthet|
|Predikátumok| Adjon meg olyan feltételeket, amelyek kiértékelhetők SQL háromértékű logikára (3VL) (igaz/hamis/ismeretlen) vagy logikai igazságértékekre, és amelyek az utasítások és lekérdezések hatásainak korlátozására vagy a programfolyamat megváltoztatására szolgálnak.|
|Lekérdezések| Az adatok lekérése meghatározott kritériumok alapján. Ez az SQL fontos eleme.|
|Nyilatkozatok| Tartós hatással lehet a sémákra és adatokra, vagy szabályozhatja a tranzakciókat, a programfolyamatokat, a kapcsolatokat, a munkameneteket vagy a diagnosztikát.|

### SQL példa
A következő SQL utasítás létrehoz egy **DATA** nevű táblát, amelyet további `INSERT` parancs követ a rekordok ebbe a táblába történő beszúrásához.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referenciák ##

* [SQL a Wikipedia-tól](https://en.wikipedia.org/wiki/SQL)
* [SQL szintaxis](https://en.wikipedia.org/wiki/SQL_syntax)

