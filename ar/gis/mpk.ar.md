{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ملف MPK - تنسيق ملف حزمة خريطة ArcGIS",
  "description":"ملف MPK - تنسيق ملف حزمة خريطة ArcGIS",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## ما هو ملف MPK؟

ملف MPK هو ملف حزمة ArcGIS Map الذي تم إنشاؤه باستخدام ArcGIS. يحتوي على مستند خريطة .mxd والبيانات ذات الصلة. بالإضافة إلى ذلك، فهو يحتوي على معلومات إضافية مثل الطبقات المرجعية والرموز والموارد الأخرى. يستخدم ملف MPK لمشاركة الخرائط والبيانات مع مستخدمين آخرين. يؤدي هذا إلى إلغاء توفر الآخرين الذين لديهم مصدر البيانات الأصلي ويساعد أيضًا في توزيع الخرائط لاستخدامها على جهاز محمول.

## تنسيق الملف إم بي إكس

تفاصيل تنسيق الملف الداخلي لملفات MPX غير متاحة للعامة كمرجع للمطور.

### إنشاء ملف MPK باستخدام ArcGIS

يمكن إنشاء ملفات MPK باستخدام ArcGIS. يمكن استخدام خيار المشاركة باسم في قائمة حزمة الخريطة لإنشاء ملف .mpk الذي يحتوي على مستند الخريطة وجميع البيانات والموارد المرجعية الخاصة به. يمكن بعد ذلك مشاركة ملف MPK هذا مع الآخرين ويمكن فتحه في ArcMap وArcGIS Pro لعرض الخريطة والبيانات.

### إنشاء ملف MPK باستخدام بايثون

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### استخدام Python لإنشاء حزم الخرائط لجميع مستندات الخريطة في مجلد

يقوم كود Python التالي بالبحث عن حزم الخرائط وإنشاءها لجميع مستندات الخرائط الموجودة في مجلد محدد.

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

## مراجع

* [خريطة الحزمة](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


