---
date: 2019-12-13
keywords: m3u, m3u 파일 형식, .m3u 확장자, m3u 멀티미디어 재생 목록, m3u 재생 목록 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "M3U 파일 형식과 M3U 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: M3U 파일 형식
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## .M3U 파일이란? ##

M3U(MP3 URL)는 .m3u 확장자로 저장된 오디오 재생 목록 파일입니다. M3U는 실제 오디오 파일이 아니며 오디오 및 때로는 비디오 파일을 가리킵니다. M3U는 Fraunhofer에서 Winplay3 소프트웨어와 함께 사용하도록 개발되었습니다. 또한 다양한 미디어 플레이어 및 소프트웨어에서 지원됩니다.

## M3U 파일 형식

M3U 파일 형식에 대한 공식 사양은 없으며 사실상의 표준입니다. M3U는 텍스트가 로컬 시스템의 기본 비유니코드 인코딩으로 인코딩된 경우 .m3u 확장자를 사용하고 텍스트가 UTF-8로 인코딩된 경우 .m3u8 확장자를 사용하는 일반 텍스트 파일입니다. M3U 파일의 각 항목은 다음 중 하나일 수 있습니다.

- 파일의 절대 경로
- M3U 파일과 관련된 파일 경로입니다.
- URL

### 확장 M3U ###

확장된 M3U에서는 "#"으로 시작하고 매개변수가 있는 경우 콜론(:)으로 끝나는 추가 지시문이 도입되었습니다. 다음은 확장 M3U에 대한 지시문 목록입니다.

- **#EXTM3U** - Extended M3U를 나타내는 파일 헤더이며 파일의 첫 번째 줄에 있어야 합니다.
- **#EXTENC:** - 텍스트 인코딩. 파일의 두 번째 줄이어야 합니다.
- **#EXTINF:** - 트랙 정보 및 기타 추가 속성에 사용됩니다.
- **#PLAYLIST:** - 재생 목록의 제목
- **#EXTGRP:** - 이름 그룹화 시작
- **#EXTALB:** - 앨범 정보
- **#EXTART:** - 앨범 아티스트
- **#EXTGENRE** - 앨범 장르
- **#EXTM3A** - 앨범 트랙 또는 챕터에 대한 단일 파일 재생 목록.
- **#EXTBYT:** - 파일 크기(바이트).
- **#EXTBIN:** - 바이너리 데이터가 뒤따릅니다.
- **#EXTIMG:** - 로고, 표지 또는 기타 이미지.

### HLS M3U ###

HLS(HTTP 라이브 스트리밍)는 Apple에서 iOS 장치로 오디오 및 라디오를 스트리밍하기 위해 만들었습니다. UTF-8로 인코딩된 확장 M3U를 기반으로 합니다. 2017년 IETF에서 RFC 8216으로 표준화했습니다. HLS 재생 목록의 태그는 "#EXT-X-"로 시작합니다. 아래는 HLS에 대한 태그 목록입니다.

- **EXT-X-VERSION** - 미디어 및 해당 서버를 기반으로 하는 파일의 호환성 버전을 나타냅니다.
- **#EXT-X-START:** - 재생 목록의 기본 시작 지점을 나타냅니다.
- **#EXT-X-PLAYLIST-TYPE:** - 재생목록의 종류(EVENT 또는 VOD)를 제공합니다.
- **#EXT-X-TARGETDURATION:** - 최대 Segment duration을 지정합니다.
- **#EXT-X-MEDIA-SEQUENCE:** - Media Sequence Number를 나타냅니다.
- **#EXT-X-INDEPENDENT-SEGMENTS** - 모든 미디어 샘플이 독립적이며 다른 세그먼트 없이 디코딩될 수 있음을 나타냅니다.
- **#EXT-X-MEDIA:** - 동일한 콘텐츠의 대체 변환을 포함하는 미디어 재생 목록을 연결하는 데 사용됩니다.
- **#EXT-X-STREAM-INF:** - Renditions의 일부인 Variant Stream을 지정합니다.
- **#EXT-X-BYTERANGE:** - 미디어 세그먼트가 URI로 식별되는 리소스의 하위 범위임을 나타냅니다.
- **#EXT-X-DISCONTINUITY** - 앞뒤 미디어 세그먼트 사이의 불연속성을 나타냅니다.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - 동일한 Variant Stream 또는 다른 Variant Streams의 다른 변환 간의 동기화를 허용합니다.
- **#EXT-X-KEY:** - 미디어 세그먼트를 해독하는 방법을 지정합니다.
- **#EXT-X-MAP:** - 미디어 초기화 섹션을 얻는 방법을 지정합니다. 해당 미디어 세그먼트를 구문 분석하는 데 필요합니다.
- **#EXT-X-PROGRAM-DATE-TIME:** - Media Segment의 첫 번째 샘플을 절대 날짜 및/또는 시간과 연결합니다.
- **#EXT-X-DATERANGE:** - 데이터 범위를 연결합니다.
- **#EXT-XI-FRAMES-ONLY** - 재생 목록의 각 미디어 세그먼트가 단일 I-프레임을 설명함을 나타냅니다.
- **EXT-XI-FRAME-STREAM-INF** - 재생 목록 파일에 멀티미디어 프레젠테이션의 I-프레임이 포함되어 있음을 나타냅니다.
- **#EXT-X-SESSION-DATA:** - 임의의 세션 데이터를
마스터 재생 목록에 포함됩니다.
- **#EXT-X-SESSION-KEY:** - 암호화 키를 허용합니다. 클라이언트는 먼저 재생 목록을 읽지 않고 이러한 키를 미리 로드할 수 있습니다.
- **#EXT-X-ENDLIST** - 더 이상 미디어 세그먼트가 파일에 추가되지 않음을 나타냅니다.

다음은 M3U에서 사용하는 인터넷 미디어 유형 목록입니다.

- **application/vnd.apple.mpegurl**: HLS 애플리케이션에서 재생 목록을 참조하는 데 사용되는 M3U에 대해 유일하게 등록된 미디어 유형(2009년 등록)입니다.
- HLS가 아닌 응용 프로그램에서 사용하는 인터넷 미디어 유형은 다음과 같습니다.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U 예제 ##

이것은 M3U 파일의 예입니다.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## 참조 ##

- [M3U - 위키피디아](https://en.wikipedia.org/wiki/M3U)
- [HTTP 라이브 스트리밍](https://tools.ietf.org/html/rfc8216)

