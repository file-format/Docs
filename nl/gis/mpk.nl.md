{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK-bestand - ArcGIS Map Package-bestandsindeling",
  "description":"Leer meer over de MPK-bestandsindeling en API's waarmee u MPK-bestanden kunt maken en openen.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-nl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Wat is een MPK-bestand?

Een MPK-bestand is een ArcGIS Map-pakketbestand dat is gemaakt met ArcGIS. Het bevat een .mxd-kaartdocument en gerelateerde gegevens. Daarnaast bevat het aanvullende informatie, zoals lagen waarnaar wordt verwezen, symbolen en andere bronnen. MPK-bestand wordt gebruikt om kaarten en gegevens met andere gebruikers te delen. Dit elimineert de beschikbaarheid van anderen die over de originele gegevensbron beschikken en helpt ook bij het distribueren van kaarten voor gebruik op een mobiel apparaat.

## MPX-bestandsindeling

De details van het interne bestandsformaat van MPX-bestanden zijn niet openbaar beschikbaar ter referentie van de ontwikkelaar.

### Maak een MPK-bestand met ArcGIS

MPK-bestanden kunnen worden gemaakt met ArcGIS. De optie Delen als in het menu Kaartpakket kan worden gebruikt om een .mpk-bestand te maken dat het kaartdocument en alle gegevens en bronnen waarnaar wordt verwezen, bevat. Dit MPK-bestand kan vervolgens met anderen worden gedeeld en kan worden geopend in ArcMap en ArcGIS Pro om de kaart en gegevens te bekijken.

### Maak een MPK-bestand met Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python gebruiken om kaartpakketten te maken voor alle kaartdocumenten in een map

De volgende Python-code zoekt en maakt kaartpakketten voor alle kaartdocumenten die zich in een opgegeven map bevinden.

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

## Referenties

* [Pakketoverzicht](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


