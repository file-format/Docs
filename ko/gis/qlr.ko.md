{
  "date" : "2019-10-11",
  "keywords" :[ "qlr 파일", "qlr 파일 형식", "qlr 파일이란", "파일", "qlr 예제", "qlr 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS 레이어 정의 파일",
  "description":"QLR 파일을 만들고 열 수 있는 QLR 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## .QLR 파일이란?

.qlr이 있는 파일은 레이어 데이터 소스에 대한 포인터를 포함하는 레이어 정의 파일입니다. 이것은 레이어에 대한 [QGIS](https://www.qgis.org/en/site/) 스타일 정보에 추가됩니다. 모든 관련 스타일에 대한 참조가 있는 이 파일은 스타일 정보를 가져오는 데 사용할 데이터의 단일 소스로 사용됩니다. QLR 파일을 사용하면 데이터 소스에 대한 정보를 이 단일 파일에 넣을 수 있으며 다른 응용 프로그램에서 읽어 스타일 정보를 로드할 수 있습니다. QLR 파일은 메모장++과 같은 텍스트 편집기로 열 수 있습니다.

## QLR 파일 형식

[QGS](/ko/gis/qgs/)와 유사한 QLR은 XML 태그 형식의 레이어 데이터 소스에 대한 포인터를 포함하는 XML 파일입니다. ArcGIS .lyr 파일과 유사합니다. QML 파일의 최상위 태그는 아래 이미지와 같습니다.

{{< figure src="../qlr.png" title="" >}}

## 참고문헌

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

