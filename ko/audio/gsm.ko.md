{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "파일", "확장자", "형식", "오디오", "모바일 오디오용 글로벌 시스템", "gsm 확장자", "gsm 파일"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"GSM 파일을 만들고 열 수 있는 GSM 파일 형식과 API에 대해 알아보세요.",
  "title" :"GSM - 모바일 오디오 파일 형식을 위한 글로벌 시스템",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## .GSM 파일이란?

GSM은 Global System for Mobile Audio Format Files와 관련된 파일 확장자입니다. GSM 확장자가 포함된 파일은 Linux, Windows 및 Mac OS 플랫폼에서 열 수 있습니다. GSM 파일 형식은 오디오 파일 카테고리에 속합니다.

GSM 파일은 손실 CBR(고정 비트 전송률) 사운드 압축 코덱으로 인코딩됩니다. GSM 오디오 파일의 샘플 속도는 8000샘플/초인 반면 데이터 속도는 약 13kbps입니다. GSM 파일 내의 비트 전송률은 음성 녹음 중 품질을 보장합니다. 또한 GSM 파일 형식은 휴대폰에서 사용되는 글로벌 표준 형식으로도 알려져 있으며 WAV 파일도 GSM 파일 형식을 사용하여 쉽게 인코딩할 수 있습니다. GSM 파일의 모든 문제는 전문가에게 가지 않고도 사용자가 직접 쉽게 해결할 수 있습니다.

사용자는 GSM 파일을 [MP3](/ko/audio/mp3/) 및 [MP4](/ko/video/mp4/) 형식으로 변환할 수도 있습니다.

## GSM 파일 형식의 간략한 역사

GSM은 유럽에서 인터넷 전화용으로 만들어진 오디오 파일 형식입니다. ETSI(European Telecommunications Standard Institute)에서 휴대폰 및 태블릿에 사용되는 2G 디지털 셀룰러로 사용하기 위해 개발했습니다. 오늘날에는 전화 대화 및 음성 메시지의 녹음을 저장하는 데 사용됩니다.

## GSM 파일 형식 사양 ##

GSM은 다음 섹션으로 구성된 구조화된 네트워크에서 작동합니다.

- **변조** : 입력 데이터를 쉽게 전송할 수 있는 형식으로 변환하는 과정입니다. 전송된 데이터는 수신단에서 복조됩니다.
- **전송 속도** : GSM은 270kbps 이상의 비트 전송률을 갖는 디지털 시스템입니다.
- **업링크 주파수 범위**: 933-960MHz
- **다운링크 주파수 범위**: 890 – 915MHz
- **Channel Spacing** : 약 200kHz가 되어야 하는 인접 장벽 사이의 간격을 의미
- **Duplex Distance** : 80MHz가 되어야 하는 상향링크와 하향링크 주파수 사이의 공간입니다.
- **음성 코딩** : GSM은 LPC(Linear Predictive Coding)를 사용합니다. LPC는 비트 전송률을 압축합니다. 오디오 신호가 필터를 통과하여 성대를 모방할 때. GSM은 13kbps로 음성을 인코딩합니다.

| 오디오 압축 형식 | 알고리즘 | 샘플 속도 | 비트 전송률 변환 | 대기 시간 | CBR | VBR | 스테레오 | 다채널 |
| ------------------------ | ---------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8kHz | 5.6kbit/s | 25ms | 예 | 아니오 | 아니오 | 아니오 |
| GSM-FR | RPE-LTP | 8kHz | 13kbit/s | 20–30ms | 예 | 아니오 | 아니오 | 아니오 |
| GSM-EFR | ACELP | 8kHz | 12.2kbit/s | 20–30ms | 예 | 아니오 | 아니오 | 아니오 |

## 참조 ##

* [GSM - 위키백과 제공](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

