{
  "date": "2022-12-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DT0 fil - DTED niveau 0 filformat",
  "description": "Lær om DT0 filformat og API'er, der kan oprette og åbne DT0 filer.",
  "linktitle": "DT0",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dt-da0"
}
},
  "lastmod": "2022-12-07"
}

## Hvad er DT0 fil?

En DT0-fil er en DTED-fil (Digital Terrain Elevation Data), der indeholder niveau 0-information til at studere terrænhøjdedata. Højdedata er ensartet fordelt i en DT0-fil og kan læses af populære GIS-programmer som ESRI ArcGIS Pro, TatukGIS, Blue Marble Geographic Global Mapper og Pitney Bowes MapInfo. DT0-filer bruges mest af videnskabelige og tekniske samfund til at studere hældningen, højden og overfladeruheden af globale terræner.

DT0 filformat ligner [DT1](/gis/dt1/) og [DT2](/gis/dt2/) filtyper, men med mindre granularitet.

### DT0 filformat

DT0 filer gemmes som binære filer på disk. Disse kan læses ved hjælp af mange GIS-applikationer. DT0 filer kan flettes ind i et File Geodatabase Raster Catalog, der kan bruges til at skabe én stor mosaik.

## Sådan konverteres Raster til DTED filer?

Der er flere værktøjer, der kan konvertere Raster til DTED-filer. [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) er et sådant værktøj, der kan konverteres Raster til DTED.

## Referencer

 * [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
 * [KML-filformat](/gis/kml/)

