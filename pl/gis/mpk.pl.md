{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik MPK — format pliku pakietu map ArcGIS",
  "description":"Dowiedz się o formacie pliku MPK i interfejsach API, które umożliwiają tworzenie i otwieranie plików MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-pl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Czym jest plik MPK?

Plik MPK to plik pakietu ArcGIS Map utworzony za pomocą ArcGIS. Zawiera dokument mapy .mxd i powiązane dane. Ponadto zawiera dodatkowe informacje, takie jak warstwy, do których istnieją odniesienia, symbole i inne zasoby. Plik MPK służy do udostępniania map i danych innym użytkownikom. Eliminuje to dostępność innych osób posiadających oryginalne źródło danych, a także pomaga w dystrybucji map do użytku na urządzeniu mobilnym.

## Format pliku MPX

Szczegóły wewnętrznego formatu plików MPX nie są dostępne publicznie w celach informacyjnych dla programistów.

### Utwórz plik MPK za pomocą ArcGIS

Pliki MPK można tworzyć za pomocą ArcGIS. Opcji Udostępnij jako” w menu Pakiet map” można użyć do utworzenia pliku .mpk zawierającego dokument mapy oraz wszystkie powiązane z nim dane i zasoby. Ten plik MPK można następnie udostępnić innym osobom i otworzyć w aplikacjach ArcMap i ArcGIS Pro w celu wyświetlenia mapy i danych.

### Utwórz plik MPK przy użyciu języka Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Używanie języka Python do tworzenia pakietów map dla wszystkich dokumentów map w folderze

Poniższy kod Pythona wyszukuje i tworzy pakiety map dla wszystkich dokumentów map znajdujących się w określonym folderze.

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

## Bibliografia

* [Mapa pakietu](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


