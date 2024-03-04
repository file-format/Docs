{
  "date": "2020-11-11",
  "keywords": [
"SQL",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie SQL failo formatą ir API, kurios gali kurti ir atidaryti SQL failus.",
  "title": "SQL failo formatas – struktūrinės užklausos kalbos duomenų failas",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-ltl"
}
},
  "lastmod": "2020-11-11"
}

## Kas yra SQL failas?

Failas su plėtiniu .sql yra struktūrinės užklausos kalbos (SQL) failas, kuriame yra kodas, skirtas dirbti su reliacinėmis duomenų bazėmis. Jis naudojamas SQL sakiniams rašyti CRUD (Create, Read, Update ir Delete) operacijoms duomenų bazėse. SQL failai yra įprasti dirbant su darbalaukiu ir žiniatinklio duomenų bazėmis. Yra keletas SQL alternatyvų, tokių kaip Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL ir keletas kitų. SQL failus galima atidaryti naudojant Microsoft SQL Server, MySQL ir kitų paprasto teksto redaktorių, pvz., Windows OS užrašų knygelę, užklausų redaktoriai.

## Trumpa istorija

* Aštuntojo dešimtmečio pradžioje sukūrė ir pristatė Donalas D. Chamberlinas ir Raymondas F. Boyce'as IBM.

* Naudojamas duomenims iš IBM originalios kvazirelacinės duomenų bazių valdymo sistemos System R saugoti ir gauti

* Pradėtas naudoti komerciniuose produktuose, naudojant jų System R prototipą, įskaitant System/38, SQL/DS ir DB2, kurie buvo parduodami atitinkamai 1979, 1981 ir 1983 m.

* Iki 1986 m. ANSI ir ISO standartų grupės oficialiai priimtos kaip standartinė „duomenų bazės kalba SQL“ reliacinėms duomenų bazių valdymo sistemoms (RDBMS).


## SQL failo formatas

SQL failai yra paprasto teksto formatu ir juos gali sudaryti keli kalbos elementai. Į vieną SQL failą galima įtraukti kelis teiginius, jei jų vykdymas įmanomas nepriklausant vienas nuo kito. Šias SQL komandas gali vykdyti užklausų redaktoriai, skirti CRUD operacijoms atlikti.

### SQL kalbos elementai

SQL kalbos elementai pateikiami toliau.

|Elementas|Aprašymas|
---|---|
|Sąlygos| Teiginių ir užklausų sudedamosios dalys.|
|Išraiškos| Gali sukurti arba skaliarines reikšmes, arba lenteles, sudarytas iš duomenų stulpelių ir eilučių|
|Predikatai| Nurodykite sąlygas, kurios gali būti įvertintos pagal SQL trijų reikšmių logiką (3VL) (teisinga/klaidinga/nežinoma) arba Būlio tiesos reikšmes ir naudojamos norint apriboti teiginių ir užklausų poveikį arba pakeisti programos srautą.|
|Užklausos| Gaukite duomenis pagal konkrečius kriterijus. Tai svarbus SQL elementas.|
|Pareiškimai| Gali turėti nuolatinį poveikį schemoms ir duomenims arba valdyti operacijas, programų srautą, ryšius, seansus ar diagnostiką.|

### SQL pavyzdys
Šis SQL sakinys sukuria lentelę pavadinimu **DATA**, po kurios pateikiamos papildomos INSERT komandos įrašams įterpti į šią lentelę.
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

## Nuorodos Nr.

* [Vikipedijos SQL](https://en.wikipedia.org/wiki/SQL)

* [SQL sintaksė](https://en.wikipedia.org/wiki/SQL_syntax)


