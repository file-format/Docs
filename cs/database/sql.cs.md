{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "rozšíření", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů SQL a rozhraních API, která mohou vytvářet a otevírat soubory SQL.",
  "title" :"Formát souboru SQL - datový soubor strukturovaného dotazovacího jazyka",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Co je soubor SQL?

Soubor s příponou .sql je soubor SQL (Structured Query Language), který obsahuje kód pro práci s relačními databázemi. Používá se k zápisu příkazů SQL pro operace CRUD (Create, Read, Update, and Delete) v databázích. Soubory SQL jsou běžné při práci s desktopovými i webovými databázemi. Existuje několik alternativ k SQL, jako je Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL a několik dalších. Soubory SQL lze otevřít pomocí editorů dotazů Microsoft SQL Server, MySQL a dalších editorů prostého textu, jako je Poznámkový blok na OS Windows.

## Stručná historie

* Vyvinuto a představeno Donalem D. Chamberlinem a Raymondem F. Boycem v IBM na počátku 70. let
* Používá se k ukládání a získávání dat z původního kvazi-relačního systému správy databází IBM System R
* Začalo se používat v základně komerčních produktů na jejich prototypu System R včetně System/38, SQL/DS a DB2, které byly komerčně dostupné v letech 1979, 1981 a 1983.
* Oficiálně přijato skupinami norem ANSI a ISO jako standard „Databázový jazyk SQL“ pro systémy správy relačních databází (RDBMS) do roku 1986

## Formát souboru SQL

Soubory SQL jsou ve formátu prostého textu a mohou se skládat z několika jazykových prvků. Do jednoho souboru SQL lze přidat více příkazů, pokud je jejich provádění možné bez závislosti na sobě. Tyto příkazy SQL mohou být spouštěny editory dotazů pro provádění operací CRUD.

### Prvky jazyka SQL

Prvky jazyka SQL jsou uvedeny níže.

|Prvek|Popis|
---|---|
|Ustanovení| Složky příkazů a dotazů.|
|Výrazy| Může vytvářet buď skalární hodnoty, nebo tabulky sestávající ze sloupců a řádků dat|
|Predikáty| Zadejte podmínky, které lze vyhodnotit na trojhodnotovou logiku SQL (3VL) (pravda/nepravda/neznámá) nebo booleovské pravdivostní hodnoty a používají se k omezení účinků příkazů a dotazů nebo ke změně toku programu.|
|Dotazy| Získejte data na základě specifických kritérií. Toto je důležitý prvek SQL.|
|Prohlášení| Může mít trvalý vliv na schémata a data nebo může řídit transakce, tok programu, připojení, relace nebo diagnostiku.|

### Příklad SQL
Následující příkaz SQL vytvoří tabulku s názvem **DATA**, po níž následují další příkazy `INSERT` pro vložení záznamů do této tabulky.
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

## Reference ##

* [SQL od Wikipedie](https://en.wikipedia.org/wiki/SQL)
* [Syntaxe SQL](https://en.wikipedia.org/wiki/SQL_syntax)

