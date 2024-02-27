{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF-fil - Geografisk dataformatfil",
  "description":"Lær om SDF-filformat og API'er, der kan oprette og åbne SDF-filer.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-da",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Hvad er en SDF fil?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Det betragtes som et optimeret filformat til store datasæt af rumlig information.

Du kan åbne en SDF-fil ved hjælp af Autodesk AutoCAD Map 3D 2022 og Autodesk AutoCAD Civil 3D 2023.

## SDF-filformat - flere oplysninger

SDF-filformatet gemmes på disken som binære filer. Den er baseret på SQLite-databasen, der bruger lagerkomponenter på lavt niveau til binær serialisering af data. En SDF-fil indeholder flere funktionsklasser pr. fil og flere geometriegenskaber for hver funktionsklasse. Data i en SDF-fil er tilgængelig med høj hastighed på grund af indeksering af hver geometriegenskab ved hjælp af et R-træ.

## Referencer

* [SDF-dataformat](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

