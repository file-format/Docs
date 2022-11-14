{
  "date" : "2019-10-11",
  "keywords" :[ "tbz 파일", "tbz 파일 형식", "tbz 파일이란", "파일", "tbz 예제", "tbz 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip 압축 타르 아카이브",
  "description":"TBZ 파일 형식과 TBZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## .TBZ 파일이란?

확장자가 .tbz인 파일은 콘텐츠 파일의 크기를 줄이기 위해 BZIP 압축을 사용하는 압축 아카이브입니다. TBZ 파일은 실제로 UNIX [TAR](/ko/compression/tar/) 아카이브 파일이며 BZIP으로 압축됩니다. 가장 최근의 두 번째 수준 압축은 BZIP을 대체한 [BZIP2](/ko/compression/bz2/)입니다. TBZ 파일 형식은 대용량 파일 전송에 적합합니다. TBZ 파일은 7-Zip, PeaZip 및 jZip과 같은 소프트웨어 응용 프로그램을 사용하여 열거나 추출할 수 있습니다. Linux 및 macOS 사용자는 터미널 창에서 BZIP2 명령을 사용하여 TBZ를 열 수도 있습니다.

## TBZ 파일 형식

TBZ 파일은 실제로 BZIP/[BZIP2](/ko/compression/bz2) 압축으로 생성된 압축 아카이브입니다. 이 파일 형식에 사용할 수 있는 공식 사양이 없습니다. 그러나 비공식 [역설계 사양](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)에 따르면 .bz2 스트림은 뒤에 오는 4바이트 헤더로 구성됩니다. 0개 이상의 압축 블록으로

## 참조 ##

* [BZIP2 형식 사양](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

