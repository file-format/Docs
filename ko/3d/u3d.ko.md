{
  "date" : "2019-10-11",
  "keywords" :[ "u3d 파일", "u3d 파일 형식", "u3d 파일이란", "파일", "u3d 예제", "u3d 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - 범용 3D 파일 형식",
  "description":"U3D 파일 형식과 U3D 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .U3D 파일이란?

**U3D**(Universal 3D)는 3D 컴퓨터 그래픽을 위한 압축 파일 형식 및 데이터 구조입니다. 삼각형 메쉬, 조명, 음영, 모션 데이터, 색상 및 구조가 있는 선 및 점과 같은 3D 모델 정보가 포함되어 있습니다. 형식은 2005년 8월에 [ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) 표준으로 승인되었습니다. 3D [PDF](/ko/pdf/) 문서는 U3D를 지원합니다. 개체 포함 및 Adobe Reader(버전 7 이상)에서 볼 수 있습니다.

U3D 형식은 3차원 데이터 저장 및 교환에 대한 보편적인 표준을 수립하는 것을 목표로 개발되었습니다. 그러나 이 형식은 교환 형식으로 사용되지 않고 3D PDF 인코딩에 주로 활용됩니다. Acrobat 3D는 지원되는 3D 파일 유형을 PDF로 변환할 때 U3D 또는 PRC로 변환합니다.

## U3D 파일 형식

U3D 파일은 [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) 참조 문서에 설명된 대로 4가지 버전을 거친 바이너리 파일 형식으로 사양 업데이트 각 에디션과 함께. PDF 파일 표준 ISO-32000은 U3D를 주석 및 멀티미디어 유형으로 허용합니다.

U3D의 초판은 지오메트리, 색상, 텍스처, 조명, 뼈대 및 변형 기반 애니메이션과 같은 3D 그래픽 속성의 주요 표현에 중점을 두었습니다. 두 번째 및 세 번째 버전은 첫 번째 버전의 일부 정오표를 수정했으며 세 번째 버전은 업계 소프트웨어에서 가장 일반적으로 사용되는 유형입니다. 네 번째 판은 고차 기본체(곡면)에 대한 정의를 제공합니다. [U3D 사양](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)은 ECMA 웹사이트에서 사용자 참조용으로 온라인으로 제공됩니다.

### U3D 파일의 데이터 유형

바이너리 파일에는 U8, U16, U32, U64, I16, I32, F32, F64 및 String 유형이 포함됩니다.

* U8 : 부호 없는 8비트 정수
* U16 : 부호 없는 16비트 정수
* U32 : 부호 없는 32비트 정수
* U64 : 부호 없는 64비트 정수
* I16 : 부호 있는 16비트 정수
* F32: IEEE 단정밀도 부동 소수점.
* F64: IEEE 배정밀도 부동 소수점.
* 문자열: U3D 파일의 문자열은 문자열의 전체 문자 길이를 정의하는 부호 없는 16비트 정수로 시작합니다. 문자열은 항상 대소문자를 구분하여 처리됩니다.

## U3D 파일 구조

U3D 파일에는 일련의 블록이 포함되어 있습니다. 각 U3D 파일에는 3가지 유형의 블록이 있습니다.

* 파일 헤더 블록
* 선언 블록
* 연속 블록

로더는 해당 블록의 데이터가 필요하지 않거나 해당 블록 유형에 대한 디코더를 사용할 수 없는 경우 블록의 끝을 결정합니다.

{{< figure src="../u3d.png" alt="U3D 파일 형식" >}}

### 파일 헤더 블록
파일 헤더 블록에는 로드된 파일에서 파일을 읽는 방법을 결정하는 데 사용되는 파일 정보가 포함되어 있습니다.

### 선언 블록

선언 블록에는 파일의 개체에 대한 정보가 포함됩니다. 선언 블록의 개체를 정의해야 합니다.

### 연속 블록

선언 블록에서 선언된 개체에 대한 추가 정보는 연속 블록에서 제공됩니다. 각 연속 블록은 선언 블록과 연결되어야 합니다.


## 참조 ##

* [U3D 파일 형식 - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D 파일 형식 사양](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

