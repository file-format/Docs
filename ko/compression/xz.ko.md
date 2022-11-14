{
  "date" : "2022-01-23",
  "keywords" :[ "xz 파일", "파일 형식", "xz 파일이란", "파일", "xz 예제", "xz 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ 파일 - XZ 압축 아카이브",
  "description":"XZ 파일 형식과 XZ 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## .XZ 파일이란?

XZ는 LZMA2 압축 알고리즘을 사용하는 압축 파일 형식입니다. 널리 사용되는 gzip 및 bzip2 형식을 대체하도록 설계되었으며 이러한 이전 표준에 비해 많은 이점을 제공합니다. XZ 파일은 많은 플랫폼에서 잘 지원되며 빠르고 쉽게 압축을 풀 수 있습니다. [ZIP](/ko/compression/zip/) 또는 [RAR](/ko/compression/rar/) 파일만큼 일반적이지는 않지만 XZ 아카이브는 압축 품질을 희생하지 않고 대용량 데이터를 저장하는 데 사용할 수 있습니다. 대용량 파일을 압축하거나 압축 해제해야 하는 경우 XZ 파일 확장자를 고려해 볼 가치가 있습니다.

## XZ 파일 형식

XZ 파일이 생성되어 디스크에 바이너리 파일로 저장됩니다. LZMA 알고리즘을 사용하여 데이터를 압축하며 최대 50%의 압축률을 달성할 수 있습니다. XZ 파일은 일반적으로 소프트웨어 배포 및 백업 아카이브에 사용됩니다. 대부분의 Linux 배포판에 포함된 XZ 유틸리티를 사용하여 압축을 풀 수 있습니다.

## Linux/Unix에서 XZ 파일 압축 풀기

XZ 파일의 압축을 풀려면 먼저 `xz-utils` 패키지를 설치하세요.
```
$ sudo apt-get install xz-utils
```

`unxz` 명령을 사용하여 .xz 파일을 추출합니다.
```
$ unxz compressed_xz_file.xz
```

또는 XZ의 --decompress 옵션과 함께 사용:
```
$ xz --decompress compressed_xz_file.xz
```

## 참고문헌

* [XZ 유틸리티](https://en.wikipedia.org/wiki/XZ_Utils)

