{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file CPG - File tabella codici ESRI",
  "description":"Scopri il formato di file CPG e le API che possono creare e aprire file CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Che cos'è un file CPG?

Un file CPG è un file opzionale che richiede lo Shapefile ESRI utilizzato per specificare la codepage per identificare il set di caratteri da utilizzare. Questi sono memorizzati in formato file di testo normale e contengono informazioni sulla codifica applicata per creare lo shapefile. Nel caso in cui un file CPG non sia disponibile, lo shapefile utilizza la codifica predefinita del sistema. Un file CPG, se presente, deve avere lo stesso prefisso di quello del file [SHP](/it/gis/shp/), ad esempio road.shp, road.cpg.

I file CPG possono essere aperti con ESRI ArcGIS Pro.

### Formato file CPG - Ulteriori informazioni

Quando si visualizza uno shapefile in ArcCatalog o qualsiasi altra applicazione ArcGIS, si vede solo lo shapefile. Ma in realtà, shapefile utilizza altri file associati che vengono letti insieme al file di forma principale. Il file CPG è anche uno di questi se è presente accanto al file SHP principale.

## Riferimenti

* [Estensioni file Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

