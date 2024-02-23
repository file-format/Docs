{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF-fil - Fil för rumslig dataformat",
  "description":"Lär dig om SDF-filformat och API:er som kan skapa och öppna SDF-filer.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-sv",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Vad är en SDF fil?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Det anses vara ett optimerat filformat för stora datamängder med rumslig information.

Du kan öppna en SDF-fil med Autodesk AutoCAD Map 3D 2022 och Autodesk AutoCAD Civil 3D 2023.

## SDF-filformat - Mer information

SDF-filformat lagras på skivan som binära filer. Den är baserad på SQLite-databasen som använder lågnivålagringskomponenter för binär serialisering av data. En SDF-fil innehåller flera funktionsklasser per fil och flera geometriegenskaper för varje funktionsklass. Data i en SDF-fil är tillgänglig med hög hastighet på grund av indexering av varje geometriegenskap med hjälp av ett R-träd.

## Referenser

* [SDF Data Format](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

