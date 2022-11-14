---
date: 2019-12-13
keywords: ogg, ogg 파일 형식, .ogg 확장자, ogg 오디오 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "OGG 파일 형식과 OGG 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: OGG 파일 - Ogg Vorbis 오디오 파일
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## .OGG 파일이란?

OGG는 .ogg 확장자로 저장되는 Ogg Vorbis 압축 오디오 파일입니다. OGG 파일은 오디오 데이터를 저장하는 데 사용되며 아티스트 및 트랙 정보 및 메타데이터도 포함할 수 있습니다. OGG는 Xiph.Org Foundation에서 유지 관리하는 무료 개방형 컨테이너 형식입니다.

## OGG 파일 형식의 간략한 역사

Ogg 프로젝트는 1993년 더 큰 프로젝트의 일부로 시작되어 Squish라는 이름이 지정되었지만 기존 상표 때문에 OggSquish로 이름이 변경되었습니다. 현대 오디오 응용 프로그램을 위한 유연한 압축 오디오 형식을 만들려는 시도로 설명되었습니다. OGG 참조는 2000년 9월 2일에 Vorbis에서 분리되었습니다.

OGM은 OGG에서 공식 비디오 지원이 부족하여 2002년에 만들어졌습니다. 이를 통해 Microsoft DirectShow 프레임워크의 비디오를 OGG 기반 래퍼에 포함할 수 있습니다. 2006년까지 OGG는 많은 비디오 게임 엔진에서 지원되었으며 일반적으로 무료 콘텐츠를 인코딩하는 데 사용되었습니다. Free Software Foundation은 2007년 5월 15일에 MP3에 대한 우수한 대안으로 Vorbis의 사용을 늘리기 위한 캠페인을 시작했습니다. 2009년 6월 30일까지 OGG는 Firefox 3.5의 HTML5 구현에서 지원하는 유일한 컨테이너 형식이었습니다.

## OGG 파일 형식

OGG 형식은 데이터 청크로 구성됩니다. 각 청크를 Ogg 페이지라고 합니다. 각 페이지는 Ogg 형식을 식별하기 위해 "OggS"로 시작합니다. 헤더에는 각 페이지를 시리즈의 일부로 식별하는 일련 번호와 페이지 번호가 포함됩니다. 페이지는 다음 구성 요소로 구성됩니다.

- **페이지 헤더**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| 비트 | 가치 | 설명 |
| --- | --- | --- |
| 0 | 0x01 | 페이지의 첫 번째 패킷이 논리 비트스트림에서 이전 패킷의 연속임을 나타냅니다. |
| 1 | 0x02 | 이 페이지가 논리 비트스트림의 첫 번째 페이지임을 나타냅니다. |
| 2 | 0x04 | 이 페이지가 논리적 비트스트림의 마지막임을 나타냅니다. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **메타데이터**: VorbisComment는 메타데이터를 저장하기 위해 가장 널리 지원되는 메커니즘입니다. 다른 메커니즘에는 다음이 포함됩니다.
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## 참조 ##

- [OGG - 위키백과](https://en.wikipedia.org/wiki/Ogg)

