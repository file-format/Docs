---
date: 2021-03-21
keywords: alac, alac 파일 형식, .alac 확장자
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "ALAC 파일 형식 및 ALAC 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: ALAC - Apple 무손실 오디오 코덱 파일 형식
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## .ALAC 파일이란?

ALAC 파일 형식은 MPEG-4 호환 QuickTime 컨테이너를 사용하는 ALAC(Apple Lossless Audio Codec)입니다. 2004년에 독점 파일 형식으로 도입되었으며, 2011년 Apple이 이를 로열티 프리로 공개 소스로 제공할 때까지였습니다. 형식은 [FLAC](/ko/audio/flac/)(무료 무손실 오디오 코덱)과 유사하지만 상대적으로 더 많은 압축을 제공합니다. [AAC](/ko/audio/aac/) 또는 [MP3](/ko/audio/mp3/)에 대한 더 나은 사운드 대안을 제공합니다. ALAC 코덱으로 인코딩된 오디오 파일은 K-Lite 코덱이 포함된 Apple QuickTime, Apple iTunes 및 Micrsoft Windows Media Player를 사용하여 열 수 있습니다.

## ALAC 파일 형식

ALAC 코덱 기반 파일은 개발자 참고용으로 [GitHub 공개 소스](https://github.com/macosforge/alac)로 제공되는 바이너리 파일입니다. 여기에는 ALAC 인코더 및 디코더의 소스가 포함되어 있습니다. Apple은 또한 'alacconvert'라는 명령줄 유틸리티를 제공하여 CAF(Core Audio Format) 및 [WAVE](/ko/audio/wav/) 파일에서 오디오 데이터를 읽고 쓸 수 있습니다. 다음은 ALAC 파일 형식에 대한 몇 가지 요점입니다.

1. '비트 깊이' - 16, 20, 24 및 32비트.
1. '샘플 레이트' - 1에서 384,000Hz 사이의 임의의 정수 샘플 레이트입니다. 최대 4,294,967,295(2^32 - 1)Hz의 이론적인 속도가 지원될 수 있습니다.
1. '패킷 크기' - 기본 패킷 크기는 기본적으로 패킷당 4096 샘플 오디오 프레임입니다. 다른 패킷 크기도 확실히 가능합니다. 그러나 기본이 아닌 패킷 크기는 Apple Lossless를 지원하는 모든 하드웨어 장치에서 제대로 작동하지 않을 수 있습니다. 16,384 샘플 프레임을 초과하는 패킷은 지원되지 않습니다.
1. '지원 채널' - 1~8개의 채널을 지원합니다. 각 채널에는 다음과 같은 정보 순서가 있습니다.

|넘 찬| 주문|
|---|---|
|1 |모노|
|2 |스테레오(왼쪽, 오른쪽)|
|3 |MPEG 3.0 B(중앙, 왼쪽, 오른쪽)|
|4 |MPEG 4.0 B(중앙, 좌, 우, 중앙 서라운드)|
|5 |MPEG 5.0 D(중앙, 왼쪽, 오른쪽, 왼쪽 서라운드, 오른쪽 서라운드)|
|6 |MPEG 5.1 D(중앙, 왼쪽, 오른쪽, 왼쪽 서라운드, 오른쪽 서라운드, 저주파 효과)|
|7 |Apple AAC 6.1(중앙, 좌측, 우측, 좌측 서라운드, 우측 서라운드, 중앙 서라운드, 저주파 효과)|
|8 |MPEG 7.1 B(중앙, 좌측 중앙, 우측 중앙, 좌측, 우측, 좌측 서라운드, 우측 서라운드, 저주파 효과)|

## 참고문헌

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [애플 무손실 오디오 코덱](https://macosforge.github.io/alac/)
* [macosforge - GitHub의 alac](https://github.com/macosforge/alac)

