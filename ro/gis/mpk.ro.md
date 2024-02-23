{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier MPK - Format de fișier ArcGIS Map Package",
  "description":"Aflați despre formatul de fișier MPK și despre API-urile care pot crea și deschide fișiere MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-ro",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Ce este un fișier MPK?

Un fișier MPK este un fișier de pachet ArcGIS Map care este creat cu ArcGIS. Conține un document de hartă .mxd și date aferente. În plus, conține informații suplimentare, cum ar fi straturi de referință, simboluri și alte resurse. Fișierul MPK este folosit pentru a partaja hărți și date cu alți utilizatori. Acest lucru elimină disponibilitatea altor persoane care au sursa originală de date și ajută, de asemenea, la distribuirea hărților pentru a fi utilizate pe un dispozitiv mobil.

## Format de fișier MPX

Detaliile formatului de fișier intern ale fișierelor MPX nu sunt disponibile public pentru referință de către dezvoltatori.

### Creați fișierul MPK utilizând ArcGIS

Fișierele MPK pot fi create folosind ArcGIS. Opțiunea Partajare ca” din meniul Pachet hărți” poate fi utilizată pentru a crea un fișier .mpk care conține documentul hărții și toate datele și resursele sale de referință. Acest fișier MPK poate fi apoi partajat altor persoane și poate fi deschis în ArcMap și ArcGIS Pro pentru a vizualiza harta și datele.

### Creați fișierul MPK folosind Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Utilizarea Python pentru a crea pachete de hărți pentru toate documentele de hărți dintr-un folder

Următorul cod Python găsește și creează pachete de hărți pentru toate documentele de hărți care se află într-un folder specificat.

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

## Referințe

* [Harta pachetului](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


