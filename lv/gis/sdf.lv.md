{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF fails — telpisko datu formāta fails",
  "description":"Uzziniet par SDF failu formātu un API, kas var izveidot un atvērt SDF failus.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Kas ir SDF fails?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Tas tiek uzskatīts par optimizētu faila formātu lielām telpiskās informācijas datu kopām.

SDF failu var atvērt, izmantojot Autodesk AutoCAD Map 3D 2022 un Autodesk AutoCAD Civil 3D 2023.

## SDF faila formāts — vairāk informācijas

SDF failu formāti tiek saglabāti diskā kā bināri faili. Tā ir balstīta uz SQLite datu bāzi, kas izmanto zema līmeņa krātuves komponentus datu binārajai serializācijai. SDF fails satur vairākas objektu klases katrā failā un vairākus ģeometrijas rekvizītus katrai objektu klasei. Dati SDF failā ir pieejami lielā ātrumā, jo tiek indeksēts katrs ģeometrijas rekvizīts, izmantojot R-koku.

## Atsauces

* [SDF datu formāts](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

