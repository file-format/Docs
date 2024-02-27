{
  "date": "2021-03-18",
  "author": {
    "display_name": "Muhammad Umar",
    "keywords": [
"QGD",
"QGIS-projektets SQL-database",
"udvidelse",
"format",
"QGIS",
"Hjælpedatabase",
"Hvad er en QGD fil"
]
},
  "draft": "false",
  "toc": true,
  "title": "QGD - SQLite-database for QGIS-projektet",
  "description": "Lær om QGD, som er en sqlite-database over QGIS-projektet og API'er, der kan oprette og åbne QGD-filer.",
  "linktitle": "QGD",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-dad"
}
},
  "lastmod": "2021-03-18"
}

## Hvad er en QGD fil?

Filen med filtypenavnet .QGD er faktisk den tilknyttede sqlite-database for **QGIS**-projektet, der rummer hjælpedata for projektet. QGD-filen forbliver tom, hvis der ikke vil være nogen hjælpedata for projektet.

## Detaljer om QGD-filformat

I klassisk tilstand gemmes hjælpedatabasen som en fil med filtypenavnet .qgd langs xml-filen. **Auxiliary Database**-systemet gør det muligt at læse og skrive data i systemet som en alternativ måde. Når du opretter QGZ, som er en zippet container, inkluderer .qgd-filen .qgz.

## Hvad er Auxilary Database?
Hjælpedatabasen er faktisk et standby-db-system, der er oprettet som et svar på duplikeringen af måldatabasen. Hjælpedatabasen er faktisk et tilfælde af en duplikatdatabase ville være den database, du duplikerer til. Hvis du f.eks. opsætter en standby-database ved hjælp af duplikatdatabase, vil kildedatabasen være målet, og standby-databasen vil blive kendt som auxiliary.


## Referencer

* [QGZ – Et nyt standardprojektfilformat til QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

