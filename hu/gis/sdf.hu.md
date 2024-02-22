{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF fájl – Téradat-formátumfájl",
  "description":"Ismerje meg az SDF fájlformátumot és az API-kat, amelyek SDF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-hu",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Mi az SDF fájl?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Úgy tekintik, mint egy optimalizált fájlformátumot nagy térinformációs adatkészletekhez.

Az SDF fájlokat az Autodesk AutoCAD Map 3D 2022 és az Autodesk AutoCAD Civil 3D 2023 segítségével nyithatja meg.

## SDF fájlformátum - További információ

Az SDF fájlformátumok bináris fájlokként kerülnek a lemezre. Az SQLite adatbázison alapul, amely alacsony szintű tárolási összetevőket használ az adatok bináris szerializálásához. Egy SDF-fájl fájlonként több jellemzőosztályt és minden jellemzőosztályhoz több geometriai tulajdonságot tartalmaz. Az SDF-fájlban lévő adatok nagy sebességgel érhetők el az egyes geometriai tulajdonságok R-fa segítségével történő indexelésének köszönhetően.

## Hivatkozások

* [SDF adatformátum](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

