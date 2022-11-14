{
  "date" : "2021-04-08",
  "keywords" :[ "rpm 파일", "rpm 파일 형식", "rpm 파일이란", "파일", "rpm 예제", "rpm 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat 패키지 관리자 파일",
  "description":"RPM 파일 형식과 RPM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## .RPM 파일이란?

확장자가 .rpm인 파일은 Linux 시스템에 프로그램을 설치하기 위한 Red Hat Linux 운영 체제 패키지입니다. Red Hat 패키지 관리자는 RPM 파일 형식을 사용하며 무료 오픈 소스 패키지 관리 시스템입니다. RPM 파일을 그대로 프로그램 설치에 사용할 수 있지만 Alien이라는 데비안 프로그램을 사용하여 [DEB](/ko/compression/deb/)와 같은 다른 패키지 형식으로 변환할 수 있습니다.

## RPM 파일 형식

RPM 파일은 파일 세트를 포함할 수 있는 바이너리입니다. 대부분의 경우 RPM 파일은 소프트웨어의 컴파일된 실행 파일인 "바이너리 RPM"입니다. RPM 파일에는 소스 코드에서 패키지를 빌드하는 데 사용할 수 있는 소스 RPM(SRPM)이 포함될 수 있습니다. RPM 파일 형식은 4개의 섹션으로 구성됩니다.

* Lead - 파일을 RPM 파일로 식별합니다.
* 서명 - 무결성 및/또는 진정성을 보장하는 데 사용할 수 있습니다.
* 헤더 - 패키지 이름, 버전, 아키텍처, 파일 목록 등을 포함한 메타데이터를 포함합니다.
* 파일 아카이브 - 페이로드라고도 하며 일반적으로 [GZIP](/ko/compression/gz/)로 압축된 cpio 형식입니다.

## 참고문헌

* [RPM - 위키피디아](https://rpm.org)
* [RPM 문서](https://rpm.org/documentation.html)

