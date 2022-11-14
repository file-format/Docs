{
  "date" : "2019-10-11",
  "keywords" :[ "qml file", "qml file format", "wat is een qml file", "file", "qml example", "qml file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - Het QGIS-stijlbestandsformaat",
  "description":"Meer informatie over QML-bestandsindeling en API's die QML-bestanden kunnen maken en openen.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Wat is een QML-bestand?

Een bestand met de extensie .qml is een XML-bestand dat informatie over de stijl van lagen voor QGIS-lagen opslaat. QGIS is een open-source platformonafhankelijke GIS-toepassing die wordt gebruikt om geospatiale gegevens weer te geven met de mogelijkheid om gegevens in de vorm van lagen te organiseren. QML-bestanden bevatten informatie die door QGIS wordt gebruikt om geometrieën van objecten weer te geven, inclusief symbooldefinities, afmetingen en rotaties, labels, dekking, overvloeimodus en nog veel meer. In tegenstelling tot de QLR-bestanden bevatten QML-bestanden alle stylinginformatie op zich. QML-bestanden kunnen worden geopend in elke teksteditor, zoals Notepad++.

## QML-bestandsindeling

QLR, vergelijkbaar met [QGS](/nl/gis/qgs/) en [QLR](/nl/gis/qlr/), is een XML-bestand dat stijlinformatie voor de lagen bevat.

De onderstaande afbeelding toont de tags op het hoogste niveau van een QML-bestand (met alleen renderer_v2 en de bijbehorende symbooltag uitgevouwen).

{{< figure src="../qml.png" title="" >}}

## Referenties

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

