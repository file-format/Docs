{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL – Jelentésdefiníciós nyelvi fájl",
  "keywords" :[ "rdl", "jelentésdefiníciós nyelv", "XmlTextWriter", "XSD", "RDL elem"],
  "description":"További információ az RDL fájlformátumról, amely az SQL Server Reporting Services jelentésdefiníciójának XML-képe.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Mi az RDL fájl? ##

Az RDL (Report Definition Language) a Microsoft által a jelentések meghatározásához beállított referenciaérték. Egy RDL fájl egy vagy több RDL elemből áll. Míg egy RDL elem adattípusából és számosságából áll. Egy elem lehet egyszerű vagy összetett. Az egyszerű elemnek nincs gyermekeleme vagy attribútuma, míg az összetett elemnek vannak gyermekei és opcionális attribútumai.

## RDL XML séma definíció
Egy XML Schema Definition (XSD) fájl érvényesíti az RDL fájlt. A séma határozza meg a szabályokat arra vonatkozóan, hogy az RDL elemek hol fordulhatnak elő egy .rdl fájlban. Egy RDL elem lehet egyszerű vagy összetett. Egy egyszerű elemnek nincsenek gyermekelemei vagy attribútumai, az összetett elemeknek pedig vannak gyermekei és opcionálisan attribútumai.

## RDL létrehozása
Mivel az RDL nyílt és bővíthető természetű, sok olyan alkalmazás és eszköz készíthető, amelyek az XML-séma alapján RDL fájlokat generálnak. Az RDL alkalmazásból való létrehozásának egyik legegyszerűbb módja a **System.Xml** névtér és a System.Linq névtér Microsoft .NET Framework osztályainak használata. Különösen az **XmlTextWriter** osztály használható RDL írására. Az **XmlTextWriter** használatával létrehozhat egy teljes jelentésdefiníciót az elejétől a végéig bármely .NET Framework alkalmazásban. A fejlesztők egyéni jelentéselemeket is hozzáadhatnak egyéni tulajdonságokkal az RDL kiterjesztése érdekében.

## RDL típusok
Az alábbi táblázat felsorolja az RDL elemekben használt típusokat és attribútumokat.

|Típus|Leírás|
---|---|
|Bináris |Tulajdonság 64-es kódolású bináris értékkel.|
|Logi| Tulajdonság, amelynek értéke igaz vagy hamis. Ha nincs másképp megadva, a kihagyott opcionális logikai objektumok értéke False.|
|Dat
|Enum |Olyan tulajdonság egy karakterlánc-szöveg értékkel, amelynek a kijelölt értékek listájának egyikének kell lennie.|
|Lebegő |Lebegő értékű ingatlan. Egy pontot (.) használunk opcionális decimális elválasztóként.|
|Integer |Egy tulajdonság egész (int32) értékkel.|
|Nyelv |Olyan tulajdonság, amelynek szövegértéke nyelvi és kulturális kódot tartalmaz, például "en-us" az amerikai angolhoz. Az értéknek egy adott nyelvnek vagy egy semleges nyelvnek kell lennie, amelyhez alapértelmezett nyelv van definiálva a Microsoft .NET-keretrendszerben.|
|Név |Szövegértékkel rendelkező tulajdonság. A neveknek egyedinek kell lenniük az elem névterében. Ha nincs megadva, akkor az elem névtere a legbelső olyan objektum, amelynek neve van.|
|NormalizedString |Normalizált karakterlánc-értékkel rendelkező tulajdonság.|
|Méret |A méretelemnek tartalmaznia kell egy számot (a pont karakterrel, amely opcionális decimális elválasztóként használható). A számot a CSS hosszmértékegység jelölésének kell követnie, például cm, mm, in, pt vagy pc. A szám és a jelölő között szóköz nem kötelező. A méretjelzőkkel kapcsolatos további információkért lásd a CSS-értékek és mértékegységek hivatkozását. Az RDL-ben a Méret maximális értéke 160 hüvelyk. A minimális méret 0 hüvelyk.|
|String |Karakterlánc szövegértékkel rendelkező tulajdonság.|
|UnsignedInt |Egy tulajdonság előjel nélküli egész (uint32) értékkel.|
|Változat |Bármilyen egyszerű XML-típusú tulajdonság.|

## RDL adattípusok
Az RDL-ben a DataType Enumeration határozza meg egy attribútum, kifejezés vagy paraméter adattípusát. Az alábbi táblázat bemutatja, hogy a CLR adattípusok hogyan felelnek meg az RDL adattípusoknak.

|CLR típus(ok) |Megfelelő adattípus|
---|---|
|Logi| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Egyágyas, Dupla |Úszó|
|Karakterlánc, Char, GUID, Időtartam |Karakterlánc|


## Hivatkozások ##

- [A jelentés definíciójának nyelve (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Jelentésdefiníciós nyelv (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

