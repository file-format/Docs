{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier SQL și despre API-urile care pot crea și deschide fișiere SQL.",
  "title" :"Format de fișier SQL - Un fișier de date structurat în limbajul de interogare",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Ce este un fișier SQL?

Un fișier cu extensia .sql este un fișier SQL (Structured Query Language) care conține cod pentru a lucra cu baze de date relaționale. Este folosit pentru a scrie instrucțiuni SQL pentru operațiuni CRUD (Creare, Read, Update, and Delete) pe baze de date. Fișierele SQL sunt comune în timpul lucrului cu baze de date desktop, precum și bazate pe web. Există mai multe alternative la SQL, cum ar fi Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL și multe altele. Fișierele SQL pot fi deschise de editorii de interogări ale Microsoft SQL Server, MySQL și alte editori de text simplu, cum ar fi Notepad pe sistemul de operare Windows.

## Scurt istoric

* Dezvoltat și introdus de Donal D. Chamberlin și Raymond F. Boyce la IBM la începutul anilor 1970
* Folosit pentru a stoca și a prelua date din sistemul original de gestionare a bazelor de date cvasi-relaționale al IBM, System R
* Au început să fie utilizate în baza de produse comerciale, cu prototipul System R, inclusiv System/38, SQL/DS și DB2, care au fost disponibile comercial în 1979, 1981 și, respectiv, 1983.
* Adoptat oficial de către grupurile standard ANSI și ISO ca standard „Database Language SQL” pentru sistemele de management al bazelor de date relaționale (RDBMS) până în 1986

## Format de fișier SQL

Fișierele SQL sunt în format text simplu și pot cuprinde mai multe elemente de limbaj. Mai multe instrucțiuni pot fi adăugate la un singur fișier SQL dacă executarea lor este posibilă fără a depinde unele de altele. Aceste comenzi SQL pot fi executate de editori de interogări pentru a efectua operațiuni CRUD.

### Elemente de limbaj SQL

Elementele limbajului SQL sunt enumerate mai jos.

|Element|Descriere|
---|---|
|Clauze| Componentele constitutive ale declarațiilor și interogărilor.|
|Expresii| Poate produce fie valori scalare, fie tabele formate din coloane și rânduri de date|
|Predicate| Specificați condițiile care pot fi evaluate la logica cu trei valori SQL (3VL) (adevărat/fals/necunoscut) sau valori de adevăr boolean și sunt utilizate pentru a limita efectele declarațiilor și interogărilor sau pentru a modifica fluxul programului.|
|Interogări| Preluați datele pe baza unor criterii specifice. Acesta este un element important al SQL.|
|Declarații| Poate avea un efect persistent asupra schemelor și datelor sau poate controla tranzacțiile, fluxul de programe, conexiunile, sesiunile sau diagnosticele.|

### Exemplu SQL
Următoarea instrucțiune SQL creează un tabel numit **DATA**, urmat de comenzi suplimentare `INSERT` pentru a insera înregistrări în acest tabel.
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

## Referințe ##

* [SQL de la Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Sintaxă SQL](https://en.wikipedia.org/wiki/SQL_syntax)

