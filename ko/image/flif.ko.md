---
date: 2020-08-12
keywords: flif, .flif, flif 파일 형식, flif 파일을 여는 방법, .flif 확장자, flif 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF 파일 형식
linktitle: FLIF
description: "FLIF 파일 형식과 FLIF 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## .FLIF 파일이란? ##

FLIF(무료 무손실 이미지 형식)는 파일에 .flif 확장자를 사용하는 무손실 이미지 형식입니다. FLIF는 압축 비율 측면에서 [PNG](/ko/image/png/), 무손실 [WebP](/ko/image/webp/), 무손실 BPG 및 무손실 JPEG 2000보다 성능이 우수하다고 주장합니다. FLIF는 프로그레시브 인터레이스를 사용하므로 이미지의 부분 다운로드가 전체 이미지에 대한 손실 인코딩으로 사용될 수 있습니다.

## 간략한 역사 ##

FLIF는 2015년 9월에 발표되었고 알파 버전은 2015년 10월에 출시되었습니다. 2016년 9월에는 FLIF의 첫 번째 안정 버전이 출시되었습니다.

## FLIF 디자인 ##

FLIF는 압축을 위해 CABAC(Context-adaptive Binary arithmetic Coding), MANIAC(Meta-Adaptive Near-zero Integer Arithmetic Coding)의 변형을 사용합니다. MANIAC는 Jon Sneyers와 Pieter Wuille이 개발한 엔트로피 코딩 알고리즘입니다. MANIAC에서 컨텍스트는 인코딩 시간에 동적으로 학습되는 결정 트리의 노드입니다. 이렇게 하면 컨텍스트 모델이 이미지에 따라 달라지고 압축이 더 잘 됩니다. FLIF에는 다음과 같은 기능이 있습니다.

- 무손실 압축 지원
- 인코더 전처리로 손실 압축 지원
- 그레이스케일, RGB 및 RGBA 지원
- 채널당 1~16비트의 색심도 지원
- 인터레이스 및 비인터레이스 파일 지원
- 부분적으로 다운로드된 파일의 점진적 디코딩 지원
- 애니메이션 지원
- 임베디드 ICC 색상 프로파일, Exif 및 XMP 메타데이터 지원
- Camera Raw 파일(RGGB) 압축 지원이 제한됨

## FLIF 파일 형식 ##

FLIF 파일에는 다음 네 부분이 있습니다.

## 메인 헤더 ##

기본 헤더에는 너비, 높이, 색상 깊이, 프레임 수를 포함한 기본 메타데이터가 포함됩니다.

|유형|값|설명|
|---|---|---|
|4바이트|"FLIF"|마법|
|4비트|3 = ni 여전히; 4 = 나는 여전히; 5 = ni 님; 6 = i anim|인터레이스, 애니메이션|
|4비트|1 = 회색조; 3 = RGB; 4 = RGBA|채널 수(nb_channels)|
|1바이트|'0','1','2' ('0'=사용자 정의)|채널당 바이트(Bpc)|
|varint|너비-1|너비|
|varint|높이-1|높이|
|varint|nb_frames-2(애니메이션인 경우에만)|프레임 수(nb_frames)|

## 메타데이터 청크 ##

이 부분에는 DEFLATE 압축을 사용하여 인코딩된 Exif/XMP 메타데이터, ICC 색상 프로필 등과 같은 비픽셀이 포함됩니다. 이러한 청크는 PNG 청크와 유사하게 정의되지만 척 크기가 가변 바이트 수로 인코딩된다는 차이점이 있습니다. 청크의 이름은 4자(4바이트)이거나 선택 사항이 아닌 청크를 나타내는 32 미만의 값일 수 있습니다.

다음은 옵션 척의 예입니다.

|청크 이름|설명|내용(DEFLATE 압축 해제 후)|
|---|---|---|
|iCCP|ICC 색상 프로필|원시 ICC 색상 프로필 데이터|
|eXif|Exif 메타데이터|"Exif\0\0" 헤더 다음에 TIFF 헤더 및 EXIF 데이터|
|eXmp|XMP 메타데이터|패딩이 없는 읽기 전용 xpacket에 포함된 XMP|

### 명명 규칙 ###

- **첫 글자**: 중요한 청크에는 대문자를 사용하고 중요하지 않은 청크에는 소문자를 사용합니다.
- **Second Letter**: public 청크는 대문자, private 청크는 소문자 사용
- **세 번째 글자**: 이미지를 올바르게 표시하는 데 필요한 척은 대문자를 사용하고 이미지를 표시하는 데 소문자는 중요하지 않습니다.
- **네번째 글자**: 맹목적으로 안전하게 복사할 수 있는 척은 대문자를 사용합니다. 소문자 척은 이미지 데이터에 따라 다릅니다.

## 두 번째 헤더 ##

여기에는 픽셀의 실제 인코딩에 대한 정보가 포함됩니다.

|유형|설명|조건|기본값|
|---|---|---|---|
|1 바이트|NUL 바이트(0x00), FLIF16 비트스트림의 청크 이름||
|uni_int(1,16)|채널의 픽셀당 비트 수|Bpc == '0': repeat(nb_channels)|Bpc == '1'이면 8, Bpc == '2'이면 16|
|uni_int(0,1)|플래그: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|루프 수|nb_frames > 1||
|uni_int(0,60_000)|ms 단위의 프레임 지연|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|플래그: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|컷오프|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|알파 제수|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|플래그: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|변수|변환(아래 참조)|||
|uni_int(1) = 0|표시 비트: 변환 완료|||
|uni_int(0,2)|보이지 않는 픽셀 예측기|alpha_zero && 인터레이스 && 알파 범위에 0이 포함됨||

**채널**

|채널 번호|설명|
|---|----|
|0|빨간색 또는 회색|
|1|녹색|
|2|파란색|
|3|알파|

**변환**

|유형|설명|
|---|---|
|uni_int(1) = 1|표시 비트: 아직 완료되지 않음|
|uni_int(0,13)|변환 식별자|
|변수|변환 데이터(변환에 따라 다름)|

변환은 더 나은 압축을 위해 픽셀 데이터를 수정하고 실제로 발생하는 픽셀 값을 추적하는 데 사용됩니다.

## 픽셀 데이터 ##

이 부분은 MANIAC 엔트로피 코딩을 사용하여 인코딩된 실제 픽셀 데이터를 포함합니다. 픽셀은 인터레이스 또는 비인터레이스 인코딩을 사용하여 인코딩될 수 있습니다.

### 인터레이스 방식 ###

이 방법에서는 확대/축소 수준이 정의됩니다. Zoomlevel 0은 전체 이미지에 사용되며, zoomlevel 1은 모든 짝수 행에 사용되며, zoomlevel 2는 zoomlevel 1의 모든 짝수 열에 사용됩니다. 이미지, 축척 1:2^k. Zoomlevel은 가장 높은 것에서 가장 낮은 것으로 인코딩됩니다.

### 비인터레이스 방식 ###

이 방법에서 MANIAC 트리의 인코딩이 시작되고 바로 픽셀 인코딩이 이어집니다.

## 참조 ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [플리프](http://flif.info/)

