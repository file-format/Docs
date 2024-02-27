{
  "date": "2020-11-11",
  "keywords": [
"BCP",
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
  "description": "Lær om BCP-filformat og API'er, der kan oprette og åbne BCP-filer.",
  "title": "BCP - SQL Server Bulk Copy File Format",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-dap"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er en BCP fil?

BCP (Bulk Copy Format) er Microsoft SQL Servers tekniske dataformat, der definerer datastrukturer til at gemme forskellige databasedatatypeværdier til import/eksport. Formatet definerer fuldstændigt fortolkningen af hver datakolonne, så det sæt af værdier, der er angivet i datafilen, kan læses. Værktøjet [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) bruger BCP-filformatet til at læse data fra en sådan fil og identificere dem.


## BCP filformat

BCP-formatfilen er et XML-dokument, der definerer kolonnerækkefølgen, navnet og datatypen. Det lader brugere importere/eksportere store mængder data fra datafil, der specificerer disse felter. Dette er nyttigt ved masseimport af dataværdier fra datafiler. Antallet og rækkefølgen af datafelter i datafilen kan være anderledes end dem i destinationstabelkolonnerne. Det er, når BCP-dataformatfilen kommer til hjælp ved at angive rækkefølgen og typen af kolonner til import af data.

Strukturen af formatfilen er repræsenteret i følgende format.

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

### BCP-datatyper

|Datatype|Område|Repræsentation|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) til 263-1 (9.223.372.036.854.775.807)|`BigInt = [-]1*19DIGIT`|
|Binær|1 til 8000 bytes|hexadecimalkodet Unicode-strengformat `Binært = 32000OCTET`|
|Bit|0 eller 1|simpel Unicode-streng Bit = 0 / 1|
|Char|1 til 8000|Unicode-strengformat, Char = 16000OCTET|
|CLRUDT|VarBinær|CLRUDT = 0*nOCTET med n = 4 x (2.147.483.647)|
|Dato|0001-01-01 til 9999-12-31|ÅÅÅÅ-MM-DD strengformat|
|DatoTid|1753-01-01 00:00:00.000 til 9999-12-31 23:59:59.997| Unicode ÅÅÅÅ-MM-DD tt:mm:ss[.nnn] strengformat|
|DatoTid2|0001-01-01 00:00:00.0000000 til og med 9999-12-31 23:59:59.9999999.| Unicode ÅÅÅÅ-MM-DD tt:mm:ss[.nnnnnn] strengformat|
|DateTimeOffset|0001-01-01 00:00:00.0000000 til 9999-12-31 23:59:59.9999999 i tidszonen Coordinated Universal Time (UTC)| Unicode ÅÅÅÅ-MM-DD tt:mm:ss[.nnnnnn] [{+|-}tt:mm] strengformat|
|Decimal|-1038 + 1 til 1038 – 1|Unicode-strengformat `Decimal = [-] 0*38DIGIT [.0*38DIGIT]`|
|Float|-1,79E+308 til -2,23E-308; 0; fra 2.23E-308 til 1.79E+308|Unicode-strengformat|
|Billede|sekvens af bytes, der spænder fra 0 til 231 – 1 (2.147.483.647)|hexadecimalkodet Unicode-strengformat|
|Int|-231 (-2.147.483.648) til 231 – 1 (2.147.483.647)|Unicode-strengformat|

## Referencer

 * [BCP-format - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

