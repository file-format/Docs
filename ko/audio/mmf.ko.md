{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "파일", "확장자", "형식", "오디오", "smaf", "mmf 확장자", "mmf 파일", "모바일 음악 파일", "야마하"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MMF 파일을 만들고 열 수 있는 MMF 파일 형식 및 API에 대해 알아보세요.",
  "title" :"MMF - 모바일 음악 파일 형식",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## .MMF 파일이란?

MMF는 SMAF 파일과 관련된 파일 확장자입니다. MMF는 Mobile Music File의 약자이고 SMAF는 합성 음악 Mobile Application Format의 약자입니다. 스마트폰 내의 MMF 파일에는 시스템 벨소리, 사운드가 포함되어 있으며 그래픽 및 텍스트 표시도 포함될 수 있습니다. MMF에는 FM, PCM 및 Stream PCM을 포함한 세 가지 유형의 기기 매개변수가 포함되어 있습니다. 이러한 파일 형식은 Windows 시스템 플랫폼과 호환됩니다. MMF 파일은 데이터 파일로 분류됩니다. 일반적으로 Microsoft Mail은 MMF 파일을 지원합니다. MMF 접미사가 있는 파일은 모든 모바일 장치 또는 시스템 플랫폼에 복사할 수 있습니다.

또한 이러한 파일은 표준 MIDI 형식 파일에 비해 크기가 훨씬 작습니다. [WAV](/ko/audio/wav/) 및 [MID](/ko/audio/mid/) 파일을 MMF 형식으로 변환하여 오디오 콘텐츠로 공유 및 배포할 수 있습니다. 이 파일은 이메일을 통해 휴대폰과 PC로 직접 수신할 수 있습니다.


## MMF 파일 형식의 간략한 역사

Yamaha는 스마트폰이 더 많은 고유한 벨소리를 저장할 수 있도록 SMAF 도구를 사운드 파일로 개발했습니다. Yamaha는 MA-1, MA-2, MA-3, MA-5 및 MA-7 LSI 사운드 칩을 생산하면서 SMAF를 도입했습니다. 이러한 모든 형식은 2000년 초 동아시아 시장에서 휴대전화에 매우 친숙해졌습니다.

국제적 수준에서 MMF 형식은 삼성에 의해 승인되었습니다. MMF 형식의 도움으로 삼성은 삼성 스마트폰에서 사용할 다양한 다성 벨소리를 디자인할 수 있었습니다.

Yamaha는 이 형식을 더욱 대중적으로 만들고자 공식 Yamaha SMAF 파일에 이 형식과 호환되는 더 많은 도구를 게시했습니다. 이 사용자는 이제 컴퓨터에서 MMF 파일을 쉽게 재생할 수 있습니다.


## MMF 파일 형식 사양 ##

MMF 파일은 데이터 섹션으로 분류됩니다. 8바이트 주변의 접두사 구조는 각 세그먼트를 설명하는 데 사용됩니다.
4바이트 레이블에는 CNTI, OPDA, MSTR, MTR 및 ATR이 포함됩니다. 데이터 크기에 8바이트를 더한 값은 청크 크기입니다. 전체 파일 크기는 모든 청크 크기를 합산하여 계산됩니다. 파일이 손상되지 않은 경우 합산된 파일 크기는 기본 헤더 크기와 같아야 합니다.

### 헤더 ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

다음은 MMF 파일의 예입니다.

![](../mmf.png)

## 참고문헌

* [MMF - 위키피디아 작성](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

