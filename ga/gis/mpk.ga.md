{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad MPK - Formáid Chomhaid Phacáiste Léarscáil ArcGIS",
  "description":"Foghlaim faoi fhormáid comhaid MPK agus APIs is féidir comhaid MPK a chruthú agus a oscailt.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-ga",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Cad is comhad MPK ann?

Is comhad pacáiste Léarscáil ArcGIS é comhad MPK a chruthaítear le ArcGIS. Tá doiciméad léarscáile .mxd agus sonraí gaolmhara ann. Ina theannta sin, tá faisnéis bhreise ann amhail sraitheanna tagartha, siombailí, agus acmhainní eile. Úsáidtear comhad MPK chun léarscáileanna agus sonraí a roinnt le húsáideoirí eile. Cuireann sé seo deireadh le hinfhaighteacht daoine eile a bhfuil an bhunfhoinse sonraí acu agus cabhraíonn sé freisin le léarscáileanna a dháileadh le húsáid ar ghléas soghluaiste.

## Formáid Chomhaid MPX

Níl sonraí formáide inmheánacha comhaid MPX ar fáil go poiblí le haghaidh tagartha an fhorbróra.

### Cruthaigh Comhad MPK le ArcGIS

Is féidir comhaid MPK a chruthú ag baint úsáide as ArcGIS. Is féidir an rogha Comhroinn Mar sa roghchlár Pacáiste Léarscáileanna a úsáid chun comhad .mpk a chruthú ina bhfuil an doiciméad léarscáile agus a chuid sonraí agus acmhainní tagartha go léir. Is féidir an comhad MPK seo a roinnt le daoine eile ansin agus is féidir é a oscailt in ArcMap agus ArcGIS Pro chun an léarscáil agus na sonraí a fheiceáil.

### Cruthaigh Comhad MPK ag baint úsáide as Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python á n-úsáid chun Pacáistí Léarscáileanna a Chruthú do gach Doiciméad Léarscáile i bhfillteán

Aimsíonn agus cruthaíonn an cód Python seo a leanas pacáistí léarscáile do gach doiciméad léarscáile a bhfuil cónaí orthu i bhfillteán sonraithe.

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

## Tagairtí

* [Léarscáil an Phacáiste](https://desktop.arcgis.com/ga/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


