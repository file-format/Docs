{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SDF 파일 - 공간 데이터 형식 파일",
  "description":"SDF 파일을 만들고 열 수 있는 SDF 파일 형식 및 API에 대해 알아보십시오.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## .SDF 파일이란?

공간 데이터 파일(SDF)은 Autodesk에서 개발한 지리 데이터베이스 파일 형식입니다. 지형 공간 데이터를 저장하며 Autodesk GIS 프로그램 MapGuide 및 AutoCAD Map 3D에서 사용됩니다. SDF 파일 형식은 단일 파일 데이터베이스 파일 형식 SQLite3을 기반으로 합니다. 대용량 공간정보 데이터셋에 최적화된 파일 포맷으로 평가된다.

Autodesk AutoCAD Map 3D 2022 및 Autodesk AutoCAD Civil 3D 2023을 사용하여 SDF 파일을 열 수 있습니다.

## SDF 파일 형식 - 추가 정보

SDF 파일 형식은 바이너리 파일로 디스크에 저장됩니다. 데이터의 이진 직렬화를 위해 저수준 스토리지 구성 요소를 활용하는 SQLite 데이터베이스를 기반으로 합니다. SDF 파일에는 파일당 여러 피쳐 클래스와 각 피쳐 클래스에 대한 여러 지오메트리 특성이 포함되어 있습니다. SDF 파일의 데이터는 R-tree를 사용하는 각 지오메트리 속성의 인덱싱으로 인해 고속으로 액세스할 수 있습니다.

## 참조

* [SDF 데이터 형식](https://en.wikipedia.org/wiki/Spatial_Data_File)
* [Autodesk SDF 가져오기](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

