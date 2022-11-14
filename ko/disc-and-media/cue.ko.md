{
  "date" : "2021-06-09",
  "keywords" :[ "큐", "파일", "확장자", "형식", "큐 파일이란", "음악", "큐 파일 형식", "큐 파일 형식 사양", "큐 시트", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"CUE 파일을 생성, 변환 및 열 수 있는 CUE 파일 형식 및 API에 대해 알아보세요.",
  "title" :"CUE - 큐 시트 파일",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## .CUE 파일이란?

큐 시트 파일이라고도 하는 확장자가 .cue인 파일은 CD 또는 DVD의 트랙 레이아웃에 대한 정보가 포함된 메타데이터 파일입니다. 미디어 플레이어 및 광 디스크 저작 응용 프로그램에서 지원됩니다. CD에 저장된 주요 오디오 데이터는 트랙 길이, 디스크 제목 및 연주자의 사양과 함께 큐 파일에 의해 참조됩니다. 따라서 단일 오디오 파일에 여러 트랙이 포함된 경우 큐 파일을 사용하여 오디오를 여러 파일로 나누거나 다양한 트랙을 참조할 수 있습니다.

## CUE 파일 형식

CUE 또는 큐 시트 파일은 사람이 읽을 수 있는 일반 텍스트 형식으로 저장됩니다. 큐 파일의 정보는 하나 이상의 매개변수가 있는 명령입니다. 이러한 명령은 특정 명령 및 컨텍스트에 따라 전체 파일 또는 개별 트랙에 적용됩니다. CDRWIN 사용자 가이드는 큐 시트 구문 및 의미에 대한 사양을 설명합니다.

## CUE 시트 필수 명령

|명령|설명|
---|---|
|파일| [MP3](/ko/audio/mp3/), [WAV](/ko/audio/wav/) 또는 일반 바이너리 디스크 이미지)|와 같은 데이터 및 해당 형식을 포함하는 파일을 나타냅니다.
|트랙| 번호 및 유형 또는 모드와 같은 트랙 컨텍스트 정보를 정의합니다.|
|색인| FILE 내의 인덱스로 위치를 나타냅니다. 형식은 mm:ss:ff(분-초 프레임)입니다.|
|PREGAP 및 POSTGAP|데이터 파일에 저장되지 않은 트랙의 pregap 또는 post-gap을 나타냅니다. 길이는 INDEX와 동일한 분-초 프레임 형식으로 지정됩니다.|

### CUE 시트 예

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## 참고문헌

* [.cda 파일 - 위키피디아 작성](https://en.wikipedia.org/wiki/.cda_file)

