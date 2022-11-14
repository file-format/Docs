{
  "date" : "2019-10-11",
  "keywords" :[ "gpx 파일", "gpx 파일이란", "파일", "gpx 예", "gpx 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX 교환 파일 형식",
  "description":"GPX 파일 형식과 GPX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .GPX 파일이란?

GPX 확장자를 가진 파일은 인터넷에서 응용 프로그램과 웹 서비스 간의 GPS 데이터 교환을 위한 GPS 교환 형식을 나타냅니다. 여러 프로그램에서 가져올 웨이포인트, 경로 및 트랙과 같은 GPS 데이터를 포함하는 경량 XML 파일 형식입니다. GPX 파일 형식은 열려 있으며 다양한 응용 프로그램 및 GPS 장치에서 지원됩니다. 이러한 파일의 GPS 데이터는 지리 공간 목적의 매핑 응용 프로그램에 표시하기 위해 로드될 수 있습니다.

## GPX 파일 형식 ##

GPX 파일은 위도 및 경도 위치 데이터, 고도 값 및 기타 가능한 기타 설명 정보로 구성됩니다. 위치 데이터는 십진수로 표시되고 고도는 미터로 표시됩니다. GPX 파일의 시간은 ISO 8601 형식을 사용하는 UTC(협정 세계시)입니다. GPX 파일을 사용하면 다음과 같은 이점이 있습니다.

* GPX를 사용하면 Windows, MacOS, Linux, Palm 및 PocketPC용 프로그램 목록이 늘어남에 따라 데이터를 교환할 수 있습니다.
* GPX는 간단한 웹 페이지 또는 변환기 프로그램을 사용하여 다른 파일 형식으로 변환할 수 있습니다.
* GPX는 XML 표준을 기반으로 하므로 사용하는 많은 새 프로그램(예: Microsoft Excel)에서 GPX 파일을 읽을 수 있습니다.
* GPX를 사용하면 웹상의 누구나 좋아하는 프로그램과 즉시 작동하는 새로운 기능을 쉽게 개발할 수 있습니다.

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd)는 참조용 GPX 파일 형식에 대한 표현을 보여줍니다.

### 필수 데이터 ###

다음은 GPS 데이터를 표현하기 위한 GPX 파일의 일부인 필수 데이터입니다.

* **Waypoints**: Waypoint는 한 점의 WGS84(GPS) 좌표로 OGR 유형 wkbPoint의 피처 레이어를 나타냅니다.
* **경로**: OGR 유형 wkbLineString의 기능 레이어를 나타냅니다. 여기에는 목적지로 이어지는 턴 또는 스테이지 포인트를 보여주는 웨이포인트인 트랙 포인트 목록이 포함됩니다.
* **트랙**: 트랙은 OGR 유형 wkbMultiLineString의 기능 레이어를 나타냅니다. 경로를 설명하는 포인트의 정렬된 목록에서 웨이포인트를 포함하는 하나 이상의 세그먼트로 구성됩니다. 연속 GPS 트랙을 나타내는 트랙 포인트 목록으로 구성됩니다.

### GPX 예제 파일 ###

다음 GPX 파일은 GPX 파일의 GPS 데이터 구성을 보여주고 GPX 파일의 내용에 대한 좋은 아이디어를 줄 수 있습니다.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## 참조 ##

* [GPX 파일 형식](http://www.topografix.com/gpx.asp)
* [GPX - 위키피디아 작성](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

