{
  "date" : "2019-10-11",
  "keywords" :[ "qlr-fil", "qlr-filformat", "vad är en qlr-fil", "fil", "qlr-exempel", "qlr-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS Layer Definition File",
  "description":"Läs mer om QLR-filformat och API:er som kan skapa och öppna QLR-filer.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Vad är en QLR fil?

En fil med .qlr är en lagerdefinitionsfil som innehåller en pekare till lagerdatakällan. Detta är utöver stilinformationen för [QGIS](https://www.qgis.org/en/site/) för lagret. Med referenser till alla relaterade stilar, används den här filen som en enda källa för data som ska användas för att hämta stilinformationen. Med hjälp av QLR-filerna kan information till datakällorna läggas i denna enda fil som kan läsas av andra applikationer för att ladda stylinginformationen. QLR-filer kan öppnas med vilken textredigerare som helst som Notepad++.

## QLR filformat

QLR, liknande [QGS](/sv/gis/qgs/), är en XML-fil som innehåller pekare till lagerdatakälla i form av XML-taggar. Den liknar ArcGIS .lyr-fil. Toppnivåtaggarna för en QML-fil är som visas i bilden nedan.

{{< figure src="../qlr.png" title="" >}}

## Referenser

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

