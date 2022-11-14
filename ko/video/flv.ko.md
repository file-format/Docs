---
date: 2019-10-11
keywords: flv, .flv, flv 파일 형식, .flv 파일 형식, .flv 확장자, flv 확장자, flv 비디오 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLV 파일 형식과 FLV 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: FLV 파일 형식
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## .FLV 파일이란? ##

FLV(Flash Video)는 확장자가 .flv인 컨테이너 파일 형식입니다. FLV는 Adobe Flash Player 또는 Adobe Air를 사용하여 인터넷을 통해 오디오/비디오 콘텐츠를 전달하는 데 사용됩니다. FLV 파일의 데이터는 SWF 파일과 동일한 방식으로 인코딩됩니다. 2003년 Flash Player 7에 직접 지원이 추가되었습니다. Adobe 시스템은 FLV의 제한으로 인해 2007년에 F4V를 만들었습니다.

### 인코딩 ###

FLV 파일에는 H.263 비디오 표준의 독점 변형인 Sorenson Spark의 비디오 비트스트림이 포함되어 있습니다. Flash Player 6 및 7에 필요한 압축 형식입니다. Flash Player 버전 8은 On2 TrueMotion VP6 비디오 비트스트림을 지원합니다. Flash Player 8 이상에 권장되는 압축 형식입니다. FLV는 MP3, Nellymoser Asao 코덱 및 오픈 소스 Speex 코덱의 오디오를 지원합니다. 또한 압축되지 않은 오디오 또는 ADPCM 형식의 오디오를 지원합니다. AAC(HE-AAC/AAC SBR, AAC 기본 프로필 및 AAC-LC)는 최신 버전의 Flash Player 9에서 지원됩니다.

## 구조 ##

FLV 파일은 헤더와 패킷으로 구성됩니다. FLV 파일은 헤더로 시작합니다. 헤더에는 다음 필드가 있습니다.

- **서명**: 값은 FLV입니다.
- **버전**: 기본값은 1입니다. 0x01만 유효합니다.
- **플래그**: 0x04는 오디오에 사용되고 0x01은 비디오에 사용되므로 0x05는 오디오와 비디오 모두에 사용됩니다.
- **Header Size**: 기본값은 9입니다. 새로 확장된 헤더를 건너뛸 때 사용합니다.

헤더 다음에 패킷이 옵니다. FLV 파일은 15바이트 헤더가 있는 FLV 태그라는 여러 패킷으로 분할됩니다. 패킷에는 오디오, 비디오, 스크립트, 암호화 정보 및 페이로드에 대한 메타데이터가 포함됩니다. FLV 패킷에는 다음 필드가 있습니다.

- **예약됨**: FMS용으로 예약되어 있으며 0이어야 합니다.
- **Filter**: 패킷 필터링 여부를 나타냅니다.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: 패킷의 내용 유형을 정의합니다.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Data Size**: 메시지의 길이를 나타냅니다.
- **Timestamp Lower**: 태그 데이터가 적용되는 타임스탬프를 밀리초 단위로 저장합니다. 첫 번째 패킷에 대해 NULL로 설정됩니다.
- **Timestamp Upper**: uint32_be 값을 생성하기 위한 확장입니다.
- **Stream ID**: 첫 번째 스트림에 대해 NULL로 설정됩니다.
- **Payload Data**: 패킷 유형에 따른 데이터입니다.

## 참조 ##

- [플래시 비디오 - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

