{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "파일", "확장자", "파일 형식", "페이지 레이아웃", "캡슐화된 포스트스크립트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPS 파일 형식과 EPS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"EPS 파일 형식 - 캡슐화된 포스트스크립트 파일",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .EPS 파일이란?

.eps 파일은 캡슐화된 포스트스크립트 파일 형식으로 디스크에 저장되는 이미지 파일입니다. 텍스트, 그래픽 및 이미지의 조합을 포함할 수 있습니다. EPS 파일에는 이러한 파일을 열 수 있는 응용 프로그램에서 표시할 수 있도록 내부에 캡슐화된 비트맵 미리 보기 이미지가 포함될 수도 있습니다.

## EPS 파일 형식의 간략한 역사

기록 관점에서 EPS 파일 형식을 간단히 살펴보면 다음 정보를 알 수 있습니다.

* EPS의 첫 번째 버전은 1985년에서 1988년 사이에 Adobe에서 출시되었습니다.
* EPS 사양의 버전 2.0은 1989년 1월에 발행되었습니다.
* EPS 3.0 버전에 대한 사양은 1992년에 별도의 문서로 발행되었습니다. 이것은 가장 최근에 출판된 버전입니다.

EPS는 Adobe의 PostScript 언어 문서 구조화 규칙 사양의 9절에 설명된 개방형 구조화 규칙 확장 메커니즘과 함께 Adobe Illustrator 아트워크 파일 형식의 초기 버전의 기초를 형성했습니다.

## EPS 파일 형식

EPS는 독점적이지만 공개적으로 문서화된 형식이며 EPS 파일 형식 사양은 개발자가 참조할 수 있도록 공개되어 있습니다. EPS는 [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions)(Document Structuring Convention)를 준수하는 파일 형식이며 DSC에서 설정한 모든 규칙을 준수합니다. DSC는 Adobe의 PostScript 문서용 특수 파일 형식입니다. EPS 파일을 읽을 수 있다고 주장하는 모든 응용 프로그램은 DSC를 준수해야 합니다.

EPS 파일은 아래 설명된 대로 두 가지 주요 섹션으로 구성됩니다.

### 미리보기 이미지 ###

일반적인 EPS 파일에는 여러 시스템 또는 응용 프로그램과 관련된 워크플로에서 편리하게 사용할 수 있는 형식의 미리 보기 이미지가 포함되어 있습니다. 미리 보기의 목적은 대부분의 그래픽 응용 프로그램이 렌더링할 수 있는 형식의 이미지를 갖는 것입니다. 미리보기는 일반적으로 픽셀 치수 및/또는 비트 심도에서 저해상도입니다. 미리보기 파일은 여러 형식 중 하나일 수 있습니다. EPS_3 사양에는 세 가지 "기기별" 미리보기 형식이 나열되어 있습니다.

* Apple Macintosh의 경우 QuickDraw 응용 프로그램에서 사용하는 PICT 이미지
* DOS 컴퓨터의 경우 TIFF 비트맵
* 윈도우 메타파일.

PICT 및 Windows 메타파일은 비트맵 데이터와 벡터 그래픽을 모두 통합할 수 있습니다. 또한 사양은 포함된 비트맵 미리 보기 이미지에 대한 매우 간단한 장치 독립적 표현을 정의합니다. 이 표현을 EPSI(Encapsulated PostScript Interchange Format)라고 합니다.

EPSI 미리 보기는 ASCII 16진수로 표시되는 비트맵으로, 식별을 위해 몇 개의 PostScript 주석으로 둘러싸여 있으며 간단하고 쉽게 이동할 수 있습니다. 미리보기 형식이 다른 EPS 파일을 구별하기 위해 EPS 사양에서는 다른 DOS 파일 확장자와 Macintosh 파일 형식을 권장했습니다.

### 포스트스크립트 코드

EPS 파일 형식에는 최소한 다음이 포함되어야 합니다.

* 헤더 주석, %!PS-Adobe-3.0 EPSF-3.0
* 및 그림의 경계를 설명하는 경계 상자 주석 %%BoundingBox: llx lly urx ury. 이 4개의 인수는 경계 상자의 왼쪽 아래(llx, lly) 및 오른쪽 위(urx, ury) 모서리에 해당합니다.

EPS 파일은 다음 연산자를 사용할 수 없습니다.

* 밴드 장치,
* 클리어딕트스택
* 카피페이지
* 지우기 페이지
* 출구 서버
* 프레임 장치
* 그레스토어올
* 초기화
* 이니그래픽스
* 초기 매트릭스
* 그만두다
* 렌더밴드
* 세트글로벌
* 설정 페이지 장치
* 집합 공유
* 시작 작업.

## EPS를 다른 파일 형식으로 변환

EPS 파일은 [JPG](/ko/image/jpeg/), [PNG](/ko/image/png/), [TIFF](/ko/image/tiff/) 및 [PDF](/ko/pdf)와 같은 표준 이미지 형식으로 변환할 수 있습니다. /) Adobe Illustrator, Photoshop 및 PaintShop Pro와 같은 다른 응용 프로그램을 사용합니다.

[보안 취약점](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) EPS 파일의 Office 2016, Office 2013, Office 2010 및 Office 365는 EPS 파일을 Office 문서에 삽입하는 기능을 해제했습니다.

## 참고문헌

* [Encapsulated PostScript - By Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

