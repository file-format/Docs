{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل MPK - قالب فایل بسته نقشه ArcGIS",
  "description":"درباره فرمت فایل MPK و API هایی که می توانند فایل های MPK را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-fa",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## فایل MPK چیست؟

فایل MPK یک فایل بسته نقشه ArcGIS است که با ArcGIS ایجاد می شود. این شامل یک سند نقشه mxd و داده های مرتبط است. علاوه بر این، حاوی اطلاعات اضافی مانند لایه های مرجع، نمادها و منابع دیگر است. فایل MPK برای به اشتراک گذاری نقشه ها و داده ها با سایر کاربران استفاده می شود. این امر دسترسی دیگران را که منبع اصلی داده را دارند حذف می کند و همچنین به توزیع نقشه ها برای استفاده در دستگاه تلفن همراه کمک می کند.

## فرمت فایل MPX

جزئیات فرمت فایل داخلی فایل های MPX به صورت عمومی برای مرجع توسعه دهنده در دسترس نیست.

### فایل MPK را با استفاده از ArcGIS ایجاد کنید

فایل های MPK را می توان با استفاده از ArcGIS ایجاد کرد. گزینه Share As در منوی Map Package را می توان برای ایجاد یک فایل .mpk که حاوی سند نقشه و همه داده ها و منابع ارجاع شده آن است، استفاده کرد. سپس این فایل MPK را می توان با دیگران به اشتراک گذاشت و می تواند در ArcMap و ArcGIS Pro برای مشاهده نقشه و داده ها باز شود.

### فایل MPK را با استفاده از پایتون ایجاد کنید

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### استفاده از پایتون برای ایجاد بسته های نقشه برای همه اسناد نقشه در یک پوشه

کد پایتون زیر بسته های نقشه را برای تمام اسناد نقشه که در یک پوشه مشخص قرار دارند، پیدا کرده و ایجاد می کند.

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

## منابع

* [نقشه بسته](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


