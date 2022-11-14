{
  "date" : "2019-12-09",
  "keywords" :[ "zl 파일", "zl 파일 형식", "zl 파일이란", "파일", "zl 예제", "zl 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP 압축 파일 형식",
  "description":"ZL 파일 형식과 ZL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## .ZL 파일이란?

확장자가 .zl인 파일은 파일 압축을 위해 DEFLATE 압축 알고리즘의 변형을 사용하는 ZLIP 압축 파일 형식입니다. CPU 유형, 운영 체제, 파일 시스템, 문자 집합과 무관하므로 정보 교환에 사용할 수 있습니다. ZLIP 압축 기술 사양은 [IETF 사이트](https://tools.ietf.org/html/rfc1950)에서 확인할 수 있으며 개발자 입장에서 참고할 수 있다.

## ZL 파일 형식

zlib 스트림의 구조는 다음과 같습니다.

* `CMF(Compression Method and flags)` - 이 바이트는 압축 방식에 따라 4비트 압축 방식과 4비트 정보 필드로 구분된다.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Compression method)` - 파일에 사용된 압축 방식을 식별합니다. 그 값과 해당 압축 방법은 다음과 같습니다.

| CM 가치| 압축|
|---|---|
|CM = 8|최대 32K의 창 크기로 DEFLATE|
|CM = 15|예약됨|

* `CINFO(압축 정보)` - CM = 8의 경우 CINFO는 LZ77 창 크기의 밑이 2인 로그에서 8을 뺀 값입니다(CINFO=7은 32K 창 크기를 나타냄).

* `FLG(FLaGs)` - 이 플래그 바이트는 다음과 같이 나뉩니다.
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## 참조 ##

* [Zlib 파일 형식 사양](https://tools.ietf.org/html/rfc1950)

