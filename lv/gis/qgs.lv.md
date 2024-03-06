{
  "date": "2019-10-11",
  "keywords": [
"qgs fails",
"qgs faila formāts",
"kas ir qgs fails",
"failu",
"qgs piemērs",
"qgs faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QGS — QGIS projekta faila formāts",
  "description": "Uzziniet par QGS faila formātu un API, kas var izveidot un atvērt QGS failus.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir QGS fails?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS faila formāts

QGS faili ir [XML](/web/xml/) formātā un glabā projektu datus kā XML tagus. QGS fails satur tādu informāciju kā:

 * projekta nosaukums
 * projekts DRS
 * slāņu koks
 * fiksēšanas iestatījumi
 * attiecības
 * kartes audekla apjoms
 * projektu modeļi
 * leģenda
 * kartes skata doki (2D un 3D)
 * slāņi ar saitēm uz pamatā esošajām datu kopām (datu avotiem) un citiem slāņa rekvizītiem, ieskaitot apjomu, SRS, savienojumus, stilus, renderētāju, sajaukšanas režīmu, necaurredzamību un citus.
 * projekta īpašības

### QGS augstākā līmeņa XML tagi

{{< figure src="../qgstoplevel.png" title="" >}}

### Paplašināti augstākā līmeņa projektu slāņa tagi

{{< figure src="../qgstoplevel.png" title="" >}}

## Atsauces

* [QGIS](https://www.qgis.org/en/site/)


