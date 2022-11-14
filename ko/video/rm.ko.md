---
date: 2019-10-11
keywords: rm, .rm, rm 파일 형식, .rm 파일 형식, .rm 확장자, RealMedia 파일 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RM 파일 형식과 RM 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: RM 파일 형식
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## .RM 파일이란? ##

RealMedia는 .rm 확장자를 사용하는 RealNetworks에서 개발한 독점 멀티미디어 컨테이너 형식입니다. 인터넷을 통한 스트리밍을 위해 [RealAudio(RA)](/ko/audio/ra/) 및 [RealVideo(RV)](/ko/video/rv/)의 조합과 함께 사용됩니다. 이러한 스트림은 비트 전송률이 일정합니다. 가변 비트레이트의 경우 RealNetworks는 RMVB(RealMedia Variable Bitrate) 형식을 개발했습니다. RealMedia는 인터넷을 통해 콘텐츠를 스트리밍하는 데 적합하며 예를 들어 라이브 TV 스트리밍에 사용할 수 있습니다.

## RealMedia 파일의 구조 ##

RealMedia 파일은 각각 다음 구조를 갖는 일련의 청크로 구성됩니다.

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

다음은 RealMedia 파일에 있는 청크 유형입니다.

- **RealMedia 파일 헤더(.RMF)**: RealMedia 파일의 첫 번째 청크여야 합니다. 하나의 파일에는 하나의 RMF 청크만 있습니다. 헤더 수에 대한 정보를 포함합니다.
- **파일 속성 헤더(PROP)**: RealMedia 파일의 일반 속성에 대한 정보를 포함합니다. 각 RealMedia 파일에는 이 유형의 청크가 하나만 있습니다.
- **미디어 속성 헤더(MDPR)**: 이 청크는 스트림 속성에 대한 정보를 포함합니다. 여기에는 스트림 유형 및 사용된 코덱에 대한 정보가 포함됩니다. 파일의 각 스트림에 대해 하나의 MDPR 청크가 있습니다.
- **콘텐츠 설명 헤더(CONT)**: 이 청크에는 RealMedia 파일의 콘텐츠 제목이나 작성자와 같은 텍스트 정보가 포함됩니다. 이 청크는 정보 제공용입니다.
- **데이터 헤더(DATA)**: 이 청크는 데이터 패킷 그룹을 포함합니다.
- **인덱스 헤더(INDX)**: 이 청크는 모든 DATA 청크 다음에 오고 색인 항목을 포함합니다. 하나의 파일에는 둘 이상의 INDX 청크가 있을 수 있습니다.

## 지원되는 오디오 및 비디오 형식 ##

### 오디오 형식 ###

- lpcJ: RealAudio 1.0(VSELP)
- 28_8: RealAudio 2.0(LD-CELP
- dnet: AC3
- sipr: 시프로
- 쿡: 쿡
- atrc: ATRAC3
- ralf: RealAudio 무손실 형식
- raac: LC-AAC
- 랩: HE-AAC

### 동영상 형식 ###

- CLV1: 클리어 비디오
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264 전구체
- RV40: H.264 전구체, RV40
- RVTR: H.263+(RV20)

## 참조 ##

- [리얼미디어 - 위키피디아](https://en.wikipedia.org/wiki/RealMedia)

