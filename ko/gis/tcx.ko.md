{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX 파일 형식 - 교육 센터 XML 파일",
  "description":"TCX 파일 형식과 TCX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## .TCX 파일이란?

TCX(Training Center XML) 파일은 피트니스 장치 간에 데이터를 공유하는 데 사용되는 데이터 교환 형식입니다. 2008년 Garmin의 Training Center 제품과 함께 도입되었습니다. 심박수, 달리기 케이던스, 자전거 케이던스, 칼로리, 랩 타임 등의 운동 데이터는 TCX 파일 내부에 [XML](/ko/web/xml/) 형식으로 저장됩니다. 또한 운동 트랙에 대한 요약 데이터도 TCX 파일에 포함됩니다. TCX 파일은 Garmin 스포츠 웨어러블 장치로 생성되는 [FIT](/ko/gis/fit/) 파일과 유사합니다.

## TCX 파일 형식 - 추가 정보

TCX 파일은 각 레코드가 활동으로 저장된 XML 파일로 디스크에 저장됩니다. 활동은 [GPX]와 유사한 해당 위도 위치에 대한 타임스탬프와 함께 위치 쌍을 포함하는 시간, 랩 시간, ID, 심박수, 강도, 케이던스 및 트랙 정보와 같은 운동의 모든 데이터로 구성됩니다. (/ko/gis/gpx/) 파일.

### TCX 파일 형식 버전

Garmin에서 호스팅하는 자체 XML 스키마가 있는 이 형식에는 두 가지 버전이 있습니다. 다음은 그 중 몇 가지입니다.

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX 데이터 프로토콜

TCX XML 형식의 스위프트 버전은 Github에서 [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol)로 제공됩니다.

## 참조 ##

* [교육센터 XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX 뷰어](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

