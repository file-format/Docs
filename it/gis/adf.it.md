{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato griglia binaria ADF - ESRI ArcInfo",
  "description":"Scopri il formato di file ADF e le API che possono creare e aprire file ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Che cos'è un file ADF?

Un file con estensione .adf è un formato di file di dati raster utilizzato dalle applicazioni software ESRI come ArcGIS, ArcView e ArcInfo. I dati spaziali vengono archiviati come una griglia binaria nativa di ESRI. La griglia è composta da righe e colonne di celle che possono essere intere o in virgola mobile. Le griglie intere in un file ADF rappresentano dati discreti e le griglie a virgola mobile rappresentano dati continui. Un altro popolare formato di file ESRI è il file [SHP](/it/gis/shp/) che rappresenta le informazioni geospaziali sotto forma di dati vettoriali che devono essere utilizzati dalle applicazioni GIS (Geographic Information Systems).

## Formato file ADF - Ulteriori informazioni

I file ADF vengono salvati come file binari su disco in una griglia binaria. Le griglie di numeri interi hanno attributi che sono archiviati in una tabella degli attributi del valore (IVA). Ogni valore univoco nella griglia ha un record in IVA in cui il record memorizza il valore univoco e il numero di celle nella griglia è rappresentato da quel valore.

Le griglie a virgola mobile non hanno IVA.

### Struttura della griglia

All'interno del file ADF, le griglie vengono implementate utilizzando una struttura di dati raster affiancata. L'unità di base all'interno di questa struttura di dati raster è un blocco rettangolare di celle. Ogni blocco viene memorizzato su disco e compresso in una struttura di file di lunghezza variabile, chiamata tile. Ogni blocco viene archiviato come un record di lunghezza variabile.

I raster GRID vengono archiviati negli spazi di lavoro, in cui un'area di lavoro contiene una sottodirectory info e una sottodirectory per ogni GRID. Esistono diversi file che identificano la posizione geografica e attribuiscono i dati per la griglia corrispondente. La sottodirectory Info contiene diversi file che mantengono determinate informazioni sulla GRID e altri dataset, come le coperture, nell'area di lavoro.

## Riferimenti ##

* [Formato griglia ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
