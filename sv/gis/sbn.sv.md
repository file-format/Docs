{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - ESRI Spatial Index Binary File",
  "description":"Läs mer om SBN-filformat och API:er som kan skapa och öppna SBN-filer.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Vad är en SBN fil?

En fil med filtillägget .sbn är en rumslig indexfil som är associerad med filen ESRI ArcGIS [.shp](/sv/gis/shp/). Det används för att optimera rumsliga frågor när ett index har utförts på data. Den andra filtypen som används tillsammans med .sbn är .sbx-filen. SBN- och SBX-filerna utgör tillsammans ett formindex för att påskynda rumsliga frågor. SBN-filer är valfria och kan öppnas med [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## SBN-filformat - Mer information

SBN-filer lagras på skiva som binära filer och information om deras interna filformat är inte tillgänglig. Dessa lagrar den binära representationen av en SHP-fil för rumsliga frågor. SBX-indexfilen används tillsammans med SBN-filerna för att påskynda de rumsliga frågorna på shapefiler.

## Referenser

* [ESRI ShapeFile teknisk beskrivning](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

