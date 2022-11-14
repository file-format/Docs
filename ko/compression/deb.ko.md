{
  "date" : "2021-04-08",
  "keywords" :[ "deb 파일", "deb 파일 형식", "deb 파일이란", "파일", "deb 예제", "deb 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip 압축 타르 아카이브",
  "description":"DEB 파일을 만들고 열 수 있는 DEB 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## .DEB 파일이란?

확장자가 .deb인 파일은 Linux OS에서 소프트웨어 패키지 배포에 사용할 수 있는 데비안 바이너리 패키지 파일 형식입니다. 두 개의 [TAR](/ko/compression/tar/) 아카이브 파일로 구성됩니다. DPKG는 DEB 패키지를 읽고 설치하는 메커니즘을 제공합니다. DEB 패키지는 APT 패키지 소프트웨어 관리 인터페이스를 사용하여 설치할 수 있습니다. DEB 파일의 인터넷 미디어 유형은 `application/vnd.debian.binary-package`입니다.

## DEB 파일 형식

DEB 파일은 두 개의 [TAR](/ko/compression/tar/) 아카이브 파일로 구성됩니다. 한 아카이브에는 제어 정보가 있고 다른 아카이브에는 설치 가능한 데이터가 들어 있습니다.

### 패키지 구성

DEB 파일은 `!<arch> `. Debian 0.93부터 DEB 파일의 보관 메커니즘에는 특정 순서로 세 개의 파일이 포함되어 있습니다.

1. `Debian Binary` - 줄 바꿈으로 구분된 일련의 줄을 갖게 됩니다. 현재 버전 번호를 설명하는 한 줄만 있습니다. 현재 버전 번호는 2.0입니다.
1. `Control Archive` - 패키지 이름, 버전, 종속성 및 유지 관리자와 같은 패키지에 대한 메타 정보와 유지 관리자 스크립트가 있는 control.tar 보관 파일을 포함합니다.
1. `Data Archive` - data.tar라는 이름의 tar 아카이브이며 실제 설치 가능한 미디어 파일이 포함되어 있습니다. 아카이브는 gz, bz2, lzma 또는 xz로 압축할 수 있으며 이에 따라 데이터 아카이브의 파일 확장자가 변경됩니다.

### 제어 아카이브

제어 아카이브에는 다음과 같은 내용이 포함될 수 있습니다.

* `control` - 패키지에 대한 간략한 설명과 종속성과 같은 기타 정보가 포함되어 있습니다.
* `md5sums` - 손상되거나 불완전한 파일을 감지하기 위해 패키지에 있는 모든 파일의 MD5 체크섬을 포함합니다.
* `conffiles` - 구성 파일로 취급되어야 하는 패키지의 파일을 나열합니다. 지정하지 않는 한 업데이트 중에 구성 파일을 덮어쓰지 않습니다.
* `preinst`, postinst, prerm 및 postrm - 패키지를 설치하거나 제거하기 전이나 후에 실행되는 선택적 스크립트
* `config`는 debconf 구성 메커니즘을 지원하는 선택적 스크립트입니다.
* `shlibs` - 공유 라이브러리 종속성 목록입니다.

## 참고문헌

* [DEB - 위키백과](https://en.wikipedia.org/wiki/Deb_(file_format))
* [데비안 바이너리 패키지 형식](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

