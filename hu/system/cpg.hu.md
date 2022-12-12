{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG fájlformátum - ESRI kódlapfájl",
  "description":"További információ a CPG fájlformátumról és az API-król, amelyek CPG-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Mi az a CPG fájl?

A CPG-fájl egy olyan opcionális fájl, amelyre az ESRI Shapefile-re van szükség, amely a használandó karakterkészlet azonosítására szolgáló kódlap megadására szolgál. Ezek egyszerű szöveges fájlformátumban vannak tárolva, és információkat tartalmaznak a shapefile létrehozásához alkalmazott kódolásról. Ha egy CPG fájl nem érhető el, akkor a shapefile a rendszer alapértelmezett kódolását használja. A CPG-fájlnak, ha van, ugyanazzal az előtaggal kell rendelkeznie, mint az [SHP](/hu/gis/shp/) fájlban, például roads.shp, roads.cpg.

A CPG-fájlok az ESRI ArcGIS Pro segítségével nyithatók meg.

### CPG fájlformátum - További információ

Ha egy shape fájlt tekint meg az ArcCatalogban vagy bármely más ArcGIS alkalmazásban, akkor csak a shapefile látható. A valóságban azonban a shapefile más társított fájlokat használ, amelyek a fő shape fájl mellett kerülnek beolvasásra. A CPG-fájl is ezek közé tartozik, ha a fő SHP-fájl mellett található.

## Hivatkozások

* [Shapefile fájlkiterjesztések
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

