{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл MPK – формат файлу пакета карт ArcGIS",
  "description":"Дізнайтеся про формат файлу MPK і API, які можуть створювати та відкривати файли MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-uk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## Що таке файл MPK?

Файл MPK – це файл пакета ArcGIS Map, створений за допомогою ArcGIS. Він містить документ карти .mxd і відповідні дані. Крім того, він містить додаткову інформацію, таку як шари посилань, символи та інші ресурси. Файл MPK використовується для обміну картами та даними з іншими користувачами. Це усуває доступність інших джерел оригінальних даних, а також допомагає розповсюджувати карти для використання на мобільному пристрої.

## Формат файлу MPX

Деталі внутрішнього формату файлів MPX недоступні для розробників.

### Створіть файл MPK за допомогою ArcGIS

Файли MPK можна створювати за допомогою ArcGIS. Параметр «Поділитися як» у меню «Пакет карти» можна використати для створення файлу .mpk, який містить документ карти та всі його дані та ресурси, на які посилаються. Потім цим файлом MPK можна поділитися з іншими та відкрити в ArcMap і ArcGIS Pro для перегляду карти та даних.

### Створіть файл MPK за допомогою Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Використання Python для створення пакетів карт для всіх документів карти в папці

Наведений нижче код Python знаходить і створює пакети карт для всіх документів карт, які знаходяться у вказаній папці.

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

## Список літератури

* [Карта пакетів](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


