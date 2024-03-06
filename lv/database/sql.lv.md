{
  "date": "2020-11-11",
  "keywords": [
"SQL",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par SQL failu formātu un API, kas var izveidot un atvērt SQL failus.",
  "title": "SQL faila formāts — strukturētās vaicājumu valodas datu fails",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-lvl"
}
},
  "lastmod": "2020-11-11"
}

## Kas ir SQL fails?

Fails ar paplašinājumu .sql ir strukturētās vaicājumu valodas (SQL) fails, kas satur kodu darbam ar relāciju datu bāzēm. To izmanto, lai rakstītu SQL paziņojumus CRUD (izveides, lasīšanas, atjaunināšanas un dzēšanas) operācijām datu bāzēs. SQL faili ir izplatīti, strādājot ar darbvirsmas, kā arī tīmekļa datu bāzēm. Ir vairākas SQL alternatīvas, piemēram, Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL un vairākas citas. SQL failus var atvērt ar Microsoft SQL Server, MySQL vaicājumu redaktoriem un citiem vienkārša teksta redaktoriem, piemēram, Notepad operētājsistēmā Windows OS.

## Īsa vēsture

* 1970. gadu sākumā izstrādāja un ieviesa Donals D. Čemberlins un Reimonds F. Boiss uzņēmumā IBM.

* Izmanto, lai saglabātu un izgūtu datus no IBM sākotnējās kvazirelāciju datu bāzes pārvaldības sistēmas System R

* Sākts izmantot komerciālo produktu bāzē, izmantojot System R prototipu, tostarp System/38, SQL/DS un DB2, kas bija komerciāli pieejami attiecīgi 1979., 1981. un 1983. gadā.

* Līdz 1986. gadam ANSI un ISO standartu grupas oficiāli pieņēma kā relāciju datu bāzes pārvaldības sistēmu (RDBMS) standartu "Datubāzes valoda SQL".


## SQL faila formāts

SQL faili ir vienkārša teksta formātā un var sastāvēt no vairākiem valodas elementiem. Vienam SQL failam var pievienot vairākus paziņojumus, ja to izpilde ir iespējama bez atkarības viens no otra. Šīs SQL komandas var izpildīt vaicājumu redaktori, lai veiktu CRUD darbības.

### SQL valodas elementi

SQL valodas elementi ir norādīti tālāk.

|Elements|Apraksts|
---|---|
|Klauzulas| Paziņojumu un vaicājumu sastāvdaļas.|
|Izteiksmes| Var izveidot skalārās vērtības vai tabulas, kas sastāv no datu kolonnām un rindām|
|Predikāti| Norādiet nosacījumus, kurus var novērtēt kā SQL trīsvērtību loģiku (3VL) (patiess/nepatiess/nezināms) vai Būla patiesības vērtības un kurus izmanto, lai ierobežotu paziņojumu un vaicājumu ietekmi vai mainītu programmas plūsmu.|
|Vaicājumi| Izgūstiet datus, pamatojoties uz konkrētiem kritērijiem. Tas ir svarīgs SQL elements.|
|Paziņojumi| Var pastāvīgi ietekmēt shēmas un datus vai kontrolēt transakcijas, programmu plūsmu, savienojumus, sesijas vai diagnostiku.|

### SQL piemērs
Šis SQL priekšraksts izveido tabulu ar nosaukumu **DATA**, kam seko papildu komandas INSERT, lai šajā tabulā ievietotu ierakstus.
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

## Atsauces Nr.

* [SQL, izmantojot Wikipedia](https://en.wikipedia.org/wiki/SQL)

* [SQL sintakse](https://en.wikipedia.org/wiki/SQL_syntax)


