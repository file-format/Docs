{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ 파일 - Gzipped Tar 파일",
  "description":"TGZ 파일을 만들고 열 수 있는 TGZ 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## .TGZ 파일이란?

확장자가 .tgz인 파일은 Gnu Zip(gzip) 압축 소프트웨어를 사용하여 압축된 여러 파일과 폴더로 구성된 TAR 아카이브 파일입니다. [TAR](/ko/compression/tar/) 파일은 일반적으로 인터넷을 통한 백업 또는 배포를 위해 여러 파일을 단일 파일로 결합합니다. gzip 소프트웨어를 사용하여 압축한 후 TGZ 파일이 될 때까지 압축 해제 파일입니다. 압축 파일인 TGZ 파일은 디스크 공간을 덜 차지하며 이메일을 통해 인터넷을 통해 쉽게 전송할 수 있습니다. TGZ 파일을 열 수 있는 일부 응용 프로그램에는 WinZip, Apple Archive Utility, 7-Zip 및 WinRAR이 있습니다. TGZ 파일은 주로 UNIX 및 Linux 시스템에서 사용됩니다.

## TGZ 파일 형식

TGZ 파일은 [GZ](/ko/compression/gz/) 압축 알고리즘을 사용하여 압축된 바이너리 파일로 저장됩니다.

## Linux에서 .tgz 파일의 압축을 푸는 방법

Linux/Unix OS에서 다음 명령을 사용하여 명령줄에서 TGZ 파일의 압축을 풀 수 있습니다.

```
tar zxvf tgzCompressedFile.tgz
```

위의 명령은 압축된 TGZ 파일의 압축을 풀고 해당 파일의 TAR 아카이브를 디스크로 추출합니다.
## 참조 ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - 위키백과](https://en.wikipedia.org/wiki/Gzip)

