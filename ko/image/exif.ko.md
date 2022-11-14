{
  "date" : "2019-10-11",
  "keywords" :[ "exif 파일", "exif 파일 형식", "exif 파일이란", "파일", "exif 예제", "exif 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"EXIF 파일 형식과 EXIF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .EXIF 파일이란?
EXIF는 "Exchangeable Image File Format"의 약자로 1985년 [일본 카메라 산업 협회](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association)(JCIA)에서 처음으로 정의한 것입니다. 표준은 Japan Electronics 및 정보 기술 산업 협회(JEITA) 오늘 현재. EXIF는 디지털 카메라 및 스캐너에서 주로 사용되는 이미지 및 사운드 형식의 사양에 대한 표준입니다.

EXIF 표준에는 이미지 파일과 함께 태깅 및 메타데이터 정보가 포함됩니다. 메타데이터에는 카메라 모델, 셔터 속도, 날짜 및 시간, 조리개, 제조업체, 노출 시간, X 해상도, Y 해상도 등과 같은 정보가 포함될 수 있습니다. 일반적으로 EXIF 데이터는 기본적으로 숨겨져 있습니다. EXIF 데이터를 보려면 이미지 보기 응용 프로그램 내에서 보기 속성을 선택해야 합니다. Exif 메타데이터에는 단일 이미지 파일에 기술 및 기본 이미지 데이터와 함께 썸네일이 포함될 수도 있습니다.

## 역사 및 버전 ##

* JEIDA는 1995년 10월 Version 1을 제정하였다. 이 버전에서 JEIDA는 이미지 데이터 형식과 속성 정보, 기본 태그로 구성된 구조를 정의하였다.
* 1997년 11월, 버전 1.1은 버전 1의 대부분의 태그와 함께 도입되었지만 선택적 속성 정보 및 형식 작업에 대한 조항도 추가되었습니다.
* 1998년 6월, 버전 2, sRGB 색상 공간, 압축된 축소판 및 오디오 파일.
* 1998년 12월, 향상된 저장소 및 속성 정보가 포함된 버전 2.1.
* 2002년 2월 버전 2.2, 인쇄 마무리 기능이 추가된 개선된 버전 2.1.
* 2003년 9월, 버전 2.21, 어도비 RGB로 알려진 선택적 색 공간.

## EXIF 파일 형식

EXIF는 특정 메타데이터를 추가하여 다음 파일 형식을 사용합니다.

1. [JPEG](/ko/image/jpeg/) - 압축된 이미지 파일에 대한 이산 코사인 변환(DCT).
1. 압축되지 않은 이미지 파일용 [TIFF](/ko/image/tiff/) Rev. 6.0(RGB 또는 YCbCr).
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) 오디오 파일용(Linear [PCM](https:/) /en.wikipedia.org/wiki/Pulse-code_modulation) 또는 ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) 비압축 오디오 데이터용 μ-Law PCM 및 [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) 압축 오디오 데이터).

### EXIF에서 사용하는 마커 ###

마커 0xFFE0~~0xFFEF는 사용자 응용 프로그램에서 사용하는 "응용 프로그램 마커"입니다. 예를 들어, 구형 디지털 카메라는 이미지를 저장하기 위해 JFIF(JPEG 파일 교환 형식)를 사용합니다. JFIF는 디지캠 구성 데이터와 썸네일 이미지를 삽입하기 위해 APP0(0xFFE0) 마커를 사용합니다. 또한 EXIF는 데이터 삽입을 위해 Application Marker를 사용하지만 EXIF는 JFIF 형식과의 충돌을 피하기 위해 APP1(0xFFE1) Marker를 사용합니다. 모든 EXIF 파일 형식은 이 형식에서 시작합니다.


|SOI 마커|APP1 마커|APP1 데이터|기타 마커
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT.......|FFXX SSSS DDDD.......

SOI(0xFFD8) Marker에서 시작하므로 JPEG 파일입니다. 그러면 바로 APP1 Marker가 따라옵니다. EXIF의 모든 데이터는 이 APP1 데이터 영역에 저장됩니다. 위 표의 "SSSS" 부분은 APP1 데이터 영역(EXIF 데이터 영역)의 크기를 의미합니다. "SSSS" 크기에는 디스크립터 자체의 크기도 포함됩니다. "SSSS" 이후에 APP1 데이터가 시작됩니다. 첫 번째 부분은 EXIF, ASCII 문자 "EXIF" 및 0x00의 2바이트 사용 여부를 식별하기 위한 특수 데이터입니다. APP1 Marker 영역 다음에 다른 JPEG Marker가 따릅니다.

### Exif 데이터 구조 ###

EXIF 데이터(APP1)의 대략적인 구조는 아래와 같습니다. 위에서 논의한 바와 같이 EXIF 데이터는 ASCII 문자 "EXIF"와 2바이트의 0x00으로 시작하고 EXIF 데이터가 뒤따릅니다. EXIF는 TIFF 형식을 사용하여 데이터를 저장합니다.


