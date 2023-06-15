{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "파일", "확장자", "형식", "오디오 교환 파일 형식", "음악", "aiff 파일 형식", "aiff를 mp3로", "aiff 대 wav", "aiff를 다음으로 변환 mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AIFF 파일을 생성, 변환 및 열 수 있는 AIFF 파일 형식 및 API에 대해 알아보세요.",
  "title" :"AIFF - 오디오 교환 파일 형식",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## .AIFF 파일이란?
AIFF(Audio Interchange File Format)는 1998년 Apple에서 개발한 비압축 오디오 파일 형식이지만 Amiga 시스템에서 사용되는 래퍼 형식인 **EA IFF 85**(Electronic Arts에서 개발한 표준 교환 형식 파일)를 기반으로 합니다. . 이 파일 형식은 샘플링된 사운드를 저장하기 위한 표준을 제공합니다. 이 형식은 유연성이 충분하고 다양한 샘플 속도와 샘플 너비에서 모노 또는 다중 채널 샘플 사운드를 저장할 수 있습니다. AIFF 파일은 압축되지 않기 때문에 [MP3](/audio/mp3/)와 같은 다른 손실 형식보다 크기가 커집니다.

AIFF 파일은 44.1khz로 녹음된 16비트 샘플 크기의 비압축 스테레오 오디오 채널 2개로 구성됩니다. 고품질 오디오 때문에 5분짜리 오디오는 [WAV](/audio/wav/) 파일 형식과 유사한 최대 50MB의 디스크 공간을 차지할 수 있습니다.

## AIFF 대 WAV

AIFF와 WAV는 품질면에서 거의 동일합니다. 둘 다 동일한 PCM(펄스 코드 변조) 인코딩을 사용하므로 [MP3](/audio/mp3/)와 같은 다른 손실 형식에 비해 크기가 더 큽니다. [M4A](/audio/m4a/). 일반적인 차이점 중 일부는 아래 표에 나와 있습니다.

|AIFF|WAV|
---|---|
|MAC에 주로 사용|PC에 주로 사용|
|메타데이터 허용| 메타데이터를 허용하지 않음|

## AIFF 파일 구조

**EA IFF 85**는 데이터를 파일에 저장하기 위한 전체 구조를 설정합니다. **EA IFF 85** 파일은 여러 데이터 청크로 구성됩니다. AIFF 파일의 청크 블록은 일부 헤더 정보와 그 뒤에 오는 데이터로 구성됩니다.
{{< figure src="../chunk.png" alt="AIFF 청크" >}}

AIFF 파일은 다양한 유형의 청크 모음입니다. AIFF 파일 청크를 형성하는 데 중요한 두 가지 일반적인 유형의 청크가 있습니다.
- **Common Chunk**: 길이 및 샘플 속도와 같이 샘플링된 사운드를 설명하는 중요한 매개변수를 포함합니다.
- **Sound Data Chunk**: 실제 오디오 샘플을 포함합니다.
기기 매개변수를 나열하고, 마커를 정의하고, 애플리케이션별 정보를 저장하는 등의 다른 많은 선택적 청크가 있습니다.

### 로컬 청크 유형

AIFF를 형성하는 청크 유형은 아래 표에 나와 있습니다.

|청크 유형| 설명|
---|---|
|공통 청크|공통 청크는 샘플링된 사운드의 기본 매개변수를 설명합니다|
|사운드 데이터 청크|사운드 데이터 청크에는 실제 샘플 프레임이 포함되어 있습니다.|
|Marker Chunk|Marker Chunk에는 사운드 데이터의 위치를 가리키는 마커가 포함되어 있습니다.|
|Instrument Chunk|Instrument Chunk는 샘플러와 같은 악기가 사운드 데이터를 재생하는 데 사용할 수 있는 기본 매개변수를 정의합니다.|
|MIDI 데이터 청크|MIDI 데이터 청크는 MIDI 데이터를 저장하는 데 사용할 수 있습니다.|
|오디오 녹음 청크|오디오 녹음 청크에는 오디오 녹음 장치와 관련된 정보가 들어 있습니다.|
|Application Specific Chunk|Application Specific Chunk는 응용 프로그램 제조업체에서 어떤 용도로든 사용할 수 있습니다.|
|Comments Chunk|Comments Chunk는 FORM AIFF|에 주석을 저장하는 데 사용됩니다.
|텍스트 청크 - 이름, 작성자, 저작권, 주석| 모두 텍스트 청크|

## 참조 ##

* [오디오 교환 파일 형식 - 위키피디아 작성](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

