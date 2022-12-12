{
  "date" : "2020-11-11",
  "keywords" :["SQL", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku SQL i interfejsy API, które mogą tworzyć i otwierać pliki SQL.",
  "title" :"Format pliku SQL — plik danych w ustrukturyzowanym języku zapytań",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Czym jest plik SQL?

Plik z rozszerzeniem .sql to plik Structured Query Language (SQL), który zawiera kod do pracy z relacyjnymi bazami danych. Służy do pisania instrukcji SQL dla operacji CRUD (Create, Read, Update i Delete) w bazach danych. Pliki SQL są powszechne podczas pracy z komputerowymi i internetowymi bazami danych. Istnieje kilka alternatyw dla SQL, takich jak Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL i kilka innych. Pliki SQL mogą być otwierane przez edytory zapytań Microsoft SQL Server, MySQL i inne edytory zwykłego tekstu, takie jak Notatnik w systemie operacyjnym Windows.

## Krótka historia

* Opracowany i wprowadzony przez Donala D. Chamberlina i Raymonda F. Boyce'a w IBM na początku lat 70.
* Służy do przechowywania i pobierania danych z oryginalnego quasi-relacyjnego systemu zarządzania bazami danych IBM, System R
* Rozpoczął używanie w bazie produktów komercyjnych w prototypie Systemu R, w tym System/38, SQL/DS i DB2, które były dostępne na rynku odpowiednio w 1979, 1981 i 1983 roku.
* Oficjalnie przyjęty przez grupy norm ANSI i ISO jako standard „Database Language SQL” dla systemów zarządzania relacyjnymi bazami danych (RDBMS) do 1986 r.

## Format pliku SQL

Pliki SQL są w formacie zwykłego tekstu i mogą składać się z kilku elementów językowych. Wiele instrukcji można dodać do jednego pliku SQL, jeśli ich wykonanie jest możliwe bez zależności od siebie. Te polecenia SQL mogą być wykonywane przez edytory zapytań w celu wykonywania operacji CRUD.

### Elementy języka SQL

Elementy języka SQL są wymienione poniżej.

|Element|Opis|
---|---|
|Klauzule| Składniki składowe instrukcji i zapytań.|
|Wyrażenia| Może generować wartości skalarne lub tabele składające się z kolumn i wierszy danych|
|Predykaty| Określ warunki, które mogą być ocenione na podstawie trójwartościowej logiki SQL (3VL) (prawda/fałsz/nieznane) lub logicznych wartości prawdy i są używane do ograniczania skutków instrukcji i zapytań lub do zmiany przebiegu programu.|
|Zapytania| Pobieraj dane na podstawie określonych kryteriów. Jest to ważny element SQL.|
|Oświadczenia| Może mieć trwały wpływ na schematy i dane lub może kontrolować transakcje, przepływ programu, połączenia, sesje lub diagnostykę.|

### Przykład SQL
Poniższa instrukcja SQL tworzy tabelę o nazwie **DATA**, po której następuje dodatkowe polecenie `INSERT` w celu wstawienia rekordów do tej tabeli.
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

## Bibliografia ##

* [SQL z Wikipedii](https://en.wikipedia.org/wiki/SQL)
* [Składnia SQL](https://en.wikipedia.org/wiki/SQL_syntax)

