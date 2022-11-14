{
  "date" : "2021-02-15",
  "keywords" :[ "asf 파일", "asf 파일 형식", "asf 파일이란", "파일", "asf 예제", "asf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - 고급 시스템 파일 형식",
  "description":"ASF 파일을 만들고 열 수 있는 ASF 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }

},
  "lastmod" : "2021-02-16"
}

## .ASF 파일이란?

확장자가 .asf인 파일은 네트워크를 통해 디지털 미디어 스트림을 저장하고 재생하기 위한 멀티미디어 파일 형식입니다. 온라인 스트리밍을 위한 비디오 및 오디오 콘텐츠를 모두 포함할 수 있는 컨테이너 파일 형식입니다. ASF 파일은 거의 찾을 수 없으며 둘 다 ASF 파일을 지정하는 Windows Media Audio([WMA](/ko/audio/wma/)) 및 Windows Media Video([WMV](/ko/video/wmv/)) 파일을 더 많이 접하게 됩니다. 각각의 코덱으로 인코딩된 콘텐츠를 가지고 있습니다. Windows 미디어 파일은 Windows Media 형식 SDK를 사용하여 만들고 읽을 수 있습니다.

## ASF 파일 형식

ASF 파일은 여러 개의 독립 또는 종속 스트림으로 구성될 수 있습니다. 여기에는 다중 채널 오디오용 다중 오디오 스트림 또는 다중 비트레이트 비디오 스트림이 포함될 수 있습니다. 다중 비트 전송률은 스트림을 서로 다른 대역폭을 통한 전송에 적합하게 만듭니다. 또한 ASF 파일의 스트림은 압축되거나 압축되지 않은 형식일 수 있습니다. Microsoft Windows Media 오디오 및 비디오 9 시리즈 코덱을 사용하면 최상의 압축을 얻을 수 있습니다. ASF 파일 형식의 전체 사양은 [Microsoft 웹 사이트](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)에서 확인할 수 있습니다.

### ASF 최상위 파일 구조

ASF 파일은 논리적으로 세 가지 유형의 최상위 개체를 포함합니다.

* `Header Object` - 필수이며 모든 ASF 파일의 시작 부분에 위치해야 합니다.
* `Data Object` - 필수이며 헤더 객체를 따라야 합니다.
* `Index Object(s)` - 선택 사항이지만 ASF 파일에 대한 시간 기반 임의 액세스를 제공하는 데 유용합니다.

다음 이미지는 ASF 파일의 최상위 파일 구조를 보여줍니다.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF 최상위 헤더 객체

Header 객체는 ASF 파일의 시작 부분에 잘 알려진 바이트 시퀀스를 제공하며 선택적으로 서지 정보와 같은 메타데이터를 포함할 수 있습니다. 여기에는 데이터 개체 내의 정보를 적절하게 해석하는 데 필요한 모든 정보가 포함됩니다. 헤더 개체에는 다음을 포함하지만 이에 국한되지 않는 여러 표준 개체가 포함될 수 있습니다.

* 파일 속성 개체 - 전역 파일 속성을 포함합니다.
* 스트림 속성 개체 - 디지털 미디어 스트림과 그 특성을 정의합니다.
* 헤더 확장 개체 - 이전 버전과의 호환성을 유지하면서 ASF 파일에 추가 기능을 추가할 수 있습니다.
* 내용 설명 개체 - 서지 정보를 포함합니다.
* 스크립트 명령 개체 - 재생 타임라인에서 실행할 수 있는 명령을 포함합니다.
* Marker Object - 파일 내에서 명명된 점프 지점을 제공합니다.

헤더 객체는 다음 구조를 사용하여 표현됩니다.

|필드 이름 |필드 유형 |크기(비트)|
---|---|---|
|객체 ID| GUID| 128|
|객체 크기| 질문| 64|
|헤더 객체의 수| DWORD| 32|
|예약1| 바이트| 8|
|예약2| 바이트| 8|

#### ASF 최상위 데이터 개체

ASF 파일에 대한 모든 디지털 미디어 데이터는 데이터 개체에 포함되며 ASF 데이터 패킷의 형태로 저장됩니다. 각 데이터 패킷은 고정 길이이며 하나 이상의 디지털 미디어 스트림에 대한 데이터를 포함합니다.

#### ASF 최상위 인덱스 개체

ASF 최상위 인덱스 개체에는 다음 두 가지 유형이 있습니다.

* `Simple Index Object` - ASF 파일에 있는 비디오 데이터의 시간 기반 인덱스를 포함합니다. 인덱스 항목 사이의 시간 간격은 일정하며 단순 인덱스 개체에 저장됩니다.
* `Index Object` - 형식이 유사한 Index Object, Media Object Index Object 및 Timecode Index Object를 나타냅니다. 단순 인덱스 개체와 마찬가지로 인덱스 개체는 고정된 시간 간격으로 시간을 기준으로 인덱싱하지만 비디오 스트림에 국한되지 않습니다.

## 참고문헌

* [ASF 파일 형식 - 마이크로소프트](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime 파일 형식 - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

