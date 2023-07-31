{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier BCP și despre API-urile care pot crea și deschide fișiere BCP.",
  "title" :"BCP - SQL Server Bulk Copy File Format",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier BCP?

BCP (Bulk Copy Format) este formatul de date tehnice al Microsoft SQL Server care definește structurile de date pentru a stoca diferite valori ale tipurilor de date ale bazei de date pentru import/export. Formatul definește pe deplin interpretarea fiecărei coloane de date, astfel încât setul de valori specificat în fișierul de date să poată fi citit. Utilitarul [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) folosește formatul de fișier BCP pentru a citi date dintr-un astfel de fișier și identificați-l.


## Format de fișier BCP

Fișierul în format BCP este un document XML care definește ordinea coloanelor, numele și tipul de date. Permite utilizatorilor să importe/exporta date mari din fișierele de date care specifică aceste câmpuri. Acest lucru este util în importul în bloc al valorilor datelor din fișierele de date. Numărul și ordinea câmpurilor de date din fișierul de date pot fi diferite de cele din coloanele tabelului de destinație. Acesta este momentul în care fișierul format de date BCP vine în ajutor prin specificarea ordinii și tipului de coloane pentru importul datelor.

Structura fișierului de format este reprezentată în următorul format.

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

### Tipuri de date BCP

|Tip de date|Interval|Reprezentare|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) la 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Binar|1 până la 8000 de octeți|format de șir Unicode codificat hexazecimal `Binar = 32000OCTET`|
|Bit|0 sau 1|șir Unicode simplu Bit = "0" / "1"|
|Char|1 la 8000|Unicode String Format, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET cu n = 4 x (2.147.483.647)|
|Data|0001-01-01 până la 9999-12-31|AAAA-LL-ZZ format șir|
|DateTime|1753-01-01 00:00:00.000 până la 9999-12-31 23:59:59.997| Unicode AAAA-LL-ZZ hh:mm:ss[.nnn] format șir|
|DateTime2|0001-01-01 00:00:00.0000000 până la 9999-12-31 23:59:59.9999999.| Unicode AAAA-LL-ZZ hh:mm:ss[.nnnnnnn] format șir|
|DateTimeOffset|0001-01-01 00:00:00.0000000 până la 9999-12-31 23:59:59.9999999 în fusul orar Coordinated Universal Time (UTC)| Unicode AAAA-LL-ZZ hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] format șir|
|Decimală|-1038 + 1 până la 1038 – 1|Format șir Unicode `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1,79E+308 până la -2,23E-308; 0; de la 2.23E-308 la 1.79E+308|Format șir Unicode|
|Imagine|secvență de octeți care variază de la 0 la 231 – 1 (2.147.483.647)|format șir Unicode codificat hexazecimal|
|Int|-231 (-2.147.483.648) până la 231 – 1 (2.147.483.647)|Format șir Unicode|

## Referințe

* [Format BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

