{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over BCP-bestandsindeling en API's die BCP-bestanden kunnen maken en openen.",
  "title" :"BCP - SQL Server Bulk Copy-bestandsindeling",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een BCP-bestand?

BCP (Bulk Copy Format) is het technische gegevensformaat van Microsoft SQL Server dat gegevensstructuren definieert om verschillende databasegegevenstypewaarden op te slaan voor import/export. Het formaat definieert volledig de interpretatie van elke gegevenskolom, zodat de reeks waarden die in het gegevensbestand is gespecificeerd, kan worden gelezen. Het hulpprogramma [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) gebruikt de BCP-bestandsindeling om gegevens uit een dergelijk bestand en identificeer het.


## BCP-bestandsindeling

Het bestand in BCP-indeling is een XML-document dat de kolomvolgorde, naam en gegevenstype definieert. Hiermee kunnen gebruikers grote hoeveelheden gegevens importeren/exporteren uit een gegevensbestand waarin deze velden worden gespecificeerd. Dit is handig bij het bulksgewijs importeren van gegevenswaarden uit gegevensbestanden. Het aantal en de volgorde van gegevensvelden in het gegevensbestand kunnen verschillen van die in de kolommen van de doeltabel. Dit is wanneer het BCP-gegevensformaatbestand helpt door de volgorde en het type kolommen voor het importeren van de gegevens op te geven.

De structuur van het formaatbestand wordt weergegeven in het volgende formaat.

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

### BCP-gegevenstypen

|Gegevenstype|Bereik|Representatie|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) tot en met 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Binair|1 tot 8000 bytes|hexadecimaal gecodeerd Unicode-tekenreeksformaat `Binair = 32000OCTET`|
|Bit|0 of 1|eenvoudige Unicode-string Bit = "0" / "1"|
|Char|1 tot en met 8000|Unicode-tekenreeksformaat, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET met n = 4 x (2.147.483.647)|
|Datum|0001-01-01 t/m 9999-12-31|JJJJ-MM-DD tekenreeksformaat|
|DateTime|1753-01-01 00:00:00.000 t/m 9999-12-31 23:59:59,997| Unicode JJJJ-MM-DD uu:mm:ss[.nnn] tekenreeksformaat|
|DateTime2|0001-01-01 00:00:00.0000000 t/m 9999-12-31 23:59:59,999999.| Unicode JJJJ-MM-DD uu:mm:ss[.nnnnnnn] tekenreeksformaat|
|DateTimeOffset|0001-01-01 00:00:00.0000000 t/m 9999-12-31 23:59:59,99999999 in de tijdzone Coordinated Universal Time (UTC)| Unicode JJJJ-MM-DD uu:mm:ss[.nnnnnn] [{+|-}uu:mm] tekenreeksformaat|
|Decimaal|-1038 + 1 t/m 1038 – 1|Unicode-tekenreeksformaat `Decimaal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1.79E+308 t/m -2.23E-308; 0; van 2.23E-308 tot 1.79E+308|Unicode-tekenreeksformaat|
|Image|reeks van bytes die variëren van 0 tot 231 – 1 (2.147.483.647)|hexadecimaal gecodeerd Unicode-tekenreeksformaat|
|Int|-231 (-2.147.483.648) tot en met 231 – 1 (2.147.483.647)|Unicode-tekenreeksformaat|

## Referenties

* [BCP-indeling - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

