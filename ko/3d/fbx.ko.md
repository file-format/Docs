{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "파일", "확장자", "형식", "3D 파일 형식"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FBX 파일과 이를 생성하고 열 수 있는 API가 무엇인지 알기 위한 파일 형식 가이드",
  "title" :"FBX - FilmBox 3D 파일 형식",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .FBX 파일이란?

FBX, FilmBox는 원래 Kaydara에서 MotionBuilder용으로 개발한 인기 있는 3D 파일 형식입니다. 2006년 Autodesk Inc에 인수되었으며 현재 많은 3D 도구에서 사용되는 주요 3D 교환 형식 중 하나입니다. FBX는 바이너리 및 ASCII 파일 형식으로 제공됩니다. 형식은 디지털 콘텐츠 생성 응용 프로그램 간의 상호 운용성을 제공하기 위해 설정되었습니다. FBX 파일 형식에서/로 변환하는 데 사용할 수 있는 도구가 많이 있습니다.

## FBX 파일 형식 - 추가 정보

FBX는 독점 형식이며 바이너리 파일 형식에 대한 사양은 공식적으로 제공되지 않습니다. Autodesk는 FBX 파일에서 읽기, 쓰기 및 변환을 위해 C++ FBX SDK를 제공합니다. FBX용 Python 가져오기 및 내보내기 스크립트는 FBX SDK를 사용하지 않는 블렌더 소프트웨어에서도 사용할 수 있습니다.

### 텍스트 기반 파일 구조

텍스트 기반 파일 구조는 명확하게 명명된 식별자로 문서화된 트리 구조입니다. 각 노드에 다음이 있는 계층 구조로 배열된 노드의 중첩 목록으로 구성됩니다.

* NodeType 식별자(클래스 이름)
* 관련된 속성의 튜플, 튜플 요소는 일반적인 기본 데이터 유형입니다: ##float, integer, string## 등.
* 동일한 형식(재귀적으로)의 노드를 포함하는 목록입니다.

다음과 같이 논리적으로 나타낼 수 있습니다.

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

일부 표준 노드는 각 항목이 중첩 목록으로 구성된 암시적 목록으로 정의됩니다. FBX 지오메트리에 액세스하려는 모든 응용 프로그램은 이러한 콘텐츠를 구문 분석하고 유용한 의미를 만들어야 합니다. 텍스트 기반 FBX 파일의 예는 다음과 같습니다.

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## FBX 파일의 바이너리 파일 구조

앞서 언급했듯이 FBX 파일 형식 사양은 FBX에 대해 공개적으로 제공되지 않습니다. 블렌더 파운데이션은 회사에서 제공하는 SDK를 사용하지 않고 FBX 파일 형식을 구현하기 때문에 바이너리 파일 형식에 대한 일부 세부 정보는 [사용 가능](https://code.blender.org/2013/08/fbx-binary-file-format -specification/) 구현의 일부로.

이진 파일 구조는 다음 순서를 따릅니다.

* 헤더
* 개체 기록
* 바닥글

### FBX 헤더

파일 헤더 정보는 27바이트로 구성됩니다.

* 바이트 0 - 20: Kaydara FBX 바이너리 \x00(파일 매직, 끝에 공백 2개, NULL 종료자 포함).
* 바이트 21 - 22: [0x1A, 0x00]##(알 수 없지만 관찰된 모든 파일에 이 바이트가 표시됨).
* 바이트 23 - 26: unsigned int, 버전 번호. 예를 들어 버전 7.3의 경우 7300입니다.

### 개체 레코드 ###

헤더 다음에 빈 이름과 빈 속성 목록이 있는 전체 노드 레코드인 개체 레코드가 옵니다. 전체 파일 구성을 재귀적으로 포함합니다.

### 바닥글 ###

FBX 바닥글 섹션은 내용을 알 수 없는 파일의 끝에 있습니다.

## 레코드 형식 ##

FBX 파일의 레코드는 다음과 같이 분류됩니다.

* 노드 레코드
* 재산 기록

### 노드 레코드 형식 ###

각 노드 레코드 형식에는 이름이 지정되며 다음과 같은 메모리 레이아웃이 있습니다.


|크기(바이트)|날짜 유형|이름
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|네임렌
|이름길이|문자|이름
|?|?|속성[n], 여기서 n = 0:PropertyListLen
|선택사항| |
|?|?|중첩 목록
|13|uint8[]|널 레코드

어디:

* 'EndOffset'은 파일 시작에서 노드 레코드 끝까지의 거리입니다(즉, 다음에 오는 모든 것의 첫 번째 바이트). 이것은 알 수 없거나 필요하지 않은 레코드를 쉽게 건너뛰는 데 사용할 수 있습니다.
* `NumProperties`는 노드와 연결된 값 튜플의 속성 수입니다. 마지막 요소인 중첩 목록은 속성으로 계산되지 않습니다.
* `PropertyListLen`은 속성 목록의 길이입니다. 속성의 데이터 유형에 따라 ##NumProperties## 속성을 저장하는 데 필요한 크기입니다.
* 'NameLen'은 개체 이름의 길이(문자)입니다. 이것이 0인 유일한 경우는 목록의 최상위 수준인 것 같습니다.
* '이름'은 개체의 이름입니다. 제로 터미네이션은 없습니다.
* `속성[n]`은 n번째 속성입니다. 형식은 섹션 속성 레코드 형식을 참조하세요. 속성은 패딩 없이 순차적으로 작성됩니다.
* `NestedList`는 중첩된 목록으로, 맨 끝에 NULL 레코드가 표시됩니다.

중첩 목록 항목의 존재는 EndOffset에 도달할 때까지 남은 바이트가 있는지 확인하여 결정할 수 있습니다. 그렇다면 다음 개체 레코드는 마지막 속성 바로 다음에 읽어야 합니다. 그런 다음 개체 레코드는 13개의 0바이트를 따르고 이 바이트는 EndOffset과 결합됩니다. NULL 항목의 목적이나 요구 사항은 알려져 있지 않으며 일부 형식 기능을 가리킬 수 있습니다.

### 부동산 기록 형식 ###

속성 레코드에는 노드의 일부인 속성에 대한 세부 정보가 포함됩니다. 속성 레코드에는 다음과 같은 메모리 레이아웃이 있습니다.


|크기(바이트)|데이터 유형|이름
--- | --- | ---
|1|문자|타입코드
|?|?|데이터

TypeCode는 유사한 처리가 필요한 그룹으로 정렬된 문자 코드를 나타냅니다. TypeCode는 다음과 같은 유형으로 분류할 수 있으며 TypeCode는 이러한 유형 중 문자 코드 중 하나일 수 있습니다.

#### 기본 유형 ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

기본 스칼라 유형 레코드의 데이터는 리틀 엔디안 바이트 순서로 값의 정확히 이진 표현입니다.

#### 배열 유형 ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

배열 유형에 대한 데이터는 더 복잡하며 다음 구조로 되어 있습니다.


|크기(바이트)|데이터 유형|이름
--- | --- | ---
|4|Uint32|배열 길이
|4|Uint32|인코딩
|4|Uint32|압축 길이
|?|?|내용

### 특수 유형 ###

다음은 특수 유형 TypeCodes입니다.

```
S: String
R: raw binary data
```

이 두 TypeCode는 모두 다음과 같이 표시됩니다.


|크기(바이트)|데이터 유형|이름
--- | --- | ---
|4|Uin32|길이
|길이| |

문자열은 0으로 끝나는 것이 아니며 \0 문자를 포함할 수 있습니다(이는 실제로 일부 FBX 속성에서 사용됨).

## 참조 ##

* [FBX - Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [FBX 바이너리 파일 형식 사양](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - 위키피디아](https://en.wikipedia.org/wiki/FBX#File_format)

