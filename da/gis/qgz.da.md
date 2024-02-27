{
  "date": "2021-03-18",
  "keywords": [
"qgz fil",
"qgz filformat",
"hvad er en qgz fil",
"fil",
"qgz eksempel",
"qgz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "QGZ - Quantum GIS Compressed Project",
  "description": "Lær om QGZ filformat, som blot er en komprimeret QGS og API'er, der kan oprette og åbne QGZ filer.",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-daz"
}
},
  "lastmod": "2021-03-18"
}

## Hvad er en QGZ fil?

Filformatet **QGZ** er et komprimeret arkiv, der indeholder en [QGS](/gis/qgs/)-fil og en QGD-fil. Hvorimod QGD-filen er qgis-projektets sqlite-database, der består af hjælpedata til projektet. Hvis der ikke er nogen hjælpedata, forbliver QGD-filen tom.

## Detaljer om QGZ filformat

QGZ blev introduceret som en ny variant af **QGIS 3-projektfilformatet**. Dette format er en zippet container til QGS xml-filen. Hvis brugere vælger QGD, der er et valgfrit format, er containeren i dette tilfælde en fordel til at gemme den ekstra lagerdatabase.

I klassisk tilstand gemmes hjælpedatabasen som en fil med filtypenavnet .qgd langs xml-filen. Når du vælger den zippede container, inkluderer .qgd-filen i .qgz. Det letter bare brugerne uden problemer, brugerne kan ikke slette det eller glemme at kopiere det, når de deler projektfiler!


## Referencer

* [QGZ – Et nyt standardprojektfilformat til QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

