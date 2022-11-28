{
  "date" : "2019-10-11",
  "keywords" :[ "tga 파일", "tga 파일 형식", "tga 파일이란", "파일", "tga 예제", "tga 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA 파일 형식 - TARGA 그래픽 이미지 파일",
  "description":"TGA 파일 형식과 TGA 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .TGA 파일이란?

확장자가 .tga인 파일은 래스터 그래픽 형식이며 Truevision Inc.에서 만들었습니다. TARGA(Truevision Advanced Raster Adapter) 보드용으로 설계되었으며 IBM 호환 PC에 하이컬러/트루컬러 디스플레이 지원을 제공했습니다. 픽셀당 8, 16, 24, 32비트와 8비트 알파 채널을 지원합니다. 또한 이미지 크기를 줄이기 위해 적용할 수 있는 무손실 RLE 압축을 지원합니다. 디지털 사진과 질감은 TGA 이미지 형식을 사용합니다.

## 약력

TGA 파일 형식은 1984년 AT&T에서 컬러 프레임 버퍼용으로 개발한 신기술의 마케팅에 참여하고 있던 AT&T EPICenter(나중에 Truevision으로 알려진 독립 법인으로 추출 및 형성됨)에 의해 형성되었습니다. EPICenter는 이미 VDA(비디오 디스플레이 어댑터) 및 ICB(이미지 캡처 보드)라는 두 가지 파일 형식에 대한 작업이 이미 진행 중인 처음 두 카드에 대해 작업하고 있었습니다. 이러한 파일 형식은 성문화되었고 덜 광범위한 특정 파일 형식 TGA가 도입되었습니다. TGA는 이미 사용 중인 확장 기능으로 너비, 높이, 픽셀 깊이, 관련 색상 맵 및 이미지 원점과 같은 정보를 제공했습니다.

1989년에 출판된 TGA의 2.0 버전은 다음과 같은 몇 가지 향상된 기능을 통합했습니다.

* 썸네일
* 알파 채널
* 감마 값
* 텍스트 메타데이터

TGA 2.0 버전의 주요 기여자는 Truevision의 Shawn Steiner, Kevin Fiedly 및 David Spoelstra입니다.

## TGA TARGA 파일 형식 사양

TGA 파일은 두 가지 주요 부분으로 구성됩니다.

* 헤더
* 색상 픽셀 정보

TGA 파일의 모든 값은 형식 사양에 따라 littl-endian입니다.

### TGA 헤더

TGA 파일 헤더는 다음 5개 필드로 구성됩니다.

|필드 번호|길이 |필드 이름 |설명|
---|---|---|---|
|1| 1바이트 |ID 길이| 이미지 ID 필드의 길이(0-255)|
|2| 1바이트 |컬러맵 유형| 컬러 맵이 포함되어 있는지 여부(0 - 이 이미지에 컬러 맵 데이터가 포함되어 있지 않음을 나타냅니다. 1 - 이 이미지에 컬러 맵이 포함되어 있음을 나타냅니다.)|
|3| 1바이트 |이미지 유형| 압축 및 색상 유형(0- 포함된 이미지 데이터 없음. 1- 비압축, 컬러 매핑 이미지, 2- 비압축, 트루 컬러 이미지, 9- 실행 길이 인코딩, 컬러 매핑 이미지, 11- 실행 길이 인코딩, 흑백 이미지 )|
|4| 5바이트 |컬러맵 사양| 색상 맵 설명|
|5| 10바이트 |이미지 사양| 이미지 크기 및 형식|

### 이미지 및 색상 맵 데이터

|필드 번호 |길이 |필드 |설명|
---|---|---|---|
|6 |이미지 ID 길이 필드에서| 이미지 ID| 식별 정보가 포함된 선택적 필드|
|7 |컬러 맵 사양 필드에서| 컬러맵 데이터| 컬러 맵 데이터가 포함된 조회 테이블|
|8 |이미지 사양 필드에서| 이미지 데이터| 이미지 설명자에 따라 저장됨|

### 개발자 영역(선택 사항)

TGA 버전 2.0은 많은 개발자가 더 많은 정보를 저장하기를 원하는 추가 향상/추가 기능을 지원합니다. 정보는 선택 사항이므로 TGA 디코더가 해석할 수 없는 경우 무시됩니다.

### 확장 영역(선택 사항)

|필드 번호| 길이| 필드 |설명|
---|---|---|---|
|10| 2바이트 |확장 크기 |확장 영역의 크기(바이트), 항상 495|
|11| 41바이트| 저자 이름 |저자의 이름. 사용하지 않는 경우 바이트를 NULL(\0) 또는 공백으로 설정해야 합니다.
|12| 324바이트| 작가 코멘트| 4줄로 구성된 주석은 각각 80자에 NULL|
|13| 12바이트| 날짜/시간 스탬프 |이미지가 생성된 날짜 및 시간|
|14| 41바이트| 작업 ID||
|15| 6바이트| 작업 시간| 파일 생성에 소요된 시간, 분, 초(청구 등)|
|16| 41바이트| 소프트웨어 ID |파일을 생성한 응용 프로그램.|
|17| 3바이트| 소프트웨어 버전||
|18| 4바이트| 키 색상||
|19| 4바이트| 픽셀 종횡비||
|20| 4바이트| 감마 값||
|21| 4바이트| 색상 보정 오프셋 |파일 시작 부분부터 색상 보정 테이블(있는 경우)까지의 바이트 수|
|22| 4바이트| 우표 | 파일의 시작 부분부터 우표 이미지(있는 경우)까지의 바이트 수|
|23| 4바이트| 스캔 라인 오프셋| 파일의 시작부터 스캔 라인 테이블(있는 경우)까지의 바이트 수|
|24| 1바이트| 속성 유형| 알파 채널을 지정합니다|

### 파일 바닥글(선택 사항)

파일의 마지막 26바이트는 바닥글을 나타내며, 있는 경우 TGA 버전 2 파일일 가능성이 높습니다.

|필드 번호| 길이| 필드| 설명|
---|---|---|---|
|28| 4바이트| 확장 오프셋| 파일 시작부터 오프셋(바이트)|
|29| 4바이트| 개발자 영역 오프셋| 파일 시작부터 오프셋(바이트)|
|30| 16바이트| 서명| "TRUEVISION-XFILE" 포함|
|31| 1바이트| | "." 포함|
|32| 1바이트| | NULL 포함|


## 참고문헌

* [TGA 2.0 파일 형식 사양](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [위키피디아의 TGA](https://en.wikipedia.org/wiki/Truevision_TGA)
