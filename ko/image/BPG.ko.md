---
date: 2020-08-12
keywords: bpg, .bpg, bpg 파일 형식, bpg 파일을 여는 방법, .bpg 확장자, bpg 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG 파일 형식
linktitle: BPG
description: "BPG 파일 형식과 BPG 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## .BPG 파일이란? ##

BPG(Better Portable Graphics)는 2014년 Fabrice Bellard에서 디지털 이미지용으로 만든 파일 형식입니다. 그는 BPG가 압축 또는 크기 효율성이 더 높기 때문에 JPEG의 대체품으로 BPG를 제안했습니다. BPG는 HEVC(고효율 비디오 코딩) 비디오 압축 표준의 프레임 내 인코딩을 사용합니다.

BPG는 휴대형 및 IoT 장치에서 작동하도록 메모리 효율적인 휴대용 형식으로 설계되었습니다. 현재 웹 브라우저는 BPG 형식을 지원하지 않지만 웹 사이트는 여전히 Bellard에서 작성한 JavaScript 라이브러리를 사용하여 BPG 이미지를 전달할 수 있습니다. BPG는 샘플당 최대 14비트까지 HEVC의 메인 4:4:4 16 스틸 픽처 프로파일을 사용합니다.

## 사양 ##

BPG 컨테이너 형식은 HEVC에서 사용되는 원시 비트스트림이 아닌 일반 이미지 형식입니다. BPG는 4:4:4, 4:2:2 및 4:2:0 색상 형식을 지원합니다. 알파 채널은 별도로 코딩된 추가 채널 또는 CMYK 이미지의 네 번째 채널에서도 지원됩니다. BPG는 Exif, ICC 프로필 및 XMP에 대한 메타데이터 지원을 제공합니다. BPG는 YCbCr(ITU-R BT.601, BT.709 및 BT.2020(비일정 휘도)), YCgCo, RGB, CMYK 및 회색조 색 공간을 지원합니다. BGP는 또한 애니메이션과 손실 및 무손실 HEVC 데이터 압축을 지원합니다.

## 참조 ##

- [더 나은 휴대용 그래픽 - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

