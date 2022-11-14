{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "파일", "확장자", "파일 형식", "GPS 위치", "웨이포인트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS 위치 파일 형식",
  "description":"LOC 파일 형식과 LOC 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## .LOC 파일이란?

확장자가 .loc인 파일은 웨이포인트로 지리 공간 위치를 포함하는 GPS 위치 파일입니다. 웨이포인트는 GIS(지리 정보 시스템) 애플리케이션에서 사용하는 위치를 나타내는 위도-경도 값 쌍입니다. DeLorme Topo와 같은 GPS 매핑 프로그램은 LOC 파일을 사용하여 이러한 LOC 파일에 포함된 정보를 최종 사용자가 선택 가능한 레이어로 읽고 표시합니다. 또한 애플리케이션 간에 GPS 데이터를 교환하는 데 사용됩니다. LOC 파일은 [TopoGrafix EasyGPS](https://www.easygps.com/)와 같은 응용 프로그램을 사용하여 열 수 있습니다. 이러한 응용 프로그램은 이러한 파일의 내용을 각 지리 위치에서 지도에 표시된 레이어 및 데이터로 표시합니다.

## LOC 파일 형식 - 추가 정보

LOC 파일은 [GPX](/ko/gis/gpx/) 파일과 유사하지만 다른 형식으로 저장됩니다. 이는 경유지 및 관련 정보의 내용이 구조화된 태그에 포함된 [XML](/ko/web/xml/) 파일로 저장됩니다. XML은 서로 다른 응용 프로그램 간의 데이터 교환을 위한 일반화된 언어이므로 다른 응용 프로그램과 LOC 데이터를 쉽게 교환할 수 있습니다.

## LOC 파일 형식 - 예

다음은 LOC 파일에서 한 웨이포인트의 헤더와 텍스트입니다. 알 수 있듯이 헤더 정보에는 데이터의 위치 소스가 포함되어 있습니다. 경유지에는 'ID' 및 경유지와 관련된 관련 콘텐츠 데이터와 같은 정보가 포함됩니다. 마지막으로 웨이포인트는 위도 및 경도 값과 이 특정 웨이포인트와 관련된 텍스트의 모음입니다.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## 참고문헌

* [TopGraphic EasyGPS](https://www.easygps.com/)

