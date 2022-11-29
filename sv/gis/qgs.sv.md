{
  "date" : "2019-10-11",
  "keywords" :[ "qgs-fil", "qgs-filformat", "vad är en qgs-fil", "fil", "qgs-exempel", "qgs-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS Project File Format",
  "description":"Läs mer om QGS-filformat och API:er som kan skapa och öppna QGS-filer.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en QGS fil?

En fil med .qgs-tillägget är en projektfil som skapats med [QGIS](https://www.qgis.org/en/site/), som är en öppen källkod för plattformsoberoende GIS-applikation. Alla projektinställningar såsom lageregenskaper och hjälpdata för projektet. Det skapas när ett kartprojekt sparas på skiva. Det är faktiskt en konfigurationsfil som behåller information som pekare till GIS-data, stilinformation om lagren och projekttitel. QGS filer kan öppnas med QGIS programvara som är fritt tillgänglig att ladda ner.

## QGS filformat

QGS-filer är i formatet [XML](/sv/web/xml/) och lagrar projektdata som XML-taggar. En QGS-fil innehåller information som:

* Projekt Titel
* projekt CRS
* lagerträdet
* Snäppinställningar
* relationer
* kartan kanvas omfattning
* projektmodeller
* legend
* mapview dockor (2D och 3D)
* lagren med länkar till de underliggande datamängderna (datakällor) och andra lageregenskaper inklusive utsträckning, SRS, sammanfogningar, stilar, renderare, blandningsläge, opacitet och mer.
* projektegenskaper

### QGS toppnivå XML-taggar

{{< figure src="../qgstoplevel.png" title="" >}}

### Utökade projektlagertaggar på toppnivå

{{< figure src="../qgstoplevel.png" title="" >}}

## Referenser

* [QGIS](https://www.qgis.org/en/site/)

