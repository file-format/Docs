{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File MPK: formato file del pacchetto ArcGIS Map",
  "description":"Scopri il formato file MPK e le API che possono creare e aprire file MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-it",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Cos'è un file MPK?

Un file MPK è un file del pacchetto ArcGIS Map creato con ArcGIS. Contiene un documento cartografico .mxd e i dati correlati. Inoltre, contiene informazioni aggiuntive come layer di riferimento, simboli e altre risorse. Il file MPK viene utilizzato per condividere mappe e dati con altri utenti. Ciò elimina la disponibilità di altri che abbiano la fonte dati originale e aiuta anche a distribuire le mappe da utilizzare su un dispositivo mobile.

## Formato file MPX

I dettagli del formato file interno dei file MPX non sono disponibili pubblicamente come riferimento per lo sviluppatore.

### Crea file MPK utilizzando ArcGIS

I file MPK possono essere creati utilizzando ArcGIS. L'opzione Condividi con nome nel menu Pacchetto mappa può essere utilizzata per creare un file .mpk che contiene il documento della mappa e tutti i dati e le risorse a cui fa riferimento. Questo file MPK può quindi essere condiviso con altri e può essere aperto in ArcMap e ArcGIS Pro per visualizzare la mappa e i dati.

### Crea un file MPK usando Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Utilizzo di Python per creare pacchetti di mappe per tutti i documenti di mappa in una cartella

Il seguente codice Python trova e crea pacchetti di mappe per tutti i documenti di mappa che risiedono in una cartella specificata.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## Riferimenti

* [Mappa dei pacchetti](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


