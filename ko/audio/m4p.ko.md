{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "파일", "확장자", "형식", "m4p 파일 형식이란", "음악", "m4p 파일 형식", "M4b 대 MP3", "m4p 파일 형식 사양 "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4P 파일을 생성, 변환 및 열 수 있는 M4P 파일 형식 및 API에 대해 알아보세요.",
  "title" :"M4P - MPEG-4 오디오북 파일 형식",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## .M4P 파일이란?
확장자가 .m4p인 파일은 일반적으로 Apple iTunes Store에서 다운로드할 수 있는 오디오 파일입니다. 즉, M4P는 AAC 파일이지만 DRM(디지털 권한 관리)을 사용하여 복사 방지되어 있다고 말할 수 있습니다. M4P 파일은 승인된 시스템 또는 장치에서만 재생할 수 있음을 의미합니다. 일반적으로 M4P 파일은 Apple 멀티미디어 장치에만 해당됩니다. 따라서 이러한 파일은 Apple 맥북, 팟캐스트, iPhone 6 또는 iPhone 7과 같은 스마트폰에서만 재생할 수 있습니다.

## M4P 파일 형식
M4P는 MPEG 4 Protected(오디오)의 약자로서 고급 오디오 코덱(AAC)으로 오디오를 인코딩하고 파일의 무단 사용을 방지합니다. 이 파일 형식은 일반적으로 iTunes Music Store의 오디오 파일 형식으로 간주됩니다. Apple은 FairPlay DRM(디지털 권한 관리) 시스템을 사용하여 M4P 파일을 보호합니다. FairPlay DRM은 Veridisc에서 개발한 기술을 기반으로 합니다. 보호 메커니즘은 AES 암호화를 사용하여 AAC 오디오 스트림을 암호화하여 작동합니다. 사용자는 암호 해독을 위해 자신의 계정에 할당된 마스터 키를 받습니다. 이 파일 형식은 MP3가 원래 오디오 파일로 의도된 것이 아니라 MPEG 1 또는 2 비디오 파일에서 레이어 III로 사용되었기 때문에 MP3 파일 형식을 대체하기 위해 도입되었습니다.


## M4P 파일 형식 사양

[M4A](/ko/audio/m4a/)와 유사하게 M4P 파일도 연속적인 청크로 구성됩니다. 각 청크는 8바이트 헤더를 가지며 다음과 같이 세분화됩니다.
- 4바이트 청크 크기(빅 엔디안, 상위 바이트 먼저)
- 4바이트 청크 유형 - 사전 정의된 서명 중 하나: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "와이드", "로드", "imap", "매트", "chap", "kmat", "클립", "crgn", "동기화", "tmcd", "PICT", "scpt" ", "ctab", "ssrc".

M4A와 유사하게 M4P의 첫 번째 청크는 유형 "ftype"이고 오프셋 8에 하위 유형이 있습니다. 하위 유형에 의해 정의된 M4P는 "M4P_"여야 합니다.

알 수 없는 유형의 청크가 감지될 때까지 청크를 반복하여 M4P(MPEG-4 오디오) 파일을 구성합니다.

## 참조 ##

* [MPEG-4 14부 - 위키피디아 작성](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 오디오(M4A,M4B,M4P) 포맷 및 복구 예](https://www.file-recovery.com/m4a-signature-format.htm)

