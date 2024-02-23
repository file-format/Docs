{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik SDF — plik w formacie danych przestrzennych",
  "description":"Dowiedz się o formacie pliku SDF i interfejsach API, które umożliwiają tworzenie i otwieranie plików SDF.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf-pl",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Co to jest plik SDF?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. Jest uważany za zoptymalizowany format pliku dla dużych zbiorów danych informacji przestrzennej.

Plik SDF można otworzyć za pomocą programów Autodesk AutoCAD Map 3D 2022 i Autodesk AutoCAD Civil 3D 2023.

## Format pliku SDF — więcej informacji

Pliki w formacie SDF są zapisywane na dysku jako pliki binarne. Opiera się na bazie danych SQLite, która wykorzystuje komponenty pamięci niskiego poziomu do binarnej serializacji danych. Plik SDF zawiera wiele klas elementów na plik i wiele właściwości geometrii dla każdej klasy elementów. Dane w pliku SDF są dostępne z dużą szybkością dzięki indeksowaniu każdej właściwości geometrii przy użyciu drzewa R.

## Bibliografia

* [Format danych SDF](https://en.wikipedia.org/wiki/Spatial_Data_File)

* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

