{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "MPK ফাইল - ArcGIS ম্যাপ প্যাকেজ ফাইল ফরম্যাট",
  "description":"MPK ফাইল ফরম্যাট এবং APIগুলি সম্পর্কে জানুন যা MPK ফাইলগুলি তৈরি এবং খুলতে পারে৷",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-bn",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## একটি MPK ফাইল কি?

একটি MPK ফাইল একটি ArcGIS মানচিত্র প্যাকেজ ফাইল যা ArcGIS দিয়ে তৈরি করা হয়। এটিতে একটি .mxd মানচিত্র নথি এবং সম্পর্কিত ডেটা রয়েছে। উপরন্তু, এতে অতিরিক্ত তথ্য যেমন রেফারেন্সড লেয়ার, চিহ্ন এবং অন্যান্য সম্পদ রয়েছে। MPK ফাইল অন্যান্য ব্যবহারকারীদের সাথে মানচিত্র এবং ডেটা ভাগ করতে ব্যবহার করা হয়। এটি মূল ডেটা উত্স থাকা অন্যদের প্রাপ্যতা দূর করে এবং একটি মোবাইল ডিভাইসে ব্যবহার করার জন্য মানচিত্র বিতরণ করতে সহায়তা করে।

## MPX ফাইল ফরম্যাট

MPX ফাইলগুলির অভ্যন্তরীণ ফাইল বিন্যাস বিবরণ বিকাশকারীর রেফারেন্সের জন্য সর্বজনীনভাবে উপলব্ধ নয়৷

### ArcGIS ব্যবহার করে MPK ফাইল তৈরি করুন

MPK ফাইল ArcGIS ব্যবহার করে তৈরি করা যেতে পারে। মানচিত্র প্যাকেজ মেনুতে শেয়ার এজ বিকল্পটি একটি .mpk ফাইল তৈরি করতে ব্যবহার করা যেতে পারে যাতে মানচিত্র নথি এবং এর সমস্ত রেফারেন্সকৃত ডেটা এবং সংস্থান রয়েছে৷ এই MPK ফাইলটি তখন অন্যদের সাথে শেয়ার করা যেতে পারে এবং ম্যাপ এবং ডেটা দেখতে ArcMap এবং ArcGIS Pro-তে খোলা যেতে পারে।

### পাইথন ব্যবহার করে MPK ফাইল তৈরি করুন

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### একটি ফোল্ডারে সমস্ত মানচিত্র নথির জন্য মানচিত্র প্যাকেজ তৈরি করতে পাইথন ব্যবহার করে

নিম্নলিখিত পাইথন কোডটি একটি নির্দিষ্ট ফোল্ডারে থাকা সমস্ত মানচিত্রের নথিগুলির জন্য মানচিত্র প্যাকেজগুলি খুঁজে বের করে এবং তৈরি করে।

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

## তথ্যসূত্র

* [প্যাকেজ মানচিত্র](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


