{
  "date" : "2019-10-11",
  "keywords" :[ "qgs-bestand", "qgs-bestandsindeling", "wat is een qgs-bestand", "bestand", "qgs-voorbeeld", "qgs-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS Project-bestandsindeling",
  "description":"Meer informatie over QGS-bestandsindeling en API's die QGS-bestanden kunnen maken en openen.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een QGS-bestand?

Een bestand met de extensie .qgs is een projectbestand gemaakt met [QGIS](https://www.qgis.org/en/site/), wat een open-source platformonafhankelijke GIS-toepassing is. Alle projectinstellingen zoals laageigenschappen en hulpgegevens voor het project. Het wordt gemaakt wanneer een kaartproject op schijf wordt opgeslagen. Het is eigenlijk een configuratiebestand dat informatie vasthoudt zoals verwijzingen naar de GIS-gegevens, stylinginformatie over de lagen en projecttitel. QGS-bestanden kunnen worden geopend met QGIS-software die vrij beschikbaar is om te downloaden.

## QGS-bestandsindeling

QGS-bestanden hebben de indeling [XML](/nl/web/xml/) en slaan projectgegevens op als XML-tags. Een QGS-bestand bevat informatie zoals:

* project titel
* project CRS
* de lagenboom
* instellingen voor snappen
* relaties
* de omvang van het kaartcanvas
* projectmodellen
* legende
* mapview-docks (2D en 3D)
* de lagen met links naar de onderliggende datasets (gegevensbronnen) en andere laageigenschappen, waaronder omvang, SRS, joins, stijlen, renderer, overvloeimodus, dekking en meer.
* projecteigenschappen

### QGS XML-tags op het hoogste niveau

{{< figure src="../qgstoplevel.png" title="" >}}

### Uitgebreide tags voor projectlagen op het hoogste niveau

{{< figure src="../qgstoplevel.png" title="" >}}

## Referenties

* [QGIS](https://www.qgis.org/en/site/)

