---
date: 2020-08-12
keywords: jxr, .jxr, jxr 파일 형식, jxr 파일을 여는 방법, .jxr 확장자, jxr 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR 파일 형식
linktitle: JXR
description: "JXR 파일을 만들고 열 수 있는 JXR 파일 형식과 API에 대해 알아봅니다."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## .JXR 파일이란? ##

JPEG XR(JPEG 확장 범위)은 연속 톤 사진 이미지용 파일 형식입니다. Microsoft에서 개발한 HD Photo를 기반으로 하는 정지 이미지 압축 표준입니다. 손실 및 무손실 압축을 모두 지원합니다.

## 간략한 역사 ##

Windows Media Photo는 Microsoft가 WinHEC 2006에서 처음 발표했습니다. 2006년 11월에 HD Photo로 이름이 변경되었습니다. JPEG XR은 2009년 6월 19일에 국제 표준 ISO/IEC 29199-2로 승인되었습니다. ITU-T 및 ISO/IEC는 동의안을 게시했습니다. 형식 사양(ITU-T T.833 | ISO/IEC 29199-3), 적합성 테스트 세트(ITU-T T.834 | ISO/IEC 29199-4) 및 참조 소프트웨어(ITU-T T.835 | ISO /IEC 29199-5) 2010년 이미지 코딩 사양 완료 후 JPEG XR용. JPEG XR의 워크플로 아키텍처를 설명하는 기술 보고서는 2011년에 출판되었습니다.

## JPEG XR 디자인 ##

JPEG와 비교할 때 JPEG XR은 다음과 같은 몇 가지 개선 사항을 제공합니다.

- **더 나은 압축**: JPEG XR은 더 높은 압축률을 제공합니다.
- **무손실 압축**: JPEG XR은 무손실 압축을 지원합니다.
- **타일 구조**: JPEG XR 이미지는 각 영역을 별도로 디코딩할 수 있는 타일 영역으로 분할할 수 있습니다.
- **색상 정확도 향상**: JPEG XR에는 RGB 색상 공간을 사용하여 이미지를 지원하기 위해 YCoCg 색상 공간으로의 내부 변환이 포함됩니다. JPEG XR은 구성 요소당 16비트(픽셀당 64비트) 정수 CMYK 색상 모델도 지원합니다. JPEG XR은 HDR 이미지에 대해 RGBE 공유 지수 부동 소수점 색상 형식을 지원합니다. JPEG XR은 회색조 및 다중 채널 색상 인코딩도 지원합니다.
- **투명도 맵**: JPEG XR은 투명도를 위해 알파 채널을 지원합니다.
- **압축 영역 이미지 수정**: JPEG XR 이미지는 손실 인코딩, 해상도 감소, 자르기, 뒤집기, 회전으로 변환될 수 있으며 타일 구조는 파일의 전체 디코딩 없이 모두 변경될 수 있습니다.
- **메타데이터 지원**: JPEG XR 이미지 파일에는 여러 장치에서 일관된 색상 표현을 위한 ICC 색상 프로필이 포함될 수 있습니다. 형식은 Exif 및 XMP 메타데이터 형식도 지원합니다.

## 컨테이너 형식 ##

JPEG XR 이미지 데이터는 IFT(이미지 파일 디렉토리) 태그 테이블을 사용하여 TIFF와 같은 컨테이너 형식으로 저장할 수 있습니다. JXR 파일은 IFD 태그에 다음을 포함합니다.

- 이미지 데이터: 연속된 자체 포함된 이미지 데이터입니다.
- 선택적 알파 채널 데이터: 이것이 있는 경우 이미지 데이터를 별도로 압축하여 투명도를 지원하지 않는 응용 프로그램을 지원할 수 있습니다.
- 메타데이터
- 선택적 XMP 메타데이터
- 선택적 Exif 메타데이터

TIFF 형식을 기반으로 하므로 4GB 파일 크기 제한과 같은 모든 TIFF 형식 제한을 상속합니다.

## 참조 ##

- [JPEG XR - 위키백과](https://en.wikipedia.org/wiki/JPEG_XR)

