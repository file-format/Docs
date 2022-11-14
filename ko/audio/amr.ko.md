{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "파일", "확장자", "형식", "amr 파일이란", "음악", "amr 파일 형식", "amr 파일","amr 파일을 다음으로 변환 mp3", "amr 파일 재생"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AMR 파일을 생성, 변환 및 열 수 있는 AMR 파일 형식 및 API에 대해 알아보세요.",
  "title" :"AMR - 적응형 다중 속도 코덱 파일",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## .AMR 파일이란?
확장자가 .amr인 파일은 **Adaptive Multi-Rate** 오디오 코덱과 관련된 오디오 데이터 형식입니다. 7.4kbit/s에서 시작하는 유료 품질 음성으로 4.75-12.2kbit/s 비트 속도로 협대역 신호를 인코딩하는 다중 속도 협대역 음성 코덱으로 구성됩니다. 링크 적응을 사용하여 기반으로 8개의 다른 비트 전송률 중 하나를 선택합니다.

## AMR 파일 형식
AMR 파일 형식은 최고의 기술 중 하나인 ACELP(Algebraic Code Excited Linear Prediction) 알고리즘과 같은 많은 코딩 기술을 사용합니다. 사람의 음성을 보다 효율적인 방식으로 압축하도록 설계되었습니다. AMR은 1999년 3GPP에 의해 표준 음성 또는 음성 코덱으로 설정되었습니다. AMR 파일 형식은 또한 많은 스마트폰에서 녹음을 저장하는 데 사용하는 **Adaptive Multi-Rate** 오디오 코덱을 사용하여 음성 오디오를 저장하는 데 사용됩니다. 연설.

### 파일 형식 구조
AMR(Adaptive Multi-Rate)은 오디오 형식입니다. 다양한 모바일 응용 프로그램 및 장치, 일반적으로 오디오 플레이어/레코더 또는 VoIP 종류의 응용 프로그램에 널리 사용됩니다. AMR은 다음과 같이 추가로 분류할 수 있습니다.

1. AMR-NB(협대역)
2. AMR-WB(광대역)

일반적으로 AMR은 AMR-NB를 나타냅니다. AMR 파일 형식의 구조는 다음과 같습니다.

각 AMR 파일에는 파일을 AMR 오디오로 인식하는 6바이트 헤더가 있습니다. 이 헤더는 항상 다음으로 설정됩니다.
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

이것은 일반적으로 모든 AMR-NB 파일에서 유사합니다. 헤더가 표준을 따르는 경우 파일이 손상되었을 가능성이 있으므로 사용해서는 안 됩니다. AMR 파일은 압축된 오디오 프레임의 정수로 구성됩니다. 이 프레임은 각각 20ms의 오디오를 구성합니다. 각 프레임은 유효한 AMR-NB 모드(DTX 모드에서 0-7, 8 SID)를 사용하여 인코딩할 수 있습니다. 프레임은 다른 비트 레이트로 인코딩될 수 있으므로 이 일반적인 방법을 AMR(Adaptive Multi-Rate)이라고 합니다.
#### AMR 모드
다음은 다양한 AMR 모드와 해당 비트 전송률입니다.

|모드| 비트율|
---|---|
|0| AMR 4.75 - 4.75kbit/s로 인코딩|
|1 | AMR 5.15 - 5.15kbit/s로 인코딩|
|2 | AMR 5.9 - 5.9kbit/s로 인코딩|
|3 | AMR 6.7 - 6.7kbit/s로 인코딩|
|4 | AMR 7.4 - 7.4kbit/s로 인코딩|
|5 | AMR 7.95 - 7.95kbit/s로 인코딩|
|6 | AMR 10.2 - 10.2kbit/s로 인코딩|
|7 | AMR 12.2 - 12.2kbit/s로 인코딩|

AMR 모드의 프레임 크기(헤더 바이트 포함)는 다음과 같습니다.

|CMR |모드 |프레임 크기(바이트)|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## 참조 ##

* [Adaptive Multi-Rate 오디오 코덱 - 위키피디아 작성](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [AMR 및 AMR-WB 오디오 코덱의 RTP 페이로드 형식 및 파일 저장 형식](https://tools.ietf.org/html/rfc4867#page-35)

