{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPG 파일 형식 - ESRI 코드 페이지 파일",
  "description":"CPG 파일 형식과 CPG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## .CPG 파일이란?

CPG 파일은 사용할 문자 집합을 식별하기 위한 코드 페이지를 지정하는 데 사용되는 ESRI Shapefile이 필요한 선택적 파일입니다. 이들은 일반 텍스트 파일 형식으로 저장되며 shapefile 생성에 적용된 인코딩에 대한 정보를 포함합니다. CPG 파일을 사용할 수 없는 경우 shapefile은 시스템 기본 인코딩을 사용합니다. CPG 파일이 있는 경우 [SHP](/ko/gis/shp/) 파일과 같은 접두어를 가져야 합니다(예:roads.shp,roads.cpg).

CPG 파일은 ESRI ArcGIS Pro로 열 수 있습니다.

### CPG 파일 형식 - 추가 정보

ArcCatalog 또는 다른 ArcGIS 응용 프로그램에서 모양 파일을 볼 때 모양 파일만 표시됩니다. 그러나 실제로 shapefile은 기본 모양 파일과 함께 읽는 다른 관련 파일을 사용합니다. CPG 파일은 기본 SHP 파일과 함께 있는 경우에도 이러한 파일 중 하나입니다.

## 참고문헌

* [Shapefile 파일 확장자
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

