{
  "date" : "2019-10-11",
  "keywords" :[ "gml 파일", "gml 파일이란", "파일", "gml 예제", "gml 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - 지리 마크업 언어 파일 형식",
  "description":"GML 파일을 만들고 열 수 있는 GML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .GML 파일이란?

GML은 OGC(Open Geospatial Consortium)에서 개발한 XML 사양을 기반으로 하는 Geography Markup Language의 약자입니다. 형식은 서로 다른 파일 형식 간의 교환을 위해 지리 데이터 기능을 저장하는 데 사용됩니다. 이는 지리 시스템을 위한 모델링 언어와 인터넷상의 지리 거래를 위한 개방형 교환 형식의 역할을 합니다.

## GML 파일 형식 ##

대부분의 XML 기반 문법과 마찬가지로 문법에는 문서를 설명하는 스키마와 실제 데이터를 포함하는 인스턴스 문서의 두 부분이 있습니다. GML 문서는 GML 스키마를 사용하여 설명됩니다. 이를 통해 사용자와 개발자는 점, 선 및 다각형을 포함하는 일반 지리 데이터 세트를 설명할 수 있습니다. 애플리케이션 스키마를 사용하여 사용자는 점, 선 및 다각형 대신 도로, 고속도로 및 교량을 참조할 수 있습니다.

지도에서 공간 데이터를 표현하기 위해 GML을 해석해서는 안 된다는 점은 주목할 가치가 있습니다. GML 콘텐츠의 표현은 GML이 만들어진 목적과 다릅니다. 간단히 말해서, GML은 표시 목적으로 매핑 응용 프로그램에서 사용할 수 있는 공간 콘텐츠를 보유하는 데만 사용된다는 점에서 XML과 유사합니다.

### GML의 콘텐츠 구성 ###

GML은 속성 및 기하학의 목록인 기능을 사용하여 공간 데이터를 나타냅니다. 속성에는 이름, 유형 및 값 설명이 있습니다. 지오메트리는 다음과 같은 기본 지오메트리 빌딩 블록으로 구성됩니다.

* 포인트들
* 라인
* 곡선
* 표면과
* 폴리곤

GML의 향후 버전은 3D 기하학과 기능 간의 위상 관계를 지원할 계획입니다.

GML 인코딩은 이미 상당히 복잡한 기능을 허용합니다. 예를 들어 기능은 다른 기능으로 구성될 수 있습니다. 따라서 공항과 같은 단일 기능은 유도로, 활주로, 옷걸이 및 공항 터미널과 같은 다른 기능으로 구성될 수 있습니다. 지리적 특징의 지오메트리는 여러 지오메트리 요소로 구성될 수도 있습니다. 따라서 기하학적으로 복잡한 피쳐는 점, 라인 스트링 및 폴리곤을 포함하는 지오메트리 유형의 혼합으로 구성될 수 있습니다.

### 예 ###

GML 1.0 및 2.0은 Polygons, Points 및 LineString 개체를 다음과 같이 인코딩합니다.

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## 참조 ##

* [GML 사양](http://www.opengeospatial.org/standards/gml)
* [GML - 위키피디아 작성](https://en.wikipedia.org/wiki/Geography_Markup_Language)

