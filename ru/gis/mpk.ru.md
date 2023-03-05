{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл MPK — формат файла пакета карт ArcGIS",
  "description":"Узнайте о формате файла MPK и API-интерфейсах, которые могут создавать и открывать файлы MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## .MPK вариант №

Файл MPK — это файл пакета ArcGIS Map, созданный с помощью ArcGIS. Он содержит документ карты .mxd и связанные данные. Кроме того, он содержит дополнительную информацию, такую как ссылочные слои, символы и другие ресурсы. Файл MPK используется для обмена картами и данными с другими пользователями. Это устраняет доступность исходного источника данных для других, а также помогает распространять карты для использования на мобильном устройстве.

## Формат файла MPX

Сведения о внутреннем формате файлов MPX недоступны для разработчиков.

### Создать файл MPK с помощью ArcGIS

Файлы MPK можно создавать с помощью ArcGIS. Параметр «Отправить как» в меню «Пакет карты» можно использовать для создания файла .mpk, который содержит документ карты и все связанные с ним данные и ресурсы. Затем этим файлом MPK можно поделиться с другими, и его можно открыть в ArcMap и ArcGIS Pro для просмотра карты и данных.

### Создать файл MPK с помощью Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Использование Python для создания пакетов карт для всех документов карты в папке

Следующий код Python находит и создает пакеты карт для всех документов карты, находящихся в указанной папке.

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

## использованная литература

* [Карта пакета](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

