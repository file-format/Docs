{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo MPK: formato de archivo del paquete de mapas de ArcGIS",
  "description":"Obtenga información sobre el formato de archivo MPK y las API que pueden crear y abrir archivos MPK",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## ¿Qué es un archivo MPK?

Un archivo MPK es un archivo de paquete de ArcGIS Map que se crea con ArcGIS. Contiene un documento de mapa .mxd y datos relacionados. Además, contiene información adicional, como capas referenciadas, símbolos y otros recursos. El archivo MPK se utiliza para compartir mapas y datos con otros usuarios. Esto elimina la disponibilidad de otros que tengan la fuente de datos original y también ayuda a distribuir mapas para usar en un dispositivo móvil.

## Formato de archivo MPX

Los detalles del formato de archivo interno de los archivos MPX no están disponibles públicamente para referencia del desarrollador.

### Crear un archivo MPK usando ArcGIS

Los archivos MPK se pueden crear usando ArcGIS. La opción "Compartir como" en el menú "Paquete de mapas" se puede usar para crear un archivo .mpk que contiene el documento de mapa y todos sus datos y recursos a los que se hace referencia. Este archivo MPK luego se puede compartir con otros y se puede abrir en ArcMap y ArcGIS Pro para ver el mapa y los datos.

### Crear archivo MPK usando Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Uso de Python para crear paquetes de mapas para todos los documentos de mapas en una carpeta

El siguiente código de Python busca y crea paquetes de mapas para todos los documentos de mapas que residen en una carpeta específica.

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

## Referencias

* [Mapa del paquete](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

