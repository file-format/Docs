{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPK 파일 - ArcGIS 맵 패키지 파일 형식",
  "description":"MPK 파일을 만들고 열 수 있는 MPK 파일 형식 및 API에 대해 알아보십시오.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## .MPK 파일이란?

MPK 파일은 ArcGIS로 생성되는 ArcGIS Map 패키지 파일입니다. 여기에는 .mxd 맵 문서 및 관련 데이터가 포함됩니다. 또한 참조된 레이어, 기호 및 기타 리소스와 같은 추가 정보가 포함되어 있습니다. MPK 파일은 다른 사용자와 지도 및 데이터를 공유하는 데 사용됩니다. 이것은 원본 데이터 소스를 가진 다른 사람의 가용성을 제거하고 모바일 장치에서 사용할 맵을 배포하는 데에도 도움이 됩니다.

## MPX 파일 형식

MPX 파일의 내부 파일 형식 세부 정보는 개발자 참조를 위해 공개적으로 사용할 수 없습니다.

### ArcGIS를 사용하여 MPK 파일 생성

MPK 파일은 ArcGIS를 사용하여 생성할 수 있습니다. "지도 패키지" 메뉴의 "다른 이름으로 공유" 옵션을 사용하여 지도 문서와 모든 참조 데이터 및 리소스를 포함하는 .mpk 파일을 만들 수 있습니다. 그런 다음 이 MPK 파일을 다른 사람과 공유할 수 있으며 ArcMap 및 ArcGIS Pro에서 열어 맵과 데이터를 볼 수 있습니다.

### Python을 사용하여 MPK 파일 만들기

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Python을 사용하여 폴더의 모든 지도 문서에 대한 지도 패키지 만들기

다음 Python 코드는 지정된 폴더에 있는 모든 맵 문서에 대한 맵 패키지를 찾아 생성합니다.

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

## 참조

* [패키지 맵](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)

