{
  "date" : "2021-04-08",
  "keywords" :[ "lzma 파일", "lzma 파일 형식", "lzma 파일이란", "파일", "lzma 예제", "lzma 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA 압축 파일 형식",
  "description":"LZMA 파일을 만들고 열 수 있는 LZMA 파일 및 API는 무엇입니까?",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## .LZMA 파일이란?

확장자가 .lzma인 파일은 LZMA(Lempel-Ziv-Markov chain Algorithm) 압축 방법을 사용하여 생성된 압축 아카이브 파일입니다. 이들은 주로 Unix 운영 체제에서 발견/사용되며 파일 크기를 최소화하기 위해 [ZIP](/ko/compression/zip/)와 같은 다른 압축 알고리즘과 유사합니다. LZMA는 레거시 파일 형식으로 .xz 형식으로 대체되거나 대체되었습니다. .lzma 형식의 MIME 유형은 \`application/x-lzma'입니다. 이 파일 형식은 LZMA SDK에서 사용하기 위해 Igor Pavlov가 설계했습니다.

## LZMA 파일 형식

LZMA 파일은 두 가지 주요 부분으로 구성됩니다.

1. 헤더
1. 압축 데이터


### LZMA 헤더

LZMA 파일에는 LZMA 압축 데이터가 뒤따르는 13바이트 헤더가 있습니다. LZMA 헤더는 다음으로 구성됩니다.

* 속성
* 사전 크기
* 압축되지 않은 크기

#### LZMA 헤더 속성

속성 필드에는 세 가지 속성이 있습니다. 약어는 괄호 안에 제공되며 그 뒤에 속성의 값 범위가 표시됩니다. 필드는 다음으로 구성됩니다.

1) 리터럴 컨텍스트 비트의 수(lc, [0, 8]);
2) 리터럴 위치 비트의 수(lp, [0, 4]); 그리고
3) 위치 비트 수(pb, [0, 4]).

#### LZMA 사전 크기

이것은 2^n 및 2^n + 2^(n-1) 범위의 값을 갖는 부호 없는 32비트 리틀 엔디안 정수로 저장됩니다. LZMA Utils는 사전 크기에 관계없이 파일의 압축을 풀 수 있습니다.

#### 압축되지 않은 크기
압축되지 않은 크기는 부호 없는 64비트 리틀 엔디안 정수로 저장됩니다. 0xFFFF_FFFF_FFFF_FFFF의 특수 값은 압축되지 않은 크기를 알 수 없음을 나타냅니다. Uncompressed Size를 알 수 없는 경우에만 값이 End of Payload Marker(\*)로 표시됩니다.

## 참고문헌
* [Lempel-Ziv-Markov 체인 알고리즘](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
