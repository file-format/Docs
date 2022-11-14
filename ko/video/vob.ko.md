---
date: 2019-10-11
keywords: vob, .vob, vob 파일 형식, .vob 파일 형식, .vob 확장자, vob 확장자, vob 비디오 형식, vob dvd 파일
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "VOB 파일 형식과 VOB 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
title: VOB 파일 형식
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## .VOB 파일이란? ##

VOB 파일은 일반적으로 .vob 확장자를 가진 DVD의 VIDEO_TS 디렉토리에 저장됩니다. VOB 파일에는 비디오 및 오디오 데이터는 물론 메뉴 및 자막과 같은 기타 데이터가 포함됩니다. VOB는 MPEG-2 프로그램 스트림 형식을 기반으로 하지만 사설 스트림에는 추가 제한 사항과 사양이 있습니다. VOB 파일은 MPEG 프로그램 스트림의 엄격한 하위 집합이므로 모든 VOB 파일은 MPEG 프로그램 스트림이지만 모든 MPEG 프로그램 스트림은 VOB와 호환되지 않습니다.

## DVD 비디오의 구조 ##

DVD가 컴퓨터에서 열리면 VIDEO_TS는 AUDIO_TS가 있는 최상위 디렉토리입니다. AUDIO_TS는 비어 있으며 사용되지 않습니다. VIDEO_TS 디렉토리에는 VOB, BUP 및 IFO 파일이 있습니다. VOB 파일에는 MPEG 콘텐츠가 포함되어 있습니다. 모든 운영 체제와 호환되도록 1GB 이하의 청크로 나뉩니다. IFO 파일에는 메뉴 및 제목 구조에 대한 정보가 포함되어 있습니다. BUK 파일은 같은 이름의 IFO 파일의 백업 파일입니다. 이러한 파일은 DVD의 물리적 손상으로 인해 IFO 파일이 손상된 경우에도 BUK 파일에서 동일한 정보를 제공할 수 있도록 물리적으로 별도의 영역에 보관하기 위한 것입니다.

### 물리적 레이아웃 ###

- 디스크의 모든 파일은 연속적이어야 합니다.
- 관련 파일은 서로 나란히 있어야 합니다(VOB, IFO, BUP).
- 번호가 매겨진 파일은 오름차순이어야 합니다.

## 복사 방지 ##

많은 비디오 DVD는 암호화되어 DVD에서 데이터를 복사할 수 없습니다. DVD의 액세스할 수 없는 리드인 영역에 있는 파일을 재생하려면 인증 및 암호 해독 키가 필요합니다. 이 키는 DVD 플레이어 또는 소프트웨어 플레이어에 있는 CSS 암호 해독 소프트웨어에서 사용됩니다. 키가 없으면 파일을 열 때 키를 요청하므로 비디오 파일을 재생할 수 없습니다.

## 참조 ##

- [VOB - 위키백과](https://en.wikipedia.org/wiki/VOB)
- [DVD-Video 내부/디렉토리 구조](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

