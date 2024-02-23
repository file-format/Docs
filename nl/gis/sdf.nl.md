{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF-bestand - Bestand voor ruimtelijke gegevensindeling",
  "description":"Meer informatie over de SDF-bestandsindeling en API's waarmee SDF-bestanden kunnen worden gemaakt en geopend.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-nl",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Wat is een SDF-bestand?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Het wordt beschouwd als een geoptimaliseerd bestandsformaat voor grote datasets met ruimtelijke informatie.

U kunt een SDF-bestand openen met Autodesk AutoCAD Map 3D 2022 en Autodesk AutoCAD Civil 3D 2023.

## SDF-bestandsindeling - Meer informatie

Het SDF-bestandsformaat wordt als binaire bestanden op schijf opgeslagen. Het is gebaseerd op de SQLite-database die opslagcomponenten op laag niveau gebruikt voor binaire serialisatie van gegevens. Een SDF-bestand bevat meerdere featureklassen per bestand en meerdere geometrie-eigenschappen voor elke featureklasse. Gegevens in een SDF-bestand zijn met hoge snelheid toegankelijk dankzij de indexering van elke geometrie-eigenschap met behulp van een R-boom.

## Referenties

* [SDF-gegevensformaat](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

