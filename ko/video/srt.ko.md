---
date: 2019-10-11
keywords: srt, .srt, srt 파일 형식, .srt 파일 형식, .srt 확장자, srt 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "SRT 파일 형식 및 SRT 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: SRT 파일 형식
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## .SRT 파일이란? ##

SRT(SubRip 파일 형식)는 .srt 확장자를 가진 SubRip 파일 형식으로 저장된 간단한 자막 파일입니다. 여기에는 일련의 자막, 시작 및 종료 타임스탬프, 자막 텍스트가 포함됩니다. SRT 파일을 사용하면 제작된 비디오 콘텐츠에 자막을 추가할 수 있습니다.

## SRT 파일 구조 ##

각 자막에는 SRT 파일의 네 부분이 있습니다.

1. 자막의 번호 또는 위치를 나타내는 숫자 카운터.
1. --> 문자로 구분된 자막 시작 및 종료 시간
1. 한 줄 이상의 자막 텍스트.
1. 자막의 끝을 나타내는 빈 줄.

### SRT의 예 ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

시간을 지정하려면 *시:분:초,밀리초(00:00:00,000)* 형식이 사용됩니다.

## SRT 파일 포맷 ##

SRT 파일의 형식은 HTML 태그에서 파생됩니다. SRT 파일의 형식 지정 태그는 다음과 같습니다.

| 효과 | 태그 |
| --- | --- |
|굵게|**\ <b>...\</b> ** 또는 {b}...{/b}|
|기울임꼴|**\ <i>...\</i> ** 또는 **{i}...{/i}**|
|밑줄|**\ <u>...\</u> ** 또는 **{u}...{/u}**|
|글꼴 색상|**\ <font color="white">...\</font> **|
|줄 위치|**{\a3}** (텍스트가 3행에 나타나기 시작해야 함을 나타냄)

## SubRip 소프트웨어 ##

SubRip은 Windows에서 실행되는 무료 소프트웨어 프로그램입니다. 다양한 비디오 형식에서 자막과 해당 타이밍을 추출하고 자막을 SRT 형식으로 저장합니다. SubRip은 광학 문자 인식을 사용하여 라이브 비디오, 기타 비디오 파일 및 DVD에서 자막을 추출합니다.

## 참조 ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
