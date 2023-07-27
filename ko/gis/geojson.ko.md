{
  "date" : "2019-10-11",
  "keywords" :[ "geojson 파일", "geojson 파일이란", "파일", "geojson 예제", "geojson 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - JSON 기반 지리 파일 형식",
  "description":"GeoJSON 파일을 만들고 열 수 있는 GeoJSON 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .GeoJSON 파일이란?

GeoJSON은 지리적 특징을 비공간적 속성으로 나타내도록 설계된 JSON 기반 형식입니다. 이 형식은 다른 JSON(JavaScript Object Notation) 개체와 결합 방식을 정의합니다. JSON 형식은 지리적 기능, 해당 공간 범위 및 속성에 대한 집합적인 정보를 나타냅니다. 이 파일의 객체는 지오메트리(Point, LineString, Polygon), 피처 또는 피처 모음을 나타낼 수 있습니다. 기능은 주소와 장소를 포인트의 거리로, 주요 도로와 경계를 선 문자열로, 국가, 지방 및 토지 지역을 폴리곤으로 반영합니다. GeoJSON을 사용하면 다양한 모바일 라우팅 및 탐색 애플리케이션이 서비스 범위를 나타낼 수 있습니다. GeoJSON의 확장은 크기가 더 작고 지리 공간 토폴로지를 인코딩하는 TopoJSON입니다.

## 간략한 역사 ##

IETF(Internet Engineering Task Force)는 형식 작성자와 함께 [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/)를 구성하여 2015년 4월에 GeoJSON을 출시했습니다. GeoJSON 사양 [RFC 7946](https://tools.ietf.org/html/rfc7946), 2016년 8월에 발표된 GeoJSON 형식의 새로운 표준 사양.

## GeoJSON 파일 형식 ##

### 좌표 ###

좌표는 모든 지리 데이터의 기본 요소입니다. 이것은 단일 숫자(십진수 형식)를 나타내는 단일 차원(경도, 위도)이며 때로는 고도에 대한 좌표도 기록합니다. 시간도 차원이지만 그 복잡성으로 인해 좌표로 기록하기 어렵습니다. 두 JSON GeoJSON의 좌표는 숫자 형식으로 지정됩니다.

### 위치 ###

정렬된 좌표 배열은 [위치](https://geojson.org/geojson-spec.html#positions)를 나타냅니다. 이것은 지구상의 한 지점을 나타낼 수 있는 가장 작은 단위입니다.

`[경도, 위도, 고도]`

현재 사양이 출시되기 전에 GeoJSON은 위치당 3개의 좌표를 기록할 수 있었지만 새 사양에서는 허용하지 않습니다.

### 기하학 ###

기하학은 유형과 좌표 모음으로 구성된 GeoJSON의 단순한 모양(점, 곡선 및 표면)입니다. 점은 단일 위치를 나타내는 가장 단순한 기하학입니다.

`{ "유형": "점", "좌표": [0, 0] }`

### 라인스트링 ###

적어도 두 개의 연결된 장소가 선을 나타내는 데 사용됩니다.

`{ "유형": "줄 문자열", "좌표": [[10, 30], [10, 10]] }`

점 및 선 스트링은 지오메트리의 가장 간단한 두 가지 범주입니다. 두 가지 유형의 기하학 모두 많은 기하학적 규칙을 방해하지 않습니다. 점은 임의의 위치에 표시될 수 있으며 점이 자체 교차하는 경우에도 선은 둘 이상의 점을 가질 수 있습니다.

### 다각형 ###

GeoJSON 기하학은 다각형에서 훨씬 더 복잡해 보입니다. 다각형에는 내부 및 외부 영역이 있으며 그 내부에 구멍이 있을 수 있습니다.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

LineStrings와 비교하여 폴리곤에서 좌표 목록은 한 단계 더 중첩되며 도넛과 같은 컷아웃을 가질 수 있습니다.

### 좌표 레벨 ###

GeoJSON 형식에서는 좌표 속성에 대해 4가지 수준의 깊이가 있습니다.

### 특징 ###

기하학은 GeoJSON의 중심 부분이므로 실제 데이터는 ID와 속성을 가진 단순한 모양 그 이상입니다. 피처는 지오메트리와 속성을 기록합니다.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

기능 속성은 단일 깊이 키 값 매핑을 포함하는 [JSON](http://json.org/) 개체 유형일 수 있습니다.

### 기능 모음 ###

GeoJSON 파일의 최상위 수준에서 FeatureCollection은 다음과 같은 가장 일반적인 것입니다.

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

GeoDjango, OpenLayers 및 Geoforge 소프트웨어를 비롯한 많은 매핑 및 GIS 소프트웨어 패키지가 GeoJSON을 지원합니다. PostGIS 및 Mapnik과도 호환됩니다. Google, yahoo 및 Bing 지도의 API 서비스도 GeoJSON을 지원합니다.

## 참조 ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - 위키피디아 작성](https://en.wikipedia.org/wiki/GeoJSON)

