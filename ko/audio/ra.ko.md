---
date: 2019-12-13
keywords: ra, ra 파일 형식, .ra 확장자, 실제 오디오 파일 형식, ra 오디오 형식, RealAudio 파일 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "RA 파일 형식 및 RA 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: RA 파일 형식
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## .RA 파일이란?

RealAudio(RA)는 Real Networks, Inc.에서 개발하고 1995년 4월에 출시한 독점 오디오 형식입니다. 파일에 .ra 확장자를 사용합니다. 낮은 비트 전송률과 높은 충실도의 오디오 코덱을 사용합니다. RA는 많은 인터넷 라디오 방송국에서 인터넷을 통한 오디오 스트리밍에 사용되었습니다. BBC 웹사이트는 2009년까지 RA를 많이 사용했지만 2011년 3월에 중단되었습니다.

## RealNetworks의 파일 확장자 ##

RealNetworks는 오디오에 RA 파일 형식을 사용했습니다. RealNetworks는 1997년 .rv 확장자를 사용하여 비디오 형식([RealVideo](/ko/video/rv/))을 제공하기 시작했습니다. [RealMedia(RM)](/ko/video/rm/)는 오디오 및 비디오 형식의 조합에 사용되었습니다. RealProduce(Real의 인코더) 최신 릴리스에서는 동영상 파일에 RV 형식을 사용하고 VBR(가변 비트 전송률) 동영상 파일에 [RealMedia Variable Bitrate(RMVB)](/ko/video/rmvb/) 형식을 사용합니다.

## 스트리밍 오디오 ##

RA는 스트리밍 미디어 형식으로 개발되었으며 HTTP를 사용하여 스트리밍할 수 있습니다. 오디오 파일은 파일의 첫 번째 부분이 수신되는 즉시 재생을 시작하고 파일의 나머지 부분이 다운로드되는 동안 계속 재생됩니다.

RealAudio의 첫 번째 버전은 독점 PNA 또는 PNM 프로토콜을 사용하여 오디오를 스트리밍했습니다. 나중에 그들은 연결을 관리하기 위해 IETF 표준화된 RTSP(실시간 스트리밍 프로토콜)로 전환했습니다. 데이터를 보내기 위해 RDT(Real Data Transfer) 프로토콜을 사용했습니다. 프로토콜은 처음에는 비밀로 유지되었지만 나중에 Helix 프로젝트를 통해 일부가 공개되었습니다.

RealAudio 파일을 스트리밍하기 위해 대부분의 페이지는 RAM(Real Audio Metadata) 또는 SMIL(Synchronized Multimedia Integration Language) 파일에 연결됩니다. 이 파일은 사용자의 미디어 플레이어를 로드하고 파일에 포함된 URL에서 오디오를 스트리밍하는 데 사용됩니다.

## RealAudio 오디오 코덱 ##

다음은 4자리 코드로 식별되는 오디오 코덱 목록과 이를 도입한 RealAudio 버전입니다.

|코덱|리얼오디오 버전|
|---|---|
|lpcJ 및 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|요리사|6|
|atrc|8|
|라크|9|
|랙|10|
|랄프|10|

## 참조 ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

