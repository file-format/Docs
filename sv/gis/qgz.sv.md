{
  "date" : "2021-03-18",
  "keywords" :[ "qgz fil", "qgz filformat", "vad är en qgz fil", "fil", "qgz exempel", "qgz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS Compressed Project",
  "description":"Lär dig om QGZ-filformat som bara är en komprimerad QGS och API:er som kan skapa och öppna QGZ-filer.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Vad är en QGZ fil?

Filformatet **QGZ** är ett komprimerat arkiv som innehåller en [QGS](/gis/qgs/) fil och en QGD-fil. Medan QGD-filen är SQLite-databasen för qgis-projektet som består av hjälpdata för projektet. Om det inte finns några extra data kommer QGD-filen att förbli tom.

## Detaljer om QGZ-filformat

QGZ introducerades som en ny variant av **QGIS 3-projektfilformatet**. Detta format är en zippad behållare för QGS xml-filen. Om användare väljer QGD som är ett valfritt format, är behållaren i detta fall fördelaktig för att lagra den extra lagringsdatabasen.

I klassiskt läge sparas den extra databasen som en fil med filtillägget .qgd längs xml-filen. När du väljer den zippade behållaren, ingår .qgd-filen i .qgz. Det underlättar bara användarna utan problem, användarna kan inte ta bort det eller glömma att kopiera det när de delar projektfiler!


## Referenser

* [QGZ – Ett nytt standardprojektfilformat för QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS-filformat](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

