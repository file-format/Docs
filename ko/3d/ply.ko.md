{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "파일", "확장자", "형식", "3D 파일 형식"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"PLY 파일 형식과 PLY 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"PLY - 다각형 3D 파일 형식",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .PLY 파일이란?

PLY(Polygon File Format)는 다각형 모음으로 설명되는 그래픽 개체를 저장하는 3D 파일 형식을 나타냅니다. 이 파일 형식의 목적은 광범위한 모델에 유용할 만큼 충분히 일반적이고 간단하고 쉬운 파일 형식을 설정하는 것입니다. PLY 파일 형식은 ASCII 및 바이너리 형식으로 제공되어 컴팩트하게 저장하고 빠르게 저장하고 로드할 수 있습니다. 파일 형식은 3D 파일 읽기를 지원하는 다양한 응용 프로그램에서 사용됩니다.

PLY 형식의 개체는 꼭짓점, 면 및 기타 요소의 컬렉션과 함께 이러한 요소에 연결할 수 있는 색상 및 법선 방향과 같은 속성으로 설명됩니다. 개체와 함께 저장할 수도 있는 기타 속성은 다음과 같습니다.

* 표면 법선
* 텍스처 좌표
* 투명도
* 범위 데이터 신뢰도
* 폴리곤의 앞뒤 속성

PLY 형식으로 표현되는 개체는 손으로 디지털화한 개체, 모델링 응용 프로그램의 다각형 개체, 범위 데이터, 행진 큐브의 삼각형, 지형 데이터 및 라디오시티 모델과 같은 다양한 소스의 결과일 수 있습니다.

## 약력

PLY 형식은 1990년대에 Greg Turk와 Stanford 그래픽 연구소의 다른 사람들에 의해 개발되었으므로 Stanford Triangle 형식이라고도 합니다. 그 이후로 파일 형식은 버전 1.0이며 더 이상 수정되지 않았습니다.

## PLY 파일 형식

단순 PLY 객체는 객체 표현을 위한 요소 모음으로 구성됩니다. 꼭짓점의 (x,y,z) 트리플 목록과 꼭짓점 목록의 실제로 인덱스인 면 목록으로 구성됩니다. 정점과 면은 요소의 두 가지 예이며 대부분의 PLY 파일은 이 두 요소로 구성됩니다. 새 속성을 만들어 개체의 요소에 연결할 수도 있지만 이러한 새 속성이 발견될 때 이전 프로그램이 중단되지 않도록 이러한 속성을 추가해야 합니다. 이러한 속성은 응용 프로그램을 읽을 때도 삭제할 수 있습니다. 또한 이 요소를 사용하여 새 요소를 만들고 속성을 정의할 수도 있습니다.

### 파일 구조

PLY 파일 형식의 파일 구조는 다음과 같습니다.

|필드
---|
|파일 헤더
|정점 목록
|페이스리스트
|기타 요소 목록

#### 예제 구조

PLY 파일 형식의 다양한 부분에 대한 후속 논의에서 아래의 예를 사용합니다.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### 파일 헤더

PLY 파일 형식 헤더는 ASCII 및 바이너리 형식 모두에 대한 ASCII 텍스트로 구성됩니다. 헤더 섹션의 시작과 끝은 ply 및 end-header 키워드로 식별됩니다. 헤더의 시작 부분에는 독자가 PLY 파일 형식을 인식하는 데 사용되는 매직 워드 ply가 있습니다. 다음 줄은 이 파일의 버전 번호를 보여줍니다. PLY 파일 형식의 주석은 각 주석 행의 시작 부분에 주석 키워드로 시작합니다.

#### 요소 키워드

그런 다음 element 키워드는 파일 내부에 있는 내용을 알려줍니다. 각 속성에는 아래와 같이 지정된 속성 유형 및 순서가 있는 특정 요소 유형에 대한 속성이 뒤에 옵니다.

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

이 특정 예에서 특정 정점 요소에는 순서가 지정된 float 유형의 3가지 속성이 있습니다.

#### 데이터 유형의 유형

속성이 가질 수 있는 데이터 유형에는 두 가지 유형이 있습니다.

'스칼라': 스칼라 데이터 유형은 다음과 같습니다.

|#이름|#유형|#바이트 수
|문자|문자|1
|uchar|서명되지 않은 문자|1
|짧은|짧은 정수|2
|ushort|부호 없는 짧은 정수|2
|int|정수|4
|uint|부호 없는 정수|4
|float|단정밀도 float|4
|배정밀도|배정밀도 부동 소수점|8

'목록': 목록 데이터 유형을 사용하는 특별한 형태의 속성 정의가 있습니다. 이에 대한 예는 위의 큐브 파일에서 가져온 것입니다.

`속성 목록 uchar int vertex_index`

이것은 "vertex_index" 속성이 먼저 속성에 포함된 인덱스 수를 알려주는 부호 없는 문자를 포함하고 그 뒤에 해당하는 정수를 포함하는 목록을 포함한다는 것을 의미합니다. 이 가변 길이 목록의 각 정수는 꼭짓점에 대한 인덱스입니다.

## 참조 ##

* [PLY 파일 형식](http://paulbourke.net/dataformats/ply/)
* [PLY - 위키피디아 작성](https://en.wikipedia.org/wiki/PLY_(file_format))

