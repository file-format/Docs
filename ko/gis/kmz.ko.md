{
  "date" : "2019-10-11",
  "keywords" :[ "kmz 파일", "kmz 파일이란", "파일", "kmz 예", "kmz 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML 압축 파일 형식",
  "description":"KMZ 파일 형식 및 KMZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .KMZ 파일이란?

KMZ(KML Zipped) 파일은 Google Earth와 같은 GIS 응용 프로그램에서 볼 수 있는 지리 공간 정보를 포함하는 압축된 [KML](/ko/gis/kml/) 파일의 표현입니다. 장소 표시에 대한 정보는 맞춤 이름과 함께 위도 및 경도로 파일에 표시됩니다. 단일 패키지 KMZ 파일은 다른 사용자와 쉽게 공유할 수 있습니다. KMZ 파일에는 모델의 지리적 표현을 위한 3D 모델 데이터도 포함될 수 있습니다. KMZ 파일은 파일을 온라인 위치에 저장한 다음 Google 지도 검색 상자에 URL을 입력하여 Google 지도에서 열 수 있습니다.

## 파일 구조 ##

MKZ 파일의 내용은 기본 KML 파일과 0개 이상의 관련 파일로 구성됩니다. WinZIP과 같은 표준 압축 해제 유틸리티를 사용하여 추출할 수 있습니다. KMZ 파일 형식도 압축 비율이 10:1인 아카이브로 압축됩니다. 애플리케이션과 같은 Google 어스의 데이터를 KMZ 파일 형식으로 직접 내보낼 수 있습니다. 기본 KML 파일의 이름은 **doc.kml**입니다. KMZ 파일을 패키징하는 동안 둘 이상의 KML 파일을 추가할 수 있지만 Google 어스가 KMZ 파일을 열고 읽을 때 첫 번째 KML 파일을 검색하기 때문에 이점이 없습니다. 아카이브에 있는 추가 KML 파일은 무시합니다. Google 어스에서 원하는 KML 파일을 읽을 수 있도록 KMZ 파일 내부에 하나의 KML 파일만 배치하는 것이 좋습니다.

doc.kml 파일에서 참조하는 이미지, 모델, 텍스처, 사운드 파일 및 기타 리소스는 기본 폴더 내의 다른 하위 폴더에 있습니다. 여기에는 지원 파일 수에 따라 약간의 복잡성이 포함될 수도 있습니다. 이러한 구성 리소스에 대한 링크는 상대적으로 참조하거나 절대 참조를 통해 참조할 수 있습니다.

### 상대 참조 ###

리소스가 기본 폴더 내의 하위 폴더 내 기본 doc.kml과 함께 배치되면 상대 참조는 다음 예와 같이 이러한 지원 파일을 가리킬 수 있습니다(아이콘만 해당).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### 절대 참조 ###

리소스도 절대적으로 참조할 수 있습니다. 절대 참조에는 링크된 파일의 전체 URL이 포함됩니다. 파일이 중앙 서버에 게시될 때 절대 참조를 사용하면 상대 참조에 비해 파일이 명확하게 유지됩니다. 로컬 파일은 절대 참조하지 않는 것이 좋습니다. 파일이 새 시스템으로 이동되면 이러한 링크가 끊어지기 때문입니다. 절대 참조의 예는 다음과 같습니다.

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## 또한보십시오 ##

* [GeoJSON](/ko/gis/geojson/)

## 참조 ##

* [Google 어스 및 KMZ 파일](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

