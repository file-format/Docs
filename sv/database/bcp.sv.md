{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om BCP-filformat och API:er som kan skapa och öppna BCP-filer.",
  "title" :"BCP - SQL Server Bulk Copy File Format",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är en BCP fil?

BCP (Bulk Copy Format) är Microsoft SQL Servers tekniska dataformat som definierar datastrukturer för att lagra olika databasdatatypvärden för import/export. Formatet definierar helt tolkningen av varje datakolumn så att uppsättningen värden som anges i datafilen kan läsas. Verktyget [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) använder BCP-filformatet för att läsa data från en sådan fil och identifiera den.


## BCP filformat

BCP-formatfilen är ett XML-dokument som definierar kolumnordningen, namnet och datatypen. Det låter användare importera/exportera stora mängder data från datafil som anger dessa fält. Detta är användbart vid massimport av datavärden från datafiler. Antalet och ordningen på datafälten i datafilen kan skilja sig från de i måltabellens kolumner. Det är då BCP-dataformatfilen kommer till hjälp genom att ange ordning och typ av kolumner för att importera data.

Formatfilens struktur representeras i följande format.

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

|Datatyp|Omfång|Representation|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) till 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Binär|1 till 8000 byte|hexadecimalkodat Unicode-strängformat `Binary = 32000OCTET`|
|Bit|0 eller 1|enkel Unicode-sträng Bit = "0" / "1"|
|Char|1 till 8000|Unicode String Format, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET med n = 4 x (2,147,483,647)|
|Datum|0001-01-01 till 9999-12-31|ÅÅÅÅ-MM-DD strängformat|
|DatumTid|1753-01-01 00:00:00.000 till 9999-12-31 23:59:59.997| Unicode ÅÅÅÅ-MM-DD tt:mm:ss[.nnn] strängformat|
|DateTime2|0001-01-01 00:00:00.0000000 till 9999-12-31 23:59:59.9999999.| Unicode ÅÅÅÅ-MM-DD hh:mm:ss[.nnnnnn] strängformat|
|DateTimeOffset|0001-01-01 00:00:00.0000000 till 9999-12-31 23:59:59.9999999 i tidszonen Coordinated Universal Time (UTC)| Unicode ÅÅÅÅ-MM-DD hh:mm:ss[.nnnnnn] [{+|-}hh:mm] strängformat|
|Decimal|-1038 + 1 till 1038 – 1|Unicode-strängformat `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1,79E+308 till -2,23E-308; 0; från 2.23E-308 till 1.79E+308|Unicode-strängformat|
|Bild|sekvens av byte som sträcker sig från 0 till 231 – 1 (2 147 483 647)|hexadecimalkodat Unicode-strängformat|
|Int|-231 (-2,147,483,648) till 231 – 1 (2,147,483,647)|Unicode-strängformat|

## Referenser

* [BCP-format – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

