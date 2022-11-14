{
  "date" : "2019-10-11",
  "keywords" :[ "kml 파일", "kml 파일이란", "파일", "kml 예제", "kml 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - 키홀 마크업 언어",
  "description":"KML 파일 형식과 KML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .KML 파일이란?

KML, Keyhole Markup Language)는 XML 표기법의 지리 정보를 포함합니다. KML로 저장된 파일은 지원하는 GIS(지리 정보 시스템) 응용 프로그램에서 열 수 있습니다. 많은 응용 프로그램이 KML 파일 형식이 국제 표준으로 채택된 후 지원을 제공하기 시작했습니다. KML은 요소와 속성이 중첩된 태그 기반 구조를 사용합니다. 모든 태그는 대소문자를 구분하며 [KML](https://developers.google.com/kml/documentation/kmlreference) 참조에 따라 이러한 태그의 순서를 따라야 합니다.

## 간략한 역사 ##

KML은 원래 Keyhole Earth Viewer로 알려진 Google Earth와 함께 사용하기 위해 개발되었습니다. KLM은 2008년 Open Geospatial Consortium에서 2008년 국제 표준으로 채택되었습니다. KLM 형식은 Google Earth와 함께 사용하도록 개발되었기 때문에 KML 파일을 보고 편집하는 최초의 형식이라는 특징이 있습니다. 시간이 지남에 따라 다양한 언어로 된 여러 API를 포함하여 KML 파일 형식을 지원하는 프로젝트가 점점 더 많아지고 있습니다.

## KML 파일 형식 사양 ##

KML 참조는 전체 파일 형식 사양을 갖기 위해 참조하기 위한 완전한 가이드입니다. 표준 KML 파일은 다음으로 구성됩니다.

* 장소 표시
* Placemarks의 설명 HTML
* 지상 오버레이
* 경로
* 다각형

이 외에도 KML 파일의 고급 버전에는 다음이 포함될 수 있습니다.

* 기하학 스타일
* 강조 표시된 아이콘의 스타일
* 화면 오버레이
* 네트워크 링크

각 KML 요소에는 파일에 있는 정보의 위치를 지정하는 위도 정보가 있습니다. 그러나 방향, 고도 및 기울기와 같은 추가 매개변수가 있을 수 있습니다.

### 장소 표시 ###

지구 표면의 위치를 나타내는 데 사용되며 다음으로 식별됩니다.<Point> 요소. 다음은 KML 파일에서 장소 표시가 표시되는 방법의 예입니다.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### 장소 표시의 설명 HTML ###

추가 정보는 장소 표시의 표현을 더욱 향상시키는 장소 표시와 연관될 수 있습니다. 이러한 정보에는 링크, 글꼴 크기, 스타일 및 색상이 포함됩니다. 또한 장소 표시의 일부가 될 텍스트 정렬 및 표도 포함됩니다.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### 지상 오버레이 ###

이것들은 지구 표면에 이미지의 레이어링을 나타냅니다. 그만큼<icon> 요소에는 오버레이 이미지 파일에 대한 링크가 포함되어 있습니다.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### 경로 ###

경로는 다음으로 표시됩니다.<LineString> 위도-경도 쌍의 모음인 요소입니다. 이를 사용하여 Google 어스에서 다양한 유형의 경로를 만들 수 있습니다.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML 파일의 공간 참조 ##

Geo-Locations에 대한 Geospatial 파일에 포함된 정보는 공간 참조 정보 없이 다른 의미를 가질 수 있습니다. 기본적으로 KML 파일의 공간 참조는 1984년 WGS84의 World Geodetic System에 의해 정의됩니다.

## 참조 ##

* [KML 참조](https://developers.google.com/kml/documentation/kmlreference)
* [KML용 Google 개발자 튜토리얼](https://developers.google.com/kml/documentation/kml_tut)
* [KML 파일 형식](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

