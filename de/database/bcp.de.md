{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das BCP-Dateiformat und APIs, die BCP-Dateien erstellen und öffnen können.",
  "title" :"BCP - SQL Server-Massenkopie-Dateiformat",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine BCP-Datei?

BCP (Bulk Copy Format) ist das technische Datenformat von Microsoft SQL Server, das Datenstrukturen definiert, um verschiedene Datenbankdatentypwerte für den Import/Export zu speichern. Das Format definiert die Interpretation jeder Datenspalte vollständig, sodass der in der Datendatei angegebene Wertesatz gelesen werden kann. Das Dienstprogramm [BCP](https://learn.microsoft.com/en-us/ previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) verwendet das BCP-Dateiformat zum Lesen Daten aus einer solchen Datei und identifizieren sie.


## BCP-Dateiformat

Die Datei im BCP-Format ist ein XML-Dokument, das die Spaltenreihenfolge, den Namen und den Datentyp definiert. Benutzer können große Datenmengen aus Datendateien importieren/exportieren, indem sie diese Felder angeben. Dies ist beim Massenimport von Datenwerten aus Datendateien hilfreich. Die Anzahl und Reihenfolge der Datenfelder in der Datendatei kann sich von denen in den Spalten der Zieltabelle unterscheiden. Hier hilft die BCP-Datenformatdatei, indem sie die Reihenfolge und Art der Spalten für den Datenimport festlegt.

Die Struktur der Formatdatei wird im folgenden Format dargestellt.

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

### BCP-Datentypen

|Datentyp|Bereich|Darstellung|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) bis 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Binär|1 bis 8000 Bytes|hexadezimal codiertes Unicode-Stringformat `Binary = 32000OCTET`|
|Bit|0 oder 1|einfacher Unicode-String Bit = "0" / "1"|
|Zeichen|1 bis 8000|Unicode-String-Format, Zeichen = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET mit n = 4 x (2.147.483.647)|
|Datum|01.01.0001 bis 31.12.9999|Zeichenfolgeformat JJJJ-MM-TT|
|DateTime|1753-01-01 00:00:00.000 bis 9999-12-31 23:59:59.997| Unicode JJJJ-MM-TT hh:mm:ss[.nnn] Zeichenkettenformat|
|DateTime2|0001-01-01 00:00:00.0000000 bis 9999-12-31 23:59:59.9999999.| Unicode JJJJ-MM-TT hh:mm:ss[.nnnnnnn] Zeichenkettenformat|
|DateTimeOffset|0001-01-01 00:00:00.0000000 bis 9999-12-31 23:59:59.9999999 in der Zeitzone der koordinierten Weltzeit (UTC)| Unicode JJJJ-MM-TT hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] Zeichenkettenformat|
|Dezimal|-1038 + 1 bis 1038 – 1|Unicode-String-Format `Dezimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Float|-1,79E+308 bis -2,23E-308; 0; von 2.23E-308 bis 1.79E+308|Unicode-String-Format|
|Bild|Folge von Bytes im Bereich von 0 bis 231 – 1 (2.147.483.647)|hexadezimal codiertes Unicode-Zeichenfolgenformat|
|Int| -231 (-2.147.483.648) bis 231 – 1 (2.147.483.647)|Unicode-String-Format|

## Verweise

* [BCP-Format – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

