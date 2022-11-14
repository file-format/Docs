{
  "date" : "2019-10-11",
  "keywords" :[ "bz2 파일", "bz2 파일 형식", "bz2 파일이란", "파일", "bz2 예제", "bz2 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - 압축 파일 형식",
  "description":"BZ2 파일이 무엇인지, BZ2 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## .BZ2 파일이란?

BZ2는 주로 UNIX나 Linux 시스템에서 [BZIP2](http://www.bzip.org/) 오픈 소스 압축 방식을 사용하여 생성된 압축 파일입니다. 단일 파일의 압축에 사용되며 여러 파일의 아카이브를 의미하지 않습니다. 이는 여러 파일을 압축 없이 단일 파일로 아카이브하는 동일한 플랫폼의 TAR 파일 형식과 대조됩니다. BZ2로 압축된 파일은 [WinZip](https://www.winzip.com/win/en/)와 같은 응용 프로그램으로 압축을 풀 수 있습니다. BZIP2는 RLE(Run-Length Encoding) 또는 [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) 압축 알고리즘을 사용하여 높은 수준의 압축을 달성합니다.

## BZ2 파일 형식

이 파일 형식에 사용할 수 있는 공식 사양이 없습니다. 그러나 비공식 [역설계 사양](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)에 따르면 .bz2 스트림은 뒤에 오는 4바이트 헤더로 구성됩니다. 0개 이상의 압축 블록으로 바로 뒤에 처리된 일반 텍스트 전체 스트림에 대한 32비트 CRC를 포함하는 스트림 끝 마커가 옵니다. 압축된 블록 사이에는 패딩이 없으며 모든 블록은 비트 정렬됩니다.

## BZ2 파일 압축 풀기/추출

WinZip과 같은 소프트웨어를 사용하여 Windows 및 Mac OS에서 BZ2 파일의 압축을 풀 수 있습니다. Linux의 경우 터미널에서 다음 명령을 실행합니다.

```
bzip2 -d filename.bz2
```

## 참고문헌

* [BZIP2 형식 사양](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

