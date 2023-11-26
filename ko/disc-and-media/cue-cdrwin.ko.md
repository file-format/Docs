{
"날짜":"2023-10-18",
   "keywords":[
"큐",
"큐 파일",
"큐 cdrwin 큐 시트 파일",
"큐 파일을 여는 방법",
"파일",
"큐 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title":"CUE 파일 형식 - CDRWIN 큐 시트",
   "description":"CUE CDRWIN 큐 시트 파일 형식과 CUE 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
"parent":"디스크 및 미디어"
}
},
"lastmod":"2023-10-18"
}

## .CUE 파일이란?

**CDRWIN 큐 시트**라고도 알려진 **.CUE** 파일은 일반적으로 BIN 또는 ISO 형식의 오디오 CD 또는 디스크 이미지의 트랙 및 레이아웃에 대한 정보를 포함하는 일반 텍스트 파일입니다. 이러한 파일은 디스크의 구조와 내용을 설명하는 데 자주 사용되므로 CD 굽기 소프트웨어 또는 가상 드라이브 소프트웨어가 원본 디스크를 정확하게 재현할 수 있습니다.

## CUE 파일의 예

다음은 ".cue" 파일의 모양에 대한 예입니다.

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN 큐 시트

CDRWIN 큐 시트는 CDRWIN 소프트웨어에서 사용되는 ".cue" 파일 형식의 특정 변형입니다. CDRWIN은 CD/DVD 굽기 및 저작 소프트웨어이며 ".cue" 시트는 이 소프트웨어와 함께 사용하도록 설계되었습니다. 이러한 ".cue" 시트에는 CDRWIN이 CD 또는 DVD를 정확하게 생성하거나 굽는 데 필요한 정보가 포함되어 있습니다.

CDRWIN 큐 시트와 관련된 몇 가지 주요 세부 정보는 다음과 같습니다.

1. **CDRWIN의 고유**: CDRWIN의 ".cue" 시트는 CDRWIN 소프트웨어에 특정한 독점 형식입니다. 표준 ".cue" 파일과 유사점을 공유하지만 CDRWIN의 기능 및 설정과 함께 작동하도록 맞춤화되었습니다.
    






2. **사용자 친화적인 인터페이스**: CDRWIN은 ".cue" 시트를 생성하고 편집하기 위한 사용하기 쉬운 인터페이스를 제공합니다. 사용자는 트랙, 인덱스, 간격 및 기타 매개변수에 대한 정보를 사용자 친화적인 방식으로 추가하거나 수정할 수 있습니다.
    






3. **호환 가능한 디스크 유형**: CDRWIN 큐 시트는 주로 데이터 디스크, 오디오 CD, 혼합 모드 디스크 등을 포함한 다양한 유형의 CD 및 DVD를 만드는 데 사용됩니다. 이 형식을 통해 사용자는 생성하려는 디스크의 유형과 내용을 지정할 수 있습니다.
    






4. **디스크 레이아웃 제어**: CDRWIN 큐 시트는 트랙 순서, 일시 정지/간격 설정 및 사용자가 가질 수 있는 기타 특정 기본 설정을 포함하여 디스크의 레이아웃과 구조에 대한 세부적인 제어 기능을 제공합니다.
    






5. **ISO 및 BIN 지원**: CDRWIN은 ISO 및 BIN 디스크 이미지 형식 모두에서 작동할 수 있습니다. ".cue" 시트는 디스크에 사용되는 이미지 파일을 지정하여 큐와 이미지 간의 적절한 동기화를 보장합니다.
    






6. **굽기 및 리핑**: 이 ".cue" 시트는 CDRWIN을 사용하여 디스크를 굽거나 디스크에서 트랙을 리핑할 때 매우 중요합니다. 이는 최종 제품이 의도한 레이아웃 및 콘텐츠와 일치하는지 확인하는 데 도움이 됩니다.
    






7. **백업 및 복원**: CDRWIN 사용자는 CD나 DVD를 백업할 때 ".cue" 시트를 만드는 경우가 많습니다. 이 시트는 나중에 트랙 레이아웃 및 타이밍을 포함하여 디스크 콘텐츠를 복원하는 데 사용될 수 있습니다.

## CUE 파일을 여는 방법?

CDRWIN 큐 시트는 CDRWIN 소프트웨어용으로 특별히 설계되었으므로 일반적으로 CDRWIN 내에서 열어서 사용하도록 되어 있습니다.

CUE 파일을 열거나 참조하는 프로그램

- CDRWIN
- 스마트 프로젝트 IsoBuster
- EZB 시스템 UltraISO

## 기타 CUE 파일

**.cue** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

**디스크 및 미디어**
- [CUE - 큐 시트 파일](/ko/disc-and-media/cue/)
- [CUE - CDRWIN 큐 시트](/ko/disc-and-media/cue-cdrwin/)

## 참고자료
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

