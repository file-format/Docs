---
date: 2020-08-12
keywords: jfif, .jfif, jfif 파일 형식, jfif 파일을 여는 방법, .jfif 확장자, jfif 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF 파일 - .jfif 파일이란 무엇입니까?
linktitle: JFIF
description: "JFIF 파일 형식과 JFIF 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## .JFIF 파일이란?

JFIF(JFIF(JPEG File Interchange Format))는 .jfif 확장자를 사용하는 이미지 형식 파일입니다. JFIF는 복잡성을 줄이고 한계를 해결하여 JIF(JPEG 교환 형식)를 기반으로 구축됩니다.

## JFIF의 간략한 역사

JFIF 문서 개발은 Eric Hamilton이 주도했으며 1991년 말에 첫 번째 버전에 대한 합의가 이루어졌습니다. 버전 1.02는 1992년 9월 7일에 게시되었습니다. RFC 2046은 JFIF 형식이 인터넷을 통해 JPEG 이미지를 전송하는 데 사용된다고 지정했습니다. JFIF는 2009년 ECMA에서 발행되었으며 2011년 ITU-T에서 Recommendation T.871로, 2013년 ISO/IEC에서 ISO/IEC 10918-5로 표준화되었습니다.

## JFIF 파일 형식 ##

JFIF 파일은 JPEG 표준의 파트 1에 정의된 일련의 마커로 구성됩니다. 각 마커는 2바이트(FF 다음에 마커 유형을 지정하는 바이트)로 구성됩니다. 마커는 독립 실행형이거나 마커 세그먼트의 시작을 나타낼 수 있습니다.

JFIF를 사용하면 Y, Cb, Cr과 같은 여러 구성 요소가 서로 다른 해상도를 가질 수 있지만 정렬은 정의되지 않습니다. JPEG와 달리 JFIF는 해상도 및 종횡비 정보를 제공할 수 있습니다. JFIF는 또한 사용할 색상 모델을 정의합니다.

### 파일 구조 ##

|세그먼트|코드|설명|
|---|---|---|
|SOI|FF D8|이미지 시작|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|추가 마커 세그먼트|
|SOS|FF DA|스캔 시작|
||압축된 이미지 데이터||
|EOI|FF D9|이미지 끝|

JFIF 표준은 다음 세그먼트를 정의합니다.

### JFIF APP0 마커 세그먼트 ###

이미지 매개변수를 포함하는 필수 세그먼트입니다. 또한 압축되지 않은 포함된 축소판을 포함할 수 있습니다.

|필드|크기(바이트)|설명|
|---|---|---|
|APP0 마커|2|FF E0|
|길이|2|APP0 마커를 제외한 세그먼트의 길이|
|식별자|5|널 바이트로 종료되는 ASCII의 JFIF(4A 46 49 46 00)|
|JFIF 버전|2|JFIF 버전|
|밀도 단위|1|다음 픽셀 밀도 필드의 단위</br> 00 : 단위 없음; 너비:높이 픽셀 종횡비는 Ydensity:Xdensity와 같습니다.</br> 01 : 인치당 픽셀 수</br> 02 : 센티미터당 픽셀 수|
|Xdensity|2|0보다 큰 수평 픽셀 밀도|
|Ydensity|2|0보다 큰 수직 픽셀 밀도|
|Xthumbnail|1|포함된 RGB 축소판의 가로 픽셀 수입니다. 0일 수 있음|
|Ythumbnail|1|포함된 RGB 축소판의 세로 픽셀 수입니다. 0일 수 있음|
|썸네일 데이터|3 × n|압축되지 않은 24비트 RGB 래스터 썸네일 데이터|

### JFIF 확장 APP0 마커 세그먼트 ###

이것은 정의된 경우 JFIF APP0 마커 세그먼트 바로 뒤에 와야 하는 선택적 섹션입니다. 이 섹션은 JFIF 버전 1.02 이상에서 지원되며 세 가지 다른 형식으로 축소판을 포함할 수 있습니다.

|필드|크기(바이트)|설명|
|---|---|---|
|APP0 마커|2|FF E0|
|길이|2|APP0 마커를 제외한 세그먼트의 길이|
|식별자|5|널 바이트로 종료되는 ASCII의 JFXX(4A 46 58 58 00)|
|썸네일 형식|1|다음 포함된 썸네일에 사용되는 데이터 형식을 지정합니다.</br> 10 : JPEG 형식</br> 11: 픽셀당 1바이트 팔레트 형식</br> 13: 픽셀당 3바이트 RGB 형식|
|썸네일 데이터|변수||

## JFIF를 다른 이미지 파일 형식으로 변환

JFIF는 [PNG](/ko/image/png/), [JPG](/ko/image/jpg/) 및 [PDF](/ko/pdf/)와 같은 널리 사용되는 이미지 파일 형식으로 변환할 수 있습니다.

## 참조 ##

- [JFIF - 위키피디아](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

