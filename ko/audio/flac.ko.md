---
date: 2019-12-13
keywords: flac, flac 파일 형식, .flac 확장자, flac 파일, flac 대 mp3
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLAC 파일 형식 및 FLAC 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: FLAC 파일 형식
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## .FLAC 파일이란?

FLAC(Free Lossless Audio Codec)은 Xiph.Org Foundation에서 개발한 무손실 압축 오디오 코딩 형식입니다. FLAC은 .flac 확장자로 저장되는 로열티 프리 개방형 형식입니다. FLAC 알고리즘을 사용하여 압축된 디지털 오디오는 일반적으로 크기가 50~70%로 줄어듭니다. FLAC 파일은 원본 오디오 파일의 동일한 복사본으로 압축을 풀 수 있습니다.

## FLAC 파일 형식

이것은 FLAC 비트스트림의 개요입니다.

- **fLaC marker**: 이 마커는 스트림의 시작 부분에 추가됩니다. 그 뒤에 하나 이상의 메타데이터 블록이 옵니다.
- **메타데이터 블록**: FLAC에서 지원하는 메타데이터 블록의 종류는 128가지입니다. 현재 다음이 정의되어 있습니다.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: 오디오 데이터는 하나 이상의 오디오 프레임으로 구성됩니다.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## FLAC 파일 형식의 간략한 역사

Josh Coalson은 2000년에 FLAC의 개발을 시작했습니다. FLAC의 첫 번째 버전은 2001년 7월 20일에 릴리스되었습니다. FLAC는 2003년 1월 20일에 Xiph.Org 플래그로 통합되었습니다. FLAC의 개발은 다음과 함께 Xiph.Org git 저장소로 이동되었습니다. 2013년 3월 26일 버전 1.3.0 릴리스.

## FLAC 프로젝트 구성

FLAC 프로젝트는 다음으로 구성됩니다.

- 스트림 형식.
- 스트림(FLAC)에 대한 간단한 컨테이너 형식입니다.
- libFLAC: 참조 인코더, 디코더 및 메타데이터 인터페이스의 라이브러리입니다.
- libFLAC++: libFLAC용 객체 지향 래퍼.
- flac: FLAC 스트림을 인코딩 및 디코딩하는 명령줄 프로그램입니다.
- metaflac: FLAC용 명령줄 메타데이터 편집기.
- Winamp, XMMX 등과 같은 음악 플레이어용 입력 플러그인
- Ogg 컨테이너 형식(Ogg FLAC).

## FLAC 디자인

음악의 밀도와 진폭에 따라 압축 파일의 크기는 원본 파일보다 80% 작을 수 있습니다.

### 소스 인코더 ###

- 정수 샘플만 지원하며 부동 소수점은 지원하지 않습니다. 샘플당 4~32비트의 PCM 비트 분해능과 1Hz~65,535Hz의 샘플링 속도를 처리할 수 있습니다. FLAC 인코딩은 샘플당 24비트로 제한됩니다.
- 채널을 그룹화하여 채널 간 상관 관계를 활용하여 압축을 높일 수 있습니다.
- CRC 체크섬은 손상된 프레임을 식별하는 데 사용됩니다.
- 오디오 샘플의 변환을 위해 FLAC은 선형 예측을 사용합니다.

### 메타데이터 ###

- FLAC은 ReplayGain을 지원합니다(오디오의 음량을 인지하고 표준화하는 데 사용).
- FLAC은 태그 지정을 위해 Vorbis 주석에 사용된 것과 동일한 시스템을 사용합니다.
- libFLAC은 인코딩/디코딩을 위해 대부분의 FLAC 응용 프로그램에서 사용됩니다.
- libFLAC API는 기본 FLAC 비트스트림에서 추상화를 높이기 위해 스트림, 탐색 가능한 스트림 및 파일로 구성됩니다.

### 압축 ###

libFLAC은 0에서 8까지의 압축 수준을 사용하며, 여기서 0은 가장 빠르고 8은 가장 느린 압축 수준입니다. 압축된 파일은 속도와 크기 사이에 균형이 있지만 항상 손실이 없습니다.

## FLAC 대 MP3
MP3는 손실 압축 형식이므로 압축을 적용한 후 크기를 줄이기 위해 오디오의 일부를 잘라낼 수 있습니다. 반면 FLAC은 무손실 파일 형식으로 오디오를 가장 순수한 형태로 들을 수 있습니다. 이전에 무손실 파일 형식은 FLAC만큼 공간 효율적이지 않은 CDA 또는 WAV였습니다. 다음 표는 몇 가지 중요한 용어에 대해 이 두 형식 간의 비교를 보여줍니다.

|용어|FLAC|MP3|
---|---|---|
|**데이터 품질**|오디오 데이터 손실 없음| 오디오 데이터를 압축할 때 일부 데이터가 손실될 수 있음|
|**크기**|손실 형식에 비해 파일 크기가 큽니다. 따라서 더 큰 저장 용량이 필요합니다| 저장 공간이 적은 소형 오디오 장치에서 재생하기에 적합한 더 작은 파일 크기 |
|**하드웨어 요구 사항**| 고품질 오디오 장비와 엄청난 저장 용량이 필요합니다. |거대한 오디오 라이브러리는 더 작은 저장 공간에 저장할 수 있습니다. 오디오 플레이어 또는 휴대폰과 같은 핸드헬드 장치에 적합|
|**인터넷을 통한 배포**|파일 크기가 커서 인터넷을 통해 쉽게 배포할 수 없음 |파일 크기가 작아 인터넷을 통해 쉽게 배포할 수 있음|
|**호환성**|지구상의 모든 장치와 거의 호환되는 가장 인기 있는 음악 및 오디오 청취 코덱신세대 PC, 전화, AV 수신기, 블루레이 플레이어, Roku 또는 Fire TV와 같은 스트리밍 장치와 호환|

## 참조 ##

- [FLAC - 위키백과](https://en.wikipedia.org/wiki/FLAC)

