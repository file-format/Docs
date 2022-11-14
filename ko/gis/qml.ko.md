{
  "date" : "2019-10-11",
  "keywords" :[ "qml 파일", "qml 파일 형식", "qml 파일이란", "파일", "qml 예제", "qml 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - QGIS 스타일 파일 형식",
  "description":"QML 파일을 만들고 열 수 있는 QML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## .QML 파일이란?

.qml 확장자가 있는 파일은 QGIS 레이어에 대한 레이어 스타일 정보를 저장하는 XML 파일입니다. QGIS는 데이터를 레이어 형태로 구성할 수 있는 기능으로 지리 공간 데이터를 표시하는 데 사용되는 오픈 소스 크로스 플랫폼 GIS 애플리케이션입니다. QML 파일에는 QGIS에서 기호 정의, 크기 및 회전, 레이블 지정, 불투명도, 혼합 모드 등을 포함하여 형상 지오메트리를 렌더링하는 데 사용하는 정보가 포함되어 있습니다. QLR 파일과 달리 QML 파일에는 모든 스타일 정보가 포함되어 있습니다. QML 파일은 메모장++과 같은 모든 텍스트 편집기에서 열 수 있습니다.

## QML 파일 형식

[QGS](/ko/gis/qgs/) 및 [QLR](/ko/gis/qlr/)과 유사한 QLR은 레이어에 대한 스타일 정보를 포함하는 XML 파일입니다.

아래 그림은 QML 파일의 최상위 태그를 보여줍니다(렌더러_v2와 해당 심볼 태그만 확장됨).

{{< figure src="../qml.png" title="" >}}

## 참고문헌

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

