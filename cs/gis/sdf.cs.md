{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor SDF – soubor ve formátu prostorových dat",
  "description":"Přečtěte si o formátu souboru SDF a rozhraních API, která mohou vytvářet a otevírat soubory SDF.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-cs",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Co je soubor SDF?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Je považován za optimalizovaný formát souboru pro velké datové sady prostorových informací.

Soubor SDF můžete otevřít pomocí aplikací Autodesk AutoCAD Map 3D 2022 a Autodesk AutoCAD Civil 3D 2023.

## Formát souboru SDF – Další informace

Soubory ve formátu SDF se ukládají na disk jako binární soubory. Je založen na databázi SQLite, která využívá nízkoúrovňové úložné komponenty pro binární serializaci dat. Soubor SDF obsahuje více tříd prvků na soubor a více vlastností geometrie pro každou třídu prvků. Data v souboru SDF jsou přístupná vysokou rychlostí díky indexování každé vlastnosti geometrie pomocí R-stromu.

## Reference

* [Datový formát SDF](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

