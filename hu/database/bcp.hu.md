{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "kiterjesztés", "fájl", "fájlformátum", "adatbázis fájltípus", "adatbázisfájl formátum", "adatbázis fájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a BCP fájlformátumról és az API-król, amelyek BCP-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"BCP - SQL Server tömeges másolási fájlformátum",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az a BCP fájl?

A BCP (Bulk Copy Format) a Microsoft SQL Server műszaki adatformátuma, amely adatstruktúrákat határoz meg a különböző adatbázis-adattípus-értékek tárolására importálás/exportálás céljából. A formátum teljes mértékben meghatározza az egyes adatoszlopok értelmezését, hogy az adatfájlban megadott értékkészlet olvasható legyen. A [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) segédprogram a BCP fájlformátumot használja az olvasáshoz egy ilyen fájlból származó adatokat, és azonosítsa azokat.


## BCP fájlformátum

A BCP formátumú fájl egy XML dokumentum, amely meghatározza az oszlopok sorrendjét, nevét és adattípusát. Lehetővé teszi a felhasználók számára nagy mennyiségű adat importálását/exportálását az ezeket a mezőket meghatározó adatfájlból. Ez hasznos az adatértékek adatfájlokból történő tömeges importálásakor. Az adatfájlban lévő adatmezők száma és sorrendje eltérhet a céltábla oszlopaiban lévőktől. Ilyenkor a BCP adatformátum fájl segít az adatok importálásához szükséges oszlopok sorrendjének és típusának megadásával.

A formátumfájl szerkezete a következő formátumban látható.

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

### BCP adattípusok

|Adattípus|Tartomány|Képviselet|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) – 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Bináris|1–8000 bájt|hexadecimális kódolású Unicode karakterlánc-formátum `Bináris = 32000OCTET`|
|Bit|0 vagy 1|egyszerű Unicode karakterlánc Bit = "0" / "1"|
|Char|1–8000|Unicode karakterlánc formátum, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET, n = 4 x (2 147 483 647)|
|Dátum|0001-01-01-9999-12-31|ÉÉÉÉ-HH-NN karakterlánc formátum|
|DátumIdő|1753-01-01 00:00:00.000 - 9999-12-31 23:59:59.997| Unicode ÉÉÉÉ-HH-NN óó:pp:ss[.nnn] karakterlánc formátum|
|DateTime2|0001-01-01 00:00:00.0000000 – 9999-12-31 23:59:59.9999999.| Unicode ÉÉÉÉ-HH-NN óó:pp:ss[.nnnnnnn] karakterlánc formátum|
|DateTimeOffset|0001-01-01 00:00:00.0000000 és 9999-12-31 23:59:59.9999999 között a koordinált világidő (UTC) időzónában| Unicode ÉÉÉÉ-HH-NN óó:pp:ss[.nnnnnnn] [{+|-}óó:pp] karakterlánc formátum|
|Tizedes|-1038 + 1-től 1038-ig – 1|Unicode karakterlánc formátum `Tizedes = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Lebegő|-1,79E+308-2,23E-308; 0; 2,23E-308-tól 1,79E+308-ig|Unicode karakterlánc-formátum|
|Kép|0 és 231 – 1 közötti bájtok sorozata (2 147 483 647)|hexadecimális kódolású Unicode karakterlánc formátum|
|Int|-231 (-2 147 483 648) – 231 – 1 (2 147 483 647)|Unicode karakterlánc-formátum|

## Hivatkozások

* [BCP-formátum – Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

