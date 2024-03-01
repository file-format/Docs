{
  "date": "2020-11-11",
  "keywords": [
"SQL",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi SQL-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata SQL-tiedostoja.",
  "title": "SQL-tiedostomuoto – strukturoitu kyselykielitietotiedosto",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-fil"
}
},
  "lastmod": "2020-11-11"
}

## Mikä on SQL-tiedosto?

Tiedosto, jonka tunniste on .sql, on SQL (Structured Query Language) -tiedosto, joka sisältää koodia relaatiotietokantojen kanssa käytettäväksi. Sitä käytetään SQL-käskyjen kirjoittamiseen tietokantojen CRUD-operaatioille (Create, Read, Update ja Delete). SQL-tiedostot ovat yleisiä työpöytä- ja verkkopohjaisten tietokantojen kanssa työskennellessä. SQL:lle on useita vaihtoehtoja, kuten Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL ja monet muut. SQL-tiedostoja voidaan avata Microsoft SQL Serverin, MySQL:n ja muiden tekstieditorien, kuten Windows-käyttöjärjestelmän Notepadin, kyselyeditorilla.

## Lyhyt historia

* Kehittäjät ja esittelijät Donal D. Chamberlin ja Raymond F. Boyce IBM:llä 1970-luvun alussa

* Käytetään tietojen tallentamiseen ja hakemiseen IBM:n alkuperäisestä kvasirelaatiotietokannan hallintajärjestelmästä System R

* Käytetään kaupallisissa tuotteissa, jotka perustuvat System R -prototyyppiin, mukaan lukien System/38, SQL/DS ja DB2, jotka olivat kaupallisesti saatavilla vuosina 1979, 1981 ja 1983.

* ANSI- ja ISO-standardiryhmät hyväksyivät virallisesti relaatiotietokannan hallintajärjestelmien (RDBMS) "Database Language SQL" -standardin vuoteen 1986 mennessä


## SQL-tiedostomuoto

SQL-tiedostot ovat pelkkää tekstiä ja voivat sisältää useita kielielementtejä. Yhteen SQL-tiedostoon voidaan lisätä useita lauseita, jos niiden suorittaminen on mahdollista ilman toisistaan riippuvuutta. Kyselyeditorit voivat suorittaa nämä SQL-komennot CRUD-toimintojen suorittamiseksi.

### SQL-kielen elementtejä

SQL-kielen elementit ovat alla lueteltuja.

|Elementti|Kuvaus|
---|---|
|Lausekkeet| Lausuntojen ja kyselyiden osatekijät.|
|lausekkeet| Voi tuottaa joko skalaariarvoja tai taulukoita, jotka koostuvat tietosarakkeista ja -riveistä|
|Predikaatit| Määritä ehdot, jotka voidaan arvioida SQL:n kolmiarvoiseksi logiikaksi (3VL) (tosi/epätosi/tuntematon) tai loogisiksi totuusarvoiksi ja joita käytetään rajoittamaan käskyjen ja kyselyiden vaikutuksia tai muuttamaan ohjelman kulkua.|
|Kyselyt| Hae tiedot tiettyjen kriteerien perusteella. Tämä on tärkeä osa SQL:ää.|
|Lausunnot| Voi vaikuttaa pysyvästi kaavioihin ja tietoihin tai ohjata tapahtumia, ohjelmakulkua, yhteyksiä, istuntoja tai diagnostiikkaa.|

### SQL-esimerkki
Seuraava SQL-käsky luo taulukon nimeltä **DATA**, jota seuraa ylimääräiset INSERT-komennot tietueiden lisäämiseksi tähän taulukkoon.
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

## Viitteet ##

* [SQL by Wikipedia](https://en.wikipedia.org/wiki/SQL)

* [SQL-syntaksi](https://en.wikipedia.org/wiki/SQL_syntax)


