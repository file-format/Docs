{
  "date" : "2019-10-11",
  "keywords" :[ "qlr-bestand", "qlr-bestandsindeling", "wat is een qlr-bestand", "bestand", "qlr-voorbeeld", "qlr-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS Layer Definition File",
  "description":"Meer informatie over QLR-bestandsindelingen en API's die QLR-bestanden kunnen maken en openen.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Wat is een QLR-bestand?

Een bestand met .qlr is een Layer Definition-bestand dat een verwijzing naar de laaggegevensbron bevat. Dit is een aanvulling op de [QGIS](https://www.qgis.org/en/site/) stijlinformatie voor de laag. Met verwijzingen naar alle gerelateerde stijlen, wordt dit bestand gebruikt als een enkele bron voor gegevens die moeten worden gebruikt voor het verkrijgen van de stijlinformatie. Met behulp van de QLR-bestanden kan informatie naar de gegevensbronnen in dit enkele bestand worden geplaatst dat door andere toepassingen kan worden gelezen om de stijlinformatie te laden. QLR-bestanden kunnen worden geopend met elke teksteditor zoals Notepad++.

## QLR-bestandsindeling

QLR, vergelijkbaar met [QGS](/nl/gis/qgs/), is een XML-bestand dat verwijzingen naar laaggegevensbronnen bevat in de vorm van XML-tags. Het is vergelijkbaar met het ArcGIS .lyr-bestand. De tags op het hoogste niveau van een QML-bestand zijn zoals weergegeven in de onderstaande afbeelding.

{{< figure src="../qlr.png" title="" >}}

## Referenties

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

