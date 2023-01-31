{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier MPK - Format de fichier du package de carte ArcGIS",
  "description":"En savoir plus sur le format de fichier MPK et les API qui peuvent créer et ouvrir des fichiers MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Qu'est-ce qu'un fichier MPK ?

Un fichier MPK est un fichier de package ArcGIS Map créé avec ArcGIS. Il contient un document ArcMap .mxd et les données associées. En outre, il contient des informations supplémentaires telles que des couches référencées, des symboles et d'autres ressources. Le fichier MPK est utilisé pour partager des cartes et des données avec d'autres utilisateurs. Cela élimine la disponibilité des autres ayant la source de données d'origine et aide également à distribuer des cartes à utiliser sur un appareil mobile.

## Format de fichier MPX

Les détails du format de fichier interne des fichiers MPX ne sont pas disponibles publiquement pour la référence du développeur.

### Créer un fichier MPK à l'aide d'ArcGIS

Les fichiers MPK peuvent être créés à l'aide d'ArcGIS. L'option "Partager en tant que" dans le menu "Package de carte" peut être utilisée pour créer un fichier .mpk qui contient le document cartographique et toutes ses données et ressources référencées. Ce fichier MPK peut ensuite être partagé avec d'autres et peut être ouvert dans ArcMap et ArcGIS Pro pour afficher la carte et les données.

### Créer un fichier MPK en utilisant Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Utilisation de Python pour créer des paquetages cartographiques pour tous les documents cartographiques d'un dossier

Le code Python suivant recherche et crée des paquetages de cartes pour tous les documents ArcMap qui résident dans un dossier spécifié.

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

## Références

* [Carte des packages](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

