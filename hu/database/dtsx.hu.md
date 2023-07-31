{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DTSX fájlformátumról és az API-król, amelyek DTSX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DTSX fájlformátum - SQL Server DTS beállítási fájl",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az a DTSX fájl?

A .dtsx (Data Transformation Services Package XML) kiterjesztésű fájl egy Data Transformation Services (DTS) fájl, amelyet a Microsoft SQL használ az adatmigráció lépéseire/szabályaira az adatok egyik adatbázisból a másikba való átviteléhez. Ez magában foglalja az átalakításokat és az opcionális feldolgozási lépéseket, amelyek a kiindulási és célpontok közötti adatátvitel során szükségesek lehetnek. Az SQL Server Integration Services (SSIS), a Microsoft SQL Server egyik összetevője, a DTSX fájlokat használja az adatbázis-kiszolgálók közötti adatfeldolgozás lépéseinek azonosítására. A DTSX fájlok a Microsoft SQL Server 2019 programmal nyithatók meg.

## DTSX fájlformátum

Az adatbázis-kiszolgálók közötti adatmozgás szabályokat és feldolgozási lépéseket igényel az adatok integritásának biztosításához a művelet során. Az SSIS biztosítja, hogy mindezek a tevékenységek, amelyek célja a különböző forrásokból származó adatok áthelyezése és összehangolása egy vállalaton belül, kényelmesen történjen. Itt jön a DTSX, amely meghatározza az SSIS által használandó struktúrákat, hogy meghatározza azokat a lépéseket, amelyekben az adatok feldolgozhatók, ahogy az ezeken a lépéseken keresztül következik.

A DTSX által leírt adatfolyam a következő képen látható.

{{< figure src="../DataFlowDTSX.png" alt="Adatfolyam DTSX" >}}

A DTSX [XML](/hu/web/xml/) alapú, és az [MS-DTSX]-ben van dokumentálva (https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). A DTSX XML továbbfejlesztett átalakítása a DTSX 2.0, amely új attribútumokat tartalmaz a struktúrákhoz, a megnevezett tulajdonságok szülő XML-attribútumként való cseréjét, a legtöbb attribútumérték alapértelmezett értékét, valamint az ismétlődő elemek szülőelemen belüli elhelyezését. A DTSX-struktúrák leírása ezekkel az [XML-sémákkal](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) cellar-text XML.

## Hivatkozások

* [DTSX formátum – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2 formátum – a Microsofttól](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