|FFE1|APP1 마커
---|---|
|SSSS|APP1 데이터|APP1 데이터 크기
|45786966 0000|Exif 헤더
|49492A00 08000000|TIFF 헤더
|XXXX. . . .|IFD0(메인 이미지)|디렉토리
|LLLLLLLL|IFD1에 대한 링크
|XXXX. . . .|IFD0의 데이터 영역
|XXXX. . . .|Exif SubIFD|디렉토리
|00000000|링크 끝
|XXXX. . . .|Exif SubIFD의 데이터 영역
|XXXX. . . .|IFD1(썸네일 이미지)|디렉토리
|00000000|링크 끝
|XXXX. . . .|IFD1의 데이터 영역
|FFD8XXXX. . . XXXXFFD9|썸네일 이미지

#### TIFF 헤더 ####

8바이트 [TIFF](/ko/image/tiff/) 파일 헤더에는 다음 정보가 포함됩니다.

`Bytes 0-1:` 파일 내에서 사용된 바이트 순서입니다. 유효한 값은 "II"(4949.H) "MM"(4D4D.H)입니다.

"II" 형식에서 바이트 순서는 16비트 및 32비트 정수 모두에 대해 항상 최하위 바이트에서 최상위 바이트입니다. 이를 리틀 엔디안 바이트 순서라고 합니다. "MM" 형식에서 바이트 순서는 16비트 및 32비트 정수 모두에 대해 항상 최상위에서 최하위 순입니다. 이를 빅 엔디안 바이트 순서라고 합니다.

`Bytes 2-3:` 파일을 TIFF 파일로 추가로 식별하는 임의적이지만 신중하게 선택한 숫자(42)입니다. 바이트 순서는 Bytes 0-1의 값에 따라 다릅니다.

`Bytes 4-7:` 첫 번째 IFD의 오프셋(바이트)입니다. 디렉토리는 헤더 뒤의 파일 위치에 있을 수 있지만 단어 경계에서 시작해야 합니다. 특히, 이미지 파일 디렉토리는 설명하는 이미지 데이터를 따를 수 있습니다. 독자는 포인터가 이끄는 대로 따라가야 합니다. 이 문서에서 바이트 오프셋이라는 용어는 TIFF 파일의 시작 부분과 관련된 위치를 나타내기 위해 항상 사용됩니다. 파일의 첫 번째 바이트의 오프셋은 0입니다.

#### 이미지 파일 디렉토리 ####

IFD는 이미지에 대한 정보와 실제 이미지 데이터에 대한 포인터를 포함합니다. 2바이트 수의 디렉토리 항목 수(즉, 필드 수)와 12바이트 필드 항목 시퀀스로 구성됩니다. , 다음 IFD의 4바이트 오프셋(없으면 0)이 뒤따릅니다. TIFF 파일에는 최소한 1개의 IFD가 있어야 하고 각 IFD에는 최소한 하나의 항목이 있어야 합니다.

##### IFD 항목 #####

각 12바이트 IFD 항목의 형식은 다음과 같습니다.


|바이트|설명
---|---|
|0-1|필드를 식별하는 태그
|2-3|필드 유형
|4-7|표시된 유형의 개수
|8-11|값 오프셋, 필드에 대한 값의 파일 오프셋(바이트). 값은 단어 경계에서 시작해야 합니다. 따라서 해당 값 오프셋은 짝수가 됩니다. 이 파일 오프셋은 이미지 데이터 이후에도 파일의 아무 곳이나 가리킬 수 있습니다.

TIFF 필드는 TIFF 태그와 그 값으로 구성된 논리적 개체이다. 이 논리적 개념은 IFD 항목으로 구현되며, IFD 항목의 마지막 4바이트인 값/오프셋 부분에 맞지 않는 경우 실제 값을 더합니다. TIFF 필드와 IFD 항목이라는 용어는 대부분의 상황에서 서로 바꿔 사용할 수 있습니다.

#### 썸네일 이미지 ####

Exif 형식은 이미지의 축소판을 포함합니다(Ricoh RDC-300Z 제외). 일반적으로 IFD1 옆에 있습니다. 썸네일에는 3가지 형식이 있습니다. JPEG 형식(JPEG은 YCbCr 사용), RGB TIFF 형식, YCbCr TIFF 형식.

##### JPEG 형식 썸네일 #####

IFD1의 Compression(0x0103) Tag 값이 '6'인 경우 썸네일 이미지 형식은 JPEG입니다. 대부분의 Exif 이미지는 썸네일로 JPEG 형식을 사용합니다. 이 경우 IFD1의 JpegIFOffset(0x0201) 태그로 썸네일의 오프셋을, JpegIFByteCount(0x0202) 태그로 썸네일의 크기를 얻을 수 있습니다. 데이터 형식은 일반 JPEG 형식으로 0xFFD8에서 시작하여 0xFFD9로 끝납니다. JPEG 형식과 160x120픽셀 크기가 Exif2.1 이상에서 권장되는 썸네일 형식인 것 같습니다.

##### TIFF 형식 썸네일 #####

IFD1의 Compression(0x0103) Tag 값이 '1'인 경우 썸네일 이미지 형식은 압축되지 않은 형식(TIFF 이미지라고 함)입니다. 썸네일 데이터의 시작점은 StripOffset(0x0111) Tag이고, 썸네일의 크기는StripByteCounts(0x0117) Tag의 합입니다.

## 참조 ##

* [EXIF - 위키피디아 작성](https://en.wikipedia.org/wiki/Exif)
* [EXIF 파일 형식](https://www.media.mit.edu/pia/Research/deepview/exif.html)

