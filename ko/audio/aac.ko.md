{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "파일", "확장자", "형식", "오디오 코딩", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AAC 파일을 만들고 열 수 있는 AAC 파일 형식 및 API에 대해 알아보세요.",
  "title" :"AAC - 고급 오디오 코딩 파일",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## .AAC 파일이란?

AAC(Advanced Audio Coding)는 손실 오디오 압축을 기반으로 오디오 파일을 나타내는 디지털 오디오 코딩 표준을 말합니다. **[MP3](/ko/audio/mp3/)** 파일 형식의 후속 제품으로 출시되었으며 데이터 압축 방법의 개발을 기반으로 하는 인코딩 프로세스에서 새로운 아이디어를 구현하는 데 측면에서 문제가 있음을 고려합니다. AAC는 동일한 비트 전송률에서 MP3에 비해 더 나은 음질을 제공합니다. MPEG-2 Part 7(ISO/IEC 13818-7)과 MPEG-4 Part 3(ISO/IEC 14496-3)의 업데이트된 형식으로 정의되었습니다.

AAC 형식은 YouTube, iPhone, iPod, iPad, Apple iTunes 및 기타 여러 플랫폼에서 기본 미디어 형식으로 채택되었습니다. AAC 파일 형식을 MP3, WMA, M4A, **[WAV](/ko/audio/wav/)** 등과 같은 다른 형식으로 변환하는 데 여러 응용 프로그램과 API를 사용할 수 있습니다.

### AAC 파일의 간략한 역사

AAC 파일 형식은 일부 개선된 MP3의 향상된 버전입니다. Fraunhofer Institute(Fraunhofer IIS - MP3 개발자), Nokia, Dolby, AT&T 및 Sony를 비롯한 여러 회사에서 기여한 이 형식은 1997년 4월 MPEG(Moving Picture Experts Group)에서 국제 표준으로 선언되었습니다. 1999년 후반, MPEG-2 Part 7은 업데이트되어 MPEG-4 표준 제품군에 포함되었습니다. ISO/IEC 14496-3: 1999 또는 MPEG-4 오디오로 식별되는 MPEG-4 파트 3으로 알려졌습니다.

## AAC 파일 형식 사양

AAC 파일 형식 사양은 MP3보다 코덱을 설계하는 데 더 많은 유연성을 허용하므로 더 많은 동시 인코딩 전략과 효율적인 압축이 가능합니다. 이 형식은 더 적은 비트 전송률에서도 더 많은 옵션을 지원한다는 점에서 MP3보다 개선된 여러 하드웨어 플랫폼에서 선택되었습니다. AAC 파일 형식 사양은 [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) 및 [MPEG-4 Part 3](https://www.iso.org)로 제공됩니다. /standard/53943.html)(무료로 다운로드할 수 없음). 형식은 다음 미디어 유형을 사용합니다.

* 오디오/AAC
* 오디오/aacp
* 오디오/3gpp
* 오디오/3gpp2
* 오디오/mp4
* 오디오/mp4a-latm
* 오디오/mpeg4-일반

## AAC 대 MP3 - 개선 사항 ##

개선 측면에서 AAC와 MP3의 주요 차이점은 다음과 같습니다.

* AAC는 더 넓은 범위의 채널(최대 48개) 및 샘플링 속도(8kHz ~ 96kHz)를 지원합니다.
* AAC는 16kHz 이상에서 더 나은 코딩 주파수를 가집니다.
* AAC는 오디오 신호의 과도 및 고정 부분에 대한 코딩을 개선하는 필터 뱅크의 주파수-시간 분해능의 변동 한계가 더 넓습니다.
* 보다 효율적이고 단순한 필터 뱅크: 하이브리드 필터 뱅크가 표준 MDCT(수정된 이산 코사인 변환)로 대체되었습니다.
* TNS(Temporal Noise Shaping), MDCT 시간의 예측 계수(장기 예측), 파라메트릭 스테레오, 지각 노이즈 대체, 스펙트럼 대역 복제(SBR)를 사용하여 압축의 향상된 효율성을 지원합니다.
* 더 유연한 조인트 스테레오(다른 주파수 범위에서 다른 방법을 사용할 수 있음)

## 참조 ##

* [AAC - 위키피디아 작성](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

