---
date: 2022-01-31
keywords: stp, .stp, stp 파일 형식, stp 파일을 여는 방법, .stp 확장자, stp 확장자
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP 파일 형식
linktitle: STP
description: "STP 파일 형식 및 STP 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## .STP 파일이란?

STP 파일은 CAD와 CAM 응용 프로그램 간의 제품 데이터 교환에 사용되는 3D CAD 파일입니다. 3D 개체에 대한 정보가 포함되어 있으며 **STEP** 파일 형식과 유사하게 저장됩니다. STP 파일은 [STEP](/ko/3d/step/) 응용 프로그램 프로토콜 ISO 10303-2xx에 따라 응용 프로그램 간의 데이터 교환을 용이하게 합니다. 이 ISO는 EXPRESS 데이터 모델링 언어에서 데이터 표현을 위한 인코딩 메커니즘을 정의합니다. STP 파일은 **Autodesk Fusion 360**과 같은 응용프로그램에서 열 수 있습니다.

## STP 파일 형식 - 추가 정보

STP 파일은 일반 ASCII 파일 형식으로 디스크에 저장됩니다. 여기에는 이러한 모델을 로드하기 위해 CAD/CAM 응용 프로그램에서 읽을 수 있는 일반 텍스트로 3D 모델 정보가 포함됩니다.

STP 파일도 .step 확장자로 저장되며 일련의 레코드로 구성됩니다. 이러한 파일에 대한 두드러진 기능은 다음과 같습니다.

* 문자 집합은 ISO 10646의 코드 포인트로 정의됩니다.
* "ISO-10303-21;" 첫 번째 레코드의 첫 번째 문자입니다.
* 주석은 "/*" 및 "*/" 문자로 둘러싸여 있습니다.
* 마지막 레코드에는 "END-ISO-10303-21;"이 포함되어 있습니다. STEP 파일이 2002 버전을 따르는 경우.
* 2016 버전에 부합하는 경우 "END-ISO-10303-21" 뒤에 하나 이상의 전자 서명이 있을 수 있습니다. 터미네이터.
* 줄 바꿈은 "\N\"으로 표시되고 페이지 나누기는 "\F\"로 표시됩니다.

## STP 파일 열기

STP 파일은 STP 뷰어와 텍스트 편집기에서 열 수 있습니다.

### STP 뷰어로 STP 파일 열기

다양한 CAD 응용 프로그램은 Windows, MacOS 및 Linux에서 볼 수 있도록 STP 파일을 열 수 있습니다. 여기에는 다음이 포함됩니다.

* Autodesk Fusion 360(교차 플랫폼)
* FreeCAD(크로스 플랫폼)
* IMSI TurboCAD(윈도우, 맥)
* Dassault Systems CATIA(Windows, Linux)

### 텍스트 편집기로 STP 파일 열기

STP 파일은 일반 텍스트 파일로 저장됩니다. 이를 통해 텍스트 편집기로 STP 파일을 열 수 있습니다. Windows OS의 Notepad 및 Notepad++ 및 MacOS의 Apple TextEdit와 같은 인기 있는 텍스트 편집기는 STP 파일을 열 수 있습니다. 텍스트 편집기에서 열리면 사용자는 STP 파일의 속성을 편집할 수 있습니다. 그러나 속성을 잘못 업데이트하면 파일이 손상될 수 있습니다.

## STP 파일을 변환하는 방법

STP 파일을 다른 파일 형식으로 변환할 수 있는 여러 응용 프로그램이 있습니다. STP 파일을 변환할 수 있는 CAD 응용 프로그램은 다음과 같습니다.

* 오토데스크 퓨전 360
* IMSI 터보캐드
* 지멘스 솔리드 에지

이 외에도 STP 파일을 다른 파일 형식으로 변환할 수 있는 여러 온라인 앱이 있습니다. 이러한 온라인 앱을 사용하면 STP 파일을 클라우드 서버에 업로드하여 원하는 형식으로 변환하고 다운로드를 위해 다시 반환할 수 있습니다.

Autodesk Fusion 360은 STP 파일을 다음 3D 및 CAD 파일 형식으로 변환할 수 있습니다.

* [OBJ](/ko/3d/obj/)
* [3MF](/ko/3d/3mf/)
* [DWG](/ko/cad/dwg/)
* [DXF](/ko/cad/dxf/)
* [ASM](/ko/cad/asm/)
* [IGES](/ko/cad/iges/)
* [STL](/ko/cad/stl/)
* [FBX](/ko/3d/fbx/)
* F3D
* [미국 달러](/ko/3일/미국 달러/)

## 참고문헌

* [ISO 10303-21 - 위키피디아](https://en.wikipedia.org/wiki/ISO_10303-21)
* [오토데스크 퓨전 360](https://www.autodesk.com/products/fusion-360/overview)

