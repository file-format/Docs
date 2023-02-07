{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZST 파일 - Zstandard 압축 파일 형식",
  "description":"ZST 파일을 만들고 열 수 있는 ZST 파일 형식 및 API에 대해 알아봅니다.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## .ZST 파일이란?

ZST 파일은 Zstandard(zstd) 압축 알고리즘으로 생성된 압축 파일입니다. 알고리즘에 의해 무손실 압축으로 생성된 압축 파일입니다. ZST 파일은 데이터베이스, 파일 시스템, 네트워크 및 게임과 같은 다양한 유형의 파일을 압축하는 데 사용할 수 있습니다. Zstandard는 전체 압축 메커니즘, 미디어 유형 및 콘텐츠 인코딩을 설명하는 [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878)에 의해 관리됩니다.

## ZST 파일 형식

ZST 파일은 압축 파일 형식으로 디스크에 저장됩니다. 압축 메커니즘은 RFC 8478을 폐기하는 RFC 8878에 설명되어 있습니다.

## ZST 프레임

ZST 파일은 하나 이상의 프레임으로 구성됩니다. 각 프레임은 Zstandard 프레임이거나 건너뛸 수 있는 프레임일 수 있습니다. Zstandard 프레임에는 압축된 데이터가 포함되는 반면 건너뛸 수 있는 프레임에는 사용자 지정 사용자 메타데이터가 포함됩니다.

### Z스탠다드 프레임

Zstandard 프레임은 다음과 같은 구조를 가집니다.

|필드|크기(바이트)|
---|---|
|Magic_Number |4바이트|
|Frame_Header |2-14바이트|
|Data_Block |n 바이트|
|[더 많은 Data_Blocks] ||
|[Content_Checksum] |4바이트|

### 건너뛸 수 있는 프레임

건너뛸 수 있는 프레임을 사용하면 연결된 프레임 흐름에 사용자 정의 메타데이터를 삽입할 수 있습니다. 건너뛸 수 있는 프레임의 구조는 다음과 같습니다.

|Magic_Number |프레임 크기 |사용자 데이터|
---|---|---|
|4바이트 |4바이트 |n바이트|

## 참조 ##

* [RFC 8878 Z표준 압축](https://www.rfc-editor.org/rfc/rfc8878)

