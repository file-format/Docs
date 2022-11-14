{
  "date" : "2021-04-08",
  "keywords" :[ "lz 파일", "lz 파일 형식", "lz 파일이란", "파일", "lz 예제", "lz 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip 압축 파일 형식",
  "description":"LZ 파일 형식과 LZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## .LZ 파일이란?

확장자가 .lz인 파일은 압축을 위한 무료 명령줄 도구인 Lzip으로 만든 압축 아카이브 파일입니다. 지원 파일을 압축하는 연결을 지원합니다. LZ 파일은 미디어 유형이 application/lzip이며 [BZ2](/ko/compression/bz2)보다 높은 압축률을 지원합니다. LZ는 LZMA(Lempel-Ziv-Markov chain) 알고리즘을 기반으로 하며 파일의 무결성을 검사하기 위한 32비트 CRC 체크섬 및 ident 바이트를 포함합니다.

## LZMA 압축 형식

LZMA 압축 형식은 적응형 이진 범위 코더를 사용하여 인코딩된 압축된 비트 스트림으로 구성됩니다. 스트림은 패킷으로 나뉩니다. 각 패킷은 단일 바이트 또는 LZ77 시퀀스를 설명합니다. 각 패킷의 길이와 거리는 암시적 또는 명시적으로 인코딩됩니다.

7가지 종류의 패킷은 다음과 같다([위키피디아](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|팩 코드(비트 시퀀스) |패킷 이름 |패킷 설명|
---|---|---|
|0 + 바이트코드| 켜짐| 적응형 이진 범위 코더를 사용하여 인코딩된 단일 바이트입니다.|
|1+0 + len + dist| 매치| 시퀀스 길이와 거리를 설명하는 일반적인 LZ77 시퀀스입니다.|
|1+1+0+0| 단축| 1바이트 LZ77 시퀀스입니다. 거리는 마지막으로 사용한 LZ77 거리와 같습니다.|
|1+1+0+1 + 렌| 롱렙[0]| LZ77 시퀀스. 거리는 마지막으로 사용한 LZ77 거리와 같습니다.|
|1+1+1+0 + len| 롱렙[1]| LZ77 시퀀스. 거리는 두 번째로 마지막으로 사용한 LZ77 거리와 같습니다.|
|1+1+1+1+0 + len| 롱렙[2]| LZ77 시퀀스. 거리는 세 번째로 마지막으로 사용한 LZ77 거리와 같습니다.|
|1+1+1+1+1 + 렌즈| 롱렙[3]| LZ77 시퀀스. 거리는 네 번째로 마지막으로 사용한 LZ77 거리와 같습니다.|


## 참고문헌

* [LZMA - 위키백과](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

