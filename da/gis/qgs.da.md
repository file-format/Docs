{
  "date": "2019-10-11",
  "keywords": [
"qgs fil",
"qgs filformat",
"hvad er en qgs-fil",
"fil",
"qgs eksempel",
"qgs filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QGS - QGIS Project File Format",
  "description": "Lær om QGS filformat og API'er, der kan oprette og åbne QGS filer.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en QGS fil?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS filformat

QGS-filer er i [XML](/web/xml/)-format og gemmer projektdata som XML-tags. En QGS-fil indeholder oplysninger som:

 * Projekt titel
 * projekt CRS
 * lagtræet
 * snapping-indstillinger
 * relationer
 * kortets lærreds udstrækning
 * projektmodeller
 * legende
 * mapview docks (2D og 3D)
 * lagene med links til de underliggende datasæt (datakilder) og andre lagegenskaber inklusive omfang, SRS, joins, typografier, renderer, blend mode, opacitet og mere.
 * projektejendomme

### QGS XML-tags på topniveau

{{< figure src="../qgstoplevel.png" title="" >}}

### Udvidede Top Level Project Layer Tags

{{< figure src="../qgstoplevel.png" title="" >}}

## Referencer

* [QGIS](https://www.qgis.org/en/site/)


