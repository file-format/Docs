{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "QGIS projekt Sqlite adatbázisa", "kiterjesztés", "formátum", "QGIS", "kiegészítő adatbázis", "Mi az a QGD fájl"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD – a QGIS projekt Sqlite adatbázisa",
  "description":"Tudjon meg többet a QGD-ről, amely a QGIS projekt sqlite adatbázisa, valamint az API-król, amelyek QGD fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Mi az a QGD fájl?

A .QGD kiterjesztésű fájl valójában a **QGIS** projekt társított sqlite adatbázisa, amely a projekt segédadatait tartalmazza. A QGD fájl üres marad, ha nem lesznek segédadatok a projekthez.

## Részletek a QGD fájlformátumról

Klasszikus módban a kiegészítő adatbázis .qgd kiterjesztésű fájlként kerül mentésre az xml fájl mellett. Az **Auxiliary Database** rendszer alternatív módon lehetővé teszi az adatok olvasását és írását a rendszerben. A QGZ létrehozásakor, amely egy tömörített tároló, a .qgd fájl belefoglalja a .qgz fájlba.

## Mi az a segédadatbázis?
A segédadatbázis valójában egy készenléti adatbázis-rendszer, amely a céladatbázis megkettőzésének válaszaként jön létre. A segédadatbázis valójában egy duplikált adatbázis esete, mint az az adatbázis, amelyre másol. Például, ha egy készenléti adatbázist állít be duplikált adatbázis használatával, akkor a forrás adatbázis lesz a cél, a készenléti adatbázis pedig a segéd.


## Hivatkozások

* [QGZ – A QGIS új alapértelmezett projektfájl-formátuma](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS fájlformátumok](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

