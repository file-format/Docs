{
  "date" : "2019-10-11",
  "keywords" :[ "b6z 파일", "b6z 파일 형식", "b6z 파일이란", "파일", "b6z 예제", "b6z 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP 아카이브 파일 형식",
  "description":"B6Z 파일 형식과 B6Z 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## .B6Z 파일이란?

확장자가 .b6z인 파일은 macOS 소프트웨어 응용 프로그램[B6Zip](http://b6zip.com)을 생성하여 파일을 압축 및 압축 해제하는 데 사용되는 압축 아카이브 파일입니다. 압축률을 높일 수 있는 비교적 새로운 아카이브 형식입니다. B6Z는 개방형 아키텍처를 가지고 있으며 최대 900000PB의 파일 크기를 지원합니다. 데이터 압축, 오류 복구 및 파일 스패닝을 지원합니다. B6Zip 유틸리티 소프트웨어는 MacOS에서 무료로 제공되어 B6Z를 포함한 다양한 유형의 압축 파일을 열 수 있습니다.

## B6Z 파일 형식

B6Z 파일 형식은 개방형 아키텍처를 기반으로 하며 AES-256 암호화 알고리즘으로 견고한 압축을 제공합니다. 기본 압축 방식으로 LZMA2를 사용하지만 다음과 같은 다른 압축 방식도 지원합니다.

|방법|설명|
---|---|
|LZMA |LZ77 알고리즘 최적화 버전|
|LZMA2| 개선된 버전의 LZMA|
|수축| 일반 LZ77 알고리즘|
|BZip2| 표준 BWT 알고리즘|
|PPMD| 드미트리 슈카린의 PPMdH|

B6Zip 유틸리티는 이러한 모든 압축 표준을 지원하며 고도로 최적화되어 있어 고속입니다. [ZIP](/ko/compression/zip/), [TAR](/ko/compression/tar/) 및 [RAR](/ko/compression/rar/) 파일 형식 작업을 지원합니다. B6Z 파일에는 MIME 유형 application/x-b6z-compressed가 있습니다.

## 참고문헌

* [B6Zip](http://b6zip.com)

