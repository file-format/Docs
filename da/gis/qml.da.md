{
  "date": "2019-10-11",
  "keywords": [
"qml fil",
"qml filformat",
"hvad er en qml-fil",
"fil",
"qml eksempel",
"qml filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QML - QGIS-stilfilformatet",
  "description": "Lær om QML filformat og API'er, der kan oprette og åbne QML filer.",
  "linktitle": "QML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qm-dal"
}
},
  "lastmod": "2021-03-14"
}

## Hvad er en QML fil?

En fil med .qml-udvidelsen er en XML-fil, der gemmer lagstilingsoplysninger for QGIS-lag. QGIS er en open source GIS-applikation på tværs af platforme, der bruges til at vise geospatiale data med evnen til at organisere data i form af lag. QML-filer indeholder information, der bruges af QGIS til at gengive funktionsgeometrier, herunder symboldefinitioner, størrelser og rotationer, mærkning, opacitet, blandingstilstand og meget mere. I modsætning til QLR-filerne indeholder QML-filer alle stylingoplysningerne i sig selv. QML-filer kan åbnes i enhver teksteditor, såsom Notepad++.

## QML filformat

QLR, i lighed med [QGS](/gis/qgs/) og [QLR](/gis/qlr/), er en XML-fil, der indeholder stilinformation for lagene.

Figuren nedenfor viser tags på øverste niveau for en QML-fil (med kun renderer_v2 og dens symboltag udvidet).

{{< figure src="../qml.png" title="" >}}

## Referencer

* [QGIS](https://www.qgis.org/en/site/)

* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

