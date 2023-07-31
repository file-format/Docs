{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DACPAC fájlformátumról és az API-król, amelyek DACPAC fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DACPAC – Data Tier AppliCation Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Mi az a DACPAC fájl?

A .dacpac kiterjesztésű fájl (a Data Tier AppliCation Package rövidítése) olyan adatbázisfájl, amelyet a Microsoft SQL Server adatréteg-alkalmazással hoztak létre, és amely tartalmazza az adatbázis-objektumok ábrázolására szolgáló adatbázismodellt. Mivel az adatbázis teljes modelljét tartalmazza, a modellben elérhető adatokból egy adatbázis visszaállítására szolgál. A DACPAC fájlokat rendszerint átadják a telepítési csoportoknak, hogy az adatbázis visszaállítása érdekében az ügyfél telephelyén telepítsék őket. Ezekkel lehet kinyitni
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30-TSzwSc0BB-XSp30B6cXjwopx06pYts89B6cXjwoxi =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## DACPAC fájlformátum – További információ

A DACPAC-adatcsomag-fájlok valójában tömörített ZIP-fájlok, amelyek több [XML](/hu/web/xml/) fájlt tartalmaznak, amelyek az adatbázis-modellre vonatkozó információkat tartalmaznak, például táblákat és nézeteket, amelyeket az adatbázis visszaállításához használnak. A DACPAC-fájlok tartalmának megtekintéséhez nevezze át a fájlokat .dacpac-ról [.zip](/hu/compression/zip/) névre, és bontsa ki a zip-archívumot bármely kicsomagoló segédprogrammal.

Az alábbiakban néhány olyan fájl található, amelyek a DACPAC-fájlban találhatók.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* modell.xml

Meg kell jegyezni, hogy a DACPAC nem tartalmaz DATA-t és egyéb szerverszintű objektumokat. A fájl tartalmazhat minden olyan objektumtípust, amely az SSDT projektben tárolható.

## Hivatkozások

* [Data Tier Applications – Előnyök](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Adatszintű alkalmazás telepítése – Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Hogyan hozhatunk létre DACPAC-fájlt?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

