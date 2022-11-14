---
date: 2019-10-11
keywords: WEBM, WEBM 파일이란, WEBM 파일 형식
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "WEBM 파일을 만들고 열 수 있는 WEBM 파일 형식과 API에 대해 알아보세요."
title: WEBM - WebM 비디오 파일 형식
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## .WEBM 파일이란?

확장자가 .webm인 파일은 로열티 프리 개방형 WebM 파일 형식을 기반으로 하는 비디오 파일입니다. 웹에서 비디오를 공유하도록 설계되었으며 비디오 및 오디오 형식을 포함한 파일 컨테이너 구조를 정의합니다. WebM은 100% 무료이며 HTML, HTTP, TCP/IP 등 누구나 구현 가능한 개방형 기술을 기반으로 고품질을 구현합니다. WebM은 웹에서 비디오를 제공하도록 특별히 설계되어 낮은 계산 공간으로 스트리밍에 최적화됩니다. 따라서 모든 장치, 특히 저전력 넷북, 핸드헬드 및 태블릿에서 비디오를 재생하는 데 적합합니다.

## WEBM 파일 형식

WebM 파일 구조는 Matroska [MKV](/ko/video/mkv/) 컨테이너 파일 형식의 하위 집합을 기반으로 합니다. WebM 파일에서 사용 가능한 비디오 스트림은 압축 효율이 높은 VP8 또는 VP9 압축 기술을 사용하여 압축됩니다. 마찬가지로 WebM 파일의 오디오 스트림은 [Xiph Foundation](https://www.xiph.org/)에서 개발한 Vorbis 또는 Opus 코덱을 사용하여 압축됩니다. 이 모든 비디오 및 오디오 코덱은 로열티 프리이며 무료로 사용할 수 있습니다.

다음은 WebM 파일 형식에 대한 요약된 사양입니다.

|필드|설명|
---|---|
|MIME 형식 |동영상/webm|
|오디오 전용 MIME 유형 |audio/webm|
|유니폼 유형 식별자| org.webmproject.webm|
|비디오 코덱 이름| VP8 또는 VP9|
|오디오 코덱 이름| 보비스 또는 오푸스|

### WebM 요소

Matroska 사양의 하위 집합인 WebM은 일부 Matroska 기능에 대한 지원을 제공합니다. 다음은 지원되는 요소에 대한 설명입니다.

#### EBML

|이름 |설명|
---|---|
|EBML|따를 데이터의 EBML 특성을 설정합니다. 각 EBML 문서는 이것으로 시작해야 합니다.|
|EBMLVersion |파일 생성에 사용된 EBML 파서의 버전.|
|EBMLReadVersion|파서가 이 파일을 읽기 위해 지원해야 하는 최소 EBML 버전.|
|EBMLMaxIDLength |이 파일에서 찾을 ID의 최대 길이입니다(Matroska에서는 4 이하).|
|EBMLMaxSizeLength|이 파일에서 찾을 수 있는 크기의 최대 길이입니다(Matroska에서는 8 이하). 이것은 요소의 시작 부분에 표시된 요소 크기를 무시하지 않습니다. 표시된 크기가 EBMLMaxSizeLength에서 허용하는 것보다 큰 요소는 유효하지 않은 것으로 간주됩니다.|
|DocType|이 EBML 헤더(이 경우 "webm") 다음에 오는 문서 유형을 설명하는 문자열.|
|DocTypeVersion|파일을 만드는 데 사용된 DocType 인터프리터의 버전입니다.|
|DocTypeReadVersion|이 파일을 읽기 위해 인터프리터가 지원해야 하는 최소 DocType 버전입니다.|

#### 전역 요소

현재 손상된 데이터를 사용할 때 예기치 않은 동작을 방지하기 위해 손상된 데이터를 무효화하는 데 사용되는 'Void' 요소만 지원됩니다. 콘텐츠가 삭제됩니다. 또한 나중에 사용하기 위해 하위 요소의 공간을 예약하는 데 사용됩니다.

#### 세그먼트
이 요소는 다른 모든 최상위(레벨 1) 요소를 포함합니다. 일반적으로 Matroska 파일은 1개의 세그먼트로 구성됩니다.

#### 메타 탐색 정보

다음 검색 정보가 지원됩니다.

|요소 이름 |설명|
---|---|
|SeekHead |다른 레벨 1 요소의 위치를 포함합니다.|
|Seek |EBML 요소에 대한 단일 탐색 항목을 포함합니다.|
|SeekID |요소 이름에 해당하는 바이너리 ID.|
|SeekPosition |옥텟 단위의 세그먼트에서 요소의 위치(0 = 첫 번째 레벨 1 요소).|

## 참고문헌

* [웹엠](https://www.webmproject.org/)
* [WebM 코드 저장소](https://www.webmproject.org/code/#webp-repositories)

