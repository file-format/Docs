{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů BCP a rozhraních API, která mohou vytvářet a otevírat soubory BCP.",
  "title" :"BCP - formát souboru hromadného kopírování serveru SQL",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor BCP?

BCP (Bulk Copy Format) je formát technických dat serveru Microsoft SQL Server, který definuje datové struktury pro ukládání různých hodnot datových typů databáze pro import/export. Formát plně definuje interpretaci každého sloupce dat tak, aby bylo možné číst sadu hodnot zadaných v datovém souboru. Nástroj [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) používá ke čtení formát souboru BCP údaje z takového souboru a identifikovat jej.


## Formát souboru BCP

Soubor formátu BCP je dokument XML, který definuje pořadí sloupců, název a datový typ. Umožňuje uživatelům importovat/exportovat velké množství dat z datového souboru specifikujícího tato pole. To je užitečné při hromadném importu datových hodnot z datových souborů. Počet a pořadí datových polí v datovém souboru se mohou lišit od těch ve sloupcích cílové tabulky. To je případ, kdy soubor formátu dat BCP pomůže zadáním pořadí a typu sloupců pro import dat.

Struktura souboru formátu je znázorněna v následujícím formátu.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Datové typy BCP

|Typ dat|Rozsah|Reprezentace|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) až 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Binární|1 až 8000 bajtů|formát řetězce Unicode v šestnáctkové soustavě `Binární = 32000OCTET`|
|Bit|0 nebo 1|jednoduchý řetězec Unicode Bit = "0" / "1"|
|Znak|1 až 8000|Formát řetězce Unicode, znak = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET s n = 4 x (2,147,483,647)|
|Datum|0001-01-01 až 9999-12-31|YYYY-MM-DD formát řetězce|
|DatumČas|1753-01-01 00:00:00.000 až 9999-12-31 23:59:59.997| Unicode RRRR-MM-DD hh:mm:ss[.nnn] formát řetězce|
|DatumČas2|0001-01-01 00:00:00.0000000 až 9999-12-31 23:59:59,9999999.| Unicode RRRR-MM-DD hh:mm:ss[.nnnnnn] formát řetězce|
|DateTimeOffset|0001-01-01 00:00:00.0000000 až 9999-12-31 23:59:59.9999999 v časovém pásmu UTC (Coordinated Universal Time)| Unicode RRRR-MM-DD hh:mm:ss[.nnnnnn] [{+|-}hh:mm] formát řetězce|
|Desetinné|-1038 + 1 až 1038 – 1|Formát řetězce Unicode `Desetinné = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Plovák|-1,79E+308 až -2,23E-308; 0; od 2.23E-308 do 1.79E+308|Formát řetězce Unicode|
|Obrázek|sekvence bajtů v rozsahu od 0 do 231 – 1 (2 147 483 647)|formát řetězce Unicode v šestnáctkové soustavě|
|Int|-231 (-2,147,483,648) až 231 – 1 (2,147,483,647)|Formát řetězce Unicode|

## Reference

* [Formát BCP – Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

