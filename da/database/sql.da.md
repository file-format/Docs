{
  "date": "2020-11-11",
  "keywords": [
"SQL",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om SQL-filformat og API'er, der kan oprette og åbne SQL-filer.",
  "title": "SQL-filformat - en datafil med struktureret forespørgselssprog",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-dal"
}
},
  "lastmod": "2020-11-11"
}

## Hvad er en SQL-fil?

En fil med filtypenavnet .sql er en SQL-fil (Structured Query Language), der indeholder kode til at arbejde med relationelle databaser. Det bruges til at skrive SQL-sætninger til CRUD-operationer (Create, Read, Update and Delete) på databaser. SQL-filer er almindelige, når du arbejder med desktop såvel som webbaserede databaser. Der er flere alternativer til SQL, såsom Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL og flere andre. SQL-filer kan åbnes af forespørgselseditorer af Microsoft SQL Server, MySQL og andre almindelige teksteditorer såsom Notesblok på Windows OS.

## Kort historie

* Udviklet og introduceret af Donal D. Chamberlin og Raymond F. Boyce hos IBM i begyndelsen af 1970'erne

* Bruges til at gemme og hente data fra IBMs originale kvasi-relationelle databasestyringssystem, System R

* Startet brugt i kommercielle produkter baseret på deres System R-prototype inklusive System/38, SQL/DS og DB2, som var kommercielt tilgængelige i henholdsvis 1979, 1981 og 1983.

* Officielt vedtaget af ANSI- og ISO-standardgrupper som standard "Database Language SQL" for relationelle databasestyringssystemer (RDBMS) i 1986


## SQL filformat

SQL-filer er i almindeligt tekstformat og kan bestå af flere sprogelementer. Flere sætninger kan tilføjes til en enkelt SQL-fil, hvis deres udførelse er mulig uden at være afhængig af hinanden. Disse SQL-kommandoer kan udføres af forespørgselseditorer til at udføre CRUD-operationer.

### SQL-sprogelementer

SQL-sprogelementer er som angivet nedenfor.

|Element|Beskrivelse|
---|---|
|Klausuler| Konstituerende komponenter i udsagn og forespørgsler.|
|Udtryk| Kan producere enten skalarværdier eller tabeller bestående af kolonner og rækker af data|
|prædikater| Angiv betingelser, der kan evalueres til SQL-logik med tre værdier (3VL) (sand/falsk/ukendt) eller boolske sandhedsværdier og bruges til at begrænse virkningerne af udsagn og forespørgsler eller til at ændre programforløb.|
|Forespørgsler| Hent dataene ud fra specifikke kriterier. Dette er et vigtigt element i SQL.|
|Erklæringer| Kan have en vedvarende effekt på skemaer og data eller kan kontrollere transaktioner, programflow, forbindelser, sessioner eller diagnostik.|

### SQL-eksempel
Den følgende SQL-sætning opretter en tabel med navnet **DATA**, efterfulgt af yderligere 'INSERT'-kommandoer for at indsætte poster i denne tabel.
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

## Referencer ##

* [SQL af Wikipedia](https://en.wikipedia.org/wiki/SQL)

* [SQL-syntaks](https://en.wikipedia.org/wiki/SQL_syntax)


