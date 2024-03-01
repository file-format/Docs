{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK-tiedosto - ArcGIS-karttapakettitiedostomuoto",
  "description":"Opi MPK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MPK-tiedostoja.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-fi",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Mikä on MPK-tiedosto?

MPK-tiedosto on ArcGIS Map -pakettitiedosto, joka luodaan ArcGIS:llä. Se sisältää .mxd-karttadokumentin ja siihen liittyvät tiedot. Lisäksi se sisältää lisätietoja, kuten viitatut tasot, symbolit ja muut resurssit. MPK-tiedostoa käytetään karttojen ja tietojen jakamiseen muiden käyttäjien kanssa. Tämä eliminoi muiden, joilla on alkuperäinen tietolähde, saatavuuden ja auttaa myös jakamaan karttoja käytettäviksi mobiililaitteella.

## MPX tiedostomuoto

MPX-tiedostojen sisäiset tiedostomuodot eivät ole saatavilla julkisesti kehittäjien viitteeksi.

### Luo MPK-tiedosto ArcGISillä

MPK-tiedostoja voidaan luoda ArcGIS:llä. Karttapaketti-valikon Jaa nimellä -vaihtoehdolla voidaan luoda .mpk-tiedosto, joka sisältää karttadokumentin ja kaikki siihen viitatut tiedot ja resurssit. Tämä MPK-tiedosto voidaan sitten jakaa muiden kanssa, ja se voidaan avata ArcMapissa ja ArcGIS Prossa nähdäksesi kartan ja tiedot.

### Luo MPK-tiedosto Pythonilla

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Pythonin käyttäminen karttapakettien luomiseen kaikille kansion karttadokumenteille

Seuraava Python-koodi etsii ja luo karttapaketit kaikille tietyssä kansiossa oleville karttadokumenteille.

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

## Viitteet

* [Pakettikartta](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


