{
  "date" : "2019-10-11",
  "keywords" :[ "qgs 파일", "qgs 파일 형식", "qgs 파일이란", "파일", "qgs 예제", "qgs 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS 프로젝트 파일 형식",
  "description":"QGS 파일을 만들고 열 수 있는 QGS 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .QGS 파일이란?

확장자가 .qgs인 파일은 오픈 소스 크로스 플랫폼 GIS 애플리케이션인 [QGIS](https://www.qgis.org/en/site/)로 생성된 프로젝트 파일입니다. 프로젝트에 대한 레이어 속성 및 보조 데이터와 같은 모든 프로젝트 설정. 맵 프로젝트를 디스크에 저장할 때 생성됩니다. 실제로 GIS 데이터에 대한 포인터, 레이어에 대한 스타일 지정 정보 및 프로젝트 제목과 같은 정보를 유지하는 구성 파일입니다. QGS 파일은 무료로 다운로드할 수 있는 QGIS 소프트웨어로 열 수 있습니다.

## QGS 파일 형식

QGS 파일은 [XML](/ko/web/xml/) 형식이며 프로젝트 데이터를 XML 태그로 저장합니다. QGS 파일에는 다음과 같은 정보가 포함되어 있습니다.

* 프로젝트 제목
* 프로젝트 CRS
* 레이어 트리
* 스냅 설정
* 관계
* 지도 캔버스 범위
* 프로젝트 모델
* 전설
* mapview 도크(2D 및 3D)
* 기본 데이터 세트(데이터 소스)에 대한 링크가 있는 레이어 및 범위, SRS, 조인, 스타일, 렌더러, 혼합 모드, 불투명도 등을 포함한 기타 레이어 속성.
* 프로젝트 속성

### QGS 최상위 XML 태그

{{< figure src="../qgstoplevel.png" title="" >}}

### 확장된 최상위 프로젝트 레이어 태그

{{< figure src="../qgstoplevel.png" title="" >}}

## 참고문헌

* [QGIS](https://www.qgis.org/en/site/)

