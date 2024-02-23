{
  "date": "2022-12-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DT0 fil - DTED nivå 0 filformat",
  "description": "Lär dig om DT0-filformat och API:er som kan skapa och öppna DT0-filer.",
  "linktitle": "DT0",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dt-sv0"
}
},
  "lastmod": "2022-12-07"
}

## Vad är DT0 fil?

En DT0-fil är en DTED-fil (Digital Terrain Elevation Data) som innehåller nivå 0-information för att studera terränghöjdsdata. Höjddata är jämnt fördelade i en DT0-fil och kan läsas av populära GIS-program som ESRI ArcGIS Pro, TatukGIS, Blue Marble Geographic Global Mapper och Pitney Bowes MapInfo. DT0-filer används mestadels av vetenskapliga och tekniska samhällen för att studera lutningen, höjden och ytjämnheten hos globala terränger.

DT0 filformat liknar filtyperna [DT1](/gis/dt1/) och [DT2](/gis/dt2/) men med mindre granularitet.

### DT0-filformat

DT0-filer sparas som binära filer på skiva. Dessa kan läsas med många GIS-applikationer. DT0-filer kan slås samman till en File Geodatabase Raster Catalog som kan användas för att skapa en stor mosaik.

## Hur konverterar man Raster till DTED-filer?

Det finns flera verktyg som kan konvertera Raster till DTED-filer. [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) är ett sådant verktyg som kan konverteras Raster till DTED.

## Referenser

 * [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
 * [KML-filformat](/gis/kml/)

