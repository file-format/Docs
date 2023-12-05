{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSF fájl – GeoMedia koordinátarendszer fájlformátuma",
  "description":"További információ a CSF-fájlformátumról és az API-król, amelyek CSF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## Mi az a CSF fájl?

A CSF-fájl egy koordinátarendszer-fájl, amely egy GIS-fájl koordináta-rendszeréről tartalmaz információkat. Az Intergraph GeoMedia szoftvere egy adott koordináta-rendszer paramétereinek meghatározására használja. Ide tartoznak az olyan információs paraméterek, mint a nullapont, a vetítés és a mértékegységek. Ezt az információt a koordinátarendszerrel nem rendelkező kimeneti adatok térképeinek előállítására használják. A GeoMedia ezeket az információkat használja fel a földrajzi adatok megfelelő koordinátarendszerben történő helyes megjelenítésére és kezelésére.

## CSF fájlformátum

A CSF-fájlok szöveges fájlként kerülnek tárolásra a földrajzi koordináta-rendszer részleteivel. A GeoMedia lehetővé teszi a földrajzi információs fájlok importálását olyan bemeneti adatokból, amelyeknek nincs meghatározott koordinátarendszere. A vetületi és koordinátarendszer segítségével a térinformatikai rendszerek pontos értékekkel jelenítik meg a térképfájlt. A CSF-fájl ugyanazon a helyen jön létre, mint a kimeneti fájl.

## Hivatkozások

* [Hogyan jeleníti meg vagy szolgálja ki helyesen a shapefile adatokat a GeoMediában?
](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)

