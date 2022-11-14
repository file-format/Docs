---
date: 2019-10-11
keywords: f4v, .f4v, f4v 파일 형식, .f4v 파일 형식, .f4v 확장자, f4v 확장자, f4v 비디오 형식, f4v 파일을 여는 방법, f4v 파일이란
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "F4V 파일을 만들고 열 수 있는 F4V 파일 형식 및 API에 대해 알아보십시오."
title: F4V 파일 형식
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## .F4V 파일이란? ##

F4V(Flash MP4 비디오 파일)는 .f4v 확장자로 저장된 비디오 파일입니다. ISO 기본 미디어 파일 형식(MPEG-4 Part 12)을 기반으로 합니다. [MP4](/ko/video/mp4/)와 매우 유사하여 비공식적으로 Flash MP4라고도 합니다. [FLV](/ko/video/flv/)에는 H.264/ACC 콘텐츠를 스트리밍할 때 제한이 있어 Adobe Systems에서 새로운 F4V 형식을 만들었습니다. Flash Player는 Flash Player 9 업데이트 3 릴리스 이후 F4V 파일을 재생할 수 있습니다.

## F4V 파일의 구조 ##

F4V 파일 형식은 ISO 기본 미디어 파일 형식(MPEG-4 Part 12)을 기반으로 하며 MP4 형식과 매우 유사합니다. 구조에 대한 자세한 내용은 [MP4](/ko/video/mp4/) 페이지를 참조하십시오. F4V와 MP4의 주요 차이점은 F4V가 저장할 수 있는 메타데이터 형식입니다. 다음은 F4V 형식에서 지원하는 메타데이터 형식 목록입니다.

- **태그 상자**: 영화(moov) 상자에 추가로 4개의 선택적 태그 상자(auth, title, dscp, cprt)가 있습니다.
- **XMP 메타데이터 상자**: 이 상자는 Movie(moov) 상자 바로 뒤에 옵니다. 이를 통해 파일은 ActionScript를 통해 XMP 메타데이터를 SWF 동영상에 전달할 수 있습니다.
- **ilst box**: 이 상자는 메타(메타) 상자 내부에 있으며 여러 메타데이터 태그를 포함할 수 있습니다. 지원되는 데이터 유형은 다음과 같습니다.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **텍스트 트랙 메타데이터 상자**: 미디어 데이터 상자(mdat) 내부의 텍스트 샘플(텍스트 또는 tx3g)입니다. 여기에는 다음 메타데이터 상자가 포함될 수 있습니다.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## 참조 ##

- [플래시 비디오 - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

