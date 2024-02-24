{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ MPK - รูปแบบไฟล์แพ็คเกจแผนที่ ArcGIS",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MPK และ API ที่สามารถสร้างและเปิดไฟล์ MPK",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-th",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## ไฟล์ MPK คืออะไร??

ไฟล์ MPK เป็นไฟล์แพ็คเกจ ArcGIS Map ที่สร้างด้วย ArcGIS ประกอบด้วยเอกสารแผนที่ .mxd และข้อมูลที่เกี่ยวข้อง นอกจากนี้ยังมีข้อมูลเพิ่มเติม เช่น เลเยอร์ที่อ้างอิง สัญลักษณ์ และทรัพยากรอื่นๆ ไฟล์ MPK ใช้เพื่อแชร์แผนที่และข้อมูลกับผู้ใช้รายอื่น ซึ่งช่วยลดความพร้อมใช้งานของผู้อื่นที่มีแหล่งข้อมูลดั้งเดิม และยังช่วยกระจายแผนที่ที่จะใช้บนอุปกรณ์เคลื่อนที่อีกด้วย

## รูปแบบไฟล์ MPX

รายละเอียดรูปแบบไฟล์ภายในของไฟล์ MPX ไม่เปิดเผยต่อสาธารณะเพื่อเป็นข้อมูลอ้างอิงของนักพัฒนา

### สร้างไฟล์ MPK โดยใช้ ArcGIS

สามารถสร้างไฟล์ MPK ได้โดยใช้ ArcGIS ตัวเลือก แชร์เป็น ในเมนู แพ็คเกจแผนที่ สามารถใช้เพื่อสร้างไฟล์ .mpk ซึ่งมีเอกสารแผนที่และข้อมูลอ้างอิงและทรัพยากรทั้งหมด ไฟล์ MPK นี้สามารถแชร์กับผู้อื่นและสามารถเปิดได้ใน ArcMap และ ArcGIS Pro เพื่อดูแผนที่และข้อมูล

### สร้างไฟล์ MPK โดยใช้ Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### การใช้ Python เพื่อสร้างแพ็คเกจแผนที่สำหรับเอกสารแผนที่ทั้งหมดในโฟลเดอร์

รหัส Python ต่อไปนี้ค้นหาและสร้างแพ็คเกจแผนที่สำหรับเอกสารแผนที่ทั้งหมดที่อยู่ในโฟลเดอร์ที่ระบุ

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

## อ้างอิง

* [แผนที่แพ็คเกจ](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


