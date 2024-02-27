{
  "date": "2019-10-11",
  "keywords": [
"qlr fil",
"qlr filformat",
"hvad er en qlr-fil",
"fil",
"qlr eksempel",
"qlr filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QLR - QGIS Layer Definition File",
  "description": "Lær om QLR filformat og API'er, der kan oprette og åbne QLR filer.",
  "linktitle": "QLR",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-ql-dar"
}
},
  "lastmod": "2021-03-14"
}

## Hvad er en QLR fil?

En fil med .qlr er en Layer Definition-fil, der indeholder en pointer til lagdatakilden. Dette er et supplement til [QGIS](https://www.qgis.org/en/site/)-stilinformationen for laget. Med referencer til alle relaterede stilarter bruges denne fil som en enkelt kilde til data, der skal bruges til at få stilinformationen. Ved at bruge QLR-filerne kan information til datakilderne lægges i denne enkelte fil, som kan læses af andre applikationer for at indlæse stylinginformationen. QLR-filer kan åbnes med en hvilken som helst teksteditor, såsom Notepad++.

## QLR filformat

QLR, der ligner [QGS](/gis/qgs/), er en XML-fil, der indeholder pointere til lagdatakilden i form af XML-tags. Den ligner ArcGIS .lyr-fil. Taggene på øverste niveau i en QML-fil er som vist på billedet nedenfor.

{{< figure src="../qlr.png" title="" >}}

## Referencer

* [QGIS](https://www.qgis.org/en/site/)

* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

