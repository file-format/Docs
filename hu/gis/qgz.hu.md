{
  "date" : "2021-03-18",
  "keywords" :[ "qgz fájl", "qgz fájlformátum", "mi az a qgz fájl", "fájl", "qgz példa", "qgz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS Compressed Project",
  "description":"Tudjon meg többet a QGZ fájlformátumról, amely csak egy tömörített QGS, és API-król, amelyek QGZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Mi az a QGZ fájl?

A **QGZ** fájlformátum egy tömörített archívum, amely egy [QGS](https://docs.fileformat.com/gis/qgs/) fájlt és egy QGD fájlt tartalmaz. Ezzel szemben a QGD fájl a qgis projekt sqlite adatbázisa, amely a projekthez tartozó segédadatokat tartalmazza. Ha nincsenek segédadatok, a QGD fájl üres marad.

## Részletek a QGZ fájlformátumról

A QGZ a **QGIS 3 projektfájl formátum** új változataként jelent meg. Ez a formátum a QGS xml fájl tömörített tárolója. Ha a felhasználók a QGD-t választják, amely opcionális formátum, ebben az esetben a konténer előnyös a kiegészítő tárolási adatbázis tárolására.

Klasszikus módban a kiegészítő adatbázis .qgd kiterjesztésű fájlként kerül mentésre az xml fájl mellett. A zip konténer kiválasztásakor a .qgd fájl bekerül a .qgz-be, csak gond nélkül megkönnyíti a felhasználókat, a felhasználók nem tudják törölni vagy elfelejteni másolni projektfájlok megosztásánál!


## Hivatkozások

* [QGZ – A QGIS új alapértelmezett projektfájl-formátuma](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS fájlformátumok](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

