---
date: 2022-01-06
keywords: vtt, .vtt, vtt 파일 형식, .vtt 파일 형식, .vtt 확장자, vtt 확장자
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: ".vtt 파일과 VTT 파일을 만들고 열 수 있는 API에 대해 알아보세요."
title: VTT 파일 형식 - 웹 비디오 텍스트 트랙 파일
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## .VTT 파일이란?

VTT 파일은 WebVTT(Web Video Text Tracks) 형식을 사용하여 시간이 지정된 텍스트 트랙(예: 자막 또는 캡션)을 표시하기 위한 정보가 포함된 텍스트 파일입니다. 시간 제한 텍스트 트랙에는 자막 또는 캡션과 같은 정보가 포함됩니다. VTT 파일의 목적은 텍스트 오버레이를<video> . 형식은 SRT 파일과 다소 유사합니다. WebVTT 기반 텍스트 파일은 UTF-8을 사용하여 인코딩됩니다. VTT 파일에는 자막, 설명, 캡션, 설명, 장 및 메타데이터와 같은 정보가 포함되어 있습니다. VTT 파일은 일반 텍스트 파일이므로 Microsoft 메모장, Apple TextEdit 및 메모장++과 같은 텍스트 편집기를 사용하여 열 수 있습니다.

## VTT 파일 형식 - 추가 정보

VTT 파일은 WebVTT 파일 형식을 사용하여 순차 텍스트 트랙 정보를 저장합니다. 시간이 지정된 각 텍스트 트랙은 다음 예와 같이 '큐'라고도 하는 한 줄 또는 여러 줄로 구성됩니다.

### VTT 파일 예

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT 파일 구조

다음은 VTT 파일의 구조 요구 사항입니다.

* 선택적 BOM(바이트 순서 표시)입니다.
* 문자열 "WEBVTT".
* WEBVTT 오른쪽의 선택적 텍스트 헤더.
* 연속된 두 줄 바꿈에 해당하는 빈 줄.
* 0개 이상의 단서 또는 설명.
* 0개 이상의 빈 줄.

## 참고문헌

* [VTT - W3 학교](https://www.w3.org/TR/webvtt1/)
* [WebVTT - 모질라](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

