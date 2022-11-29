{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om SQL-filformat och API:er som kan skapa och öppna SQL-filer.",
  "title" :"SQL-filformat - en datafil för strukturerat frågespråk",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Vad är en SQL-fil?

En fil med filtillägget .sql är en SQL-fil (Structured Query Language) som innehåller kod för att fungera med relationsdatabaser. Den används för att skriva SQL-satser för CRUD-operationer (Create, Read, Update and Delete) på databaser. SQL-filer är vanliga när man arbetar med stationära och webbaserade databaser. Det finns flera alternativ till SQL som Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL och flera andra. SQL-filer kan öppnas av frågeredigerare av Microsoft SQL Server, MySQL och andra textredigerare som Anteckningar i Windows OS.

## Kortfattad bakgrund

* Utvecklad och introducerad av Donal D. Chamberlin och Raymond F. Boyce på IBM i början av 1970-talet
* Används för att lagra och hämta data från IBM:s ursprungliga kvasi-relationella databashanteringssystem, System R
* Började användas i kommersiella produkter baserar på sin System R-prototyp inklusive System/38, SQL/DS och DB2, som var kommersiellt tillgängliga 1979, 1981 respektive 1983.
* Officiellt antagen av ANSI och ISO standardgrupper som standard "Databas Language SQL" för relationsdatabashanteringssystem (RDBMS) 1986

## SQL filformat

SQL-filer är i vanligt textformat och kan bestå av flera språkelement. Flera satser kan läggas till i en enda SQL-fil om deras exekvering är möjlig utan att vara beroende av varandra. Dessa SQL-kommandon kan exekveras av frågeredigerare för att utföra CRUD-operationer.

### SQL-språkelement

SQL-språkelement är enligt listan nedan.

|Element|Beskrivning|
---|---|
|Klausuler| Beståndsdelar i uttalanden och frågor.|
|Uttryck| Kan producera antingen skalära värden eller tabeller som består av kolumner och rader med data|
|Predikat| Ange villkor som kan utvärderas till SQL-logik med tre värden (3VL) (sant/falskt/okänt) eller booleska sanningsvärden och används för att begränsa effekterna av satser och frågor, eller för att ändra programflödet.|
|Frågor| Hämta data baserat på specifika kriterier. Detta är en viktig del av SQL.|
|Uttalanden| Kan ha en bestående effekt på scheman och data, eller kan kontrollera transaktioner, programflöde, anslutningar, sessioner eller diagnostik.|

### SQL-exempel
Följande SQL-sats skapar en tabell med namnet **DATA**, följt av ytterligare 'INSERT'-kommandon för att infoga poster i denna tabell.
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

## Referenser ##

* [SQL av Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [SQL-syntax](https://en.wikipedia.org/wiki/SQL_syntax)

