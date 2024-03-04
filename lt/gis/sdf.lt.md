{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SDF failas – erdvinių duomenų formato failas",
  "description":"Sužinokite apie SDF failo formatą ir API, kurios gali kurti ir atidaryti SDF failus.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Kas yra SDF failas?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Jis laikomas optimizuotu failo formatu dideliems erdvinės informacijos duomenų rinkiniams.

SDF failą galite atidaryti naudodami Autodesk AutoCAD Map 3D 2022 ir Autodesk AutoCAD Civil 3D 2023.

## SDF failo formatas – daugiau informacijos

SDF failo formatas yra saugomas diske kaip dvejetainiai failai. Jis pagrįstas SQLite duomenų baze, kuri naudoja žemo lygio saugojimo komponentus dvejetainiam duomenų serializavimui. SDF faile yra kelios elementų klasės viename faile ir kelios kiekvienos elementų klasės geometrijos ypatybės. Duomenis SDF faile galima pasiekti dideliu greičiu, nes kiekviena geometrijos ypatybė indeksuojama naudojant R medį.

## Nuorodos

* [SDF duomenų formatas](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

