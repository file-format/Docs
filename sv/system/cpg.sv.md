{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG-filformat - ESRI-kodsidasfil",
  "description":"Läs mer om CPG-filformat och API:er som kan skapa och öppna CPG-filer.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Vad är en CPG fil?

En CPG-fil är en valfri fil som kräver ESRI Shapefile som används för att specificera teckentabellen för att identifiera teckenuppsättningen som ska användas. Dessa lagras i vanligt textfilformat och innehåller information om den kodning som används för att skapa shapefilen. Om en CPG-fil inte är tillgänglig använder shapefilen systemets standardkodning. En CPG-fil, om den finns, måste ha samma prefix som filen [SHP](/sv/gis/shp/), till exempel roads.shp, roads.cpg.

CPG-filer kan öppnas med ESRI ArcGIS Pro.

### CPG-filformat - Mer information

När du visar en shapefil i ArcCatalog eller någon annan ArcGIS-applikation ser du bara shapefilen. Men i verkligheten använder shapefile andra associerade filer som läses vid sidan av huvudformfilen. CPG-filen är också en av dessa om den finns tillsammans med SHP-huvudfilen.

## Referenser

* [Shapefile filtillägg
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

