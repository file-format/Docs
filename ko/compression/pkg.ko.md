{
  "date" : "2021-04-08",
  "keywords" :[ "pkg 파일", "pkg 파일 형식", "pkg 파일이란", "파일", "pkg 예제", "pkg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - 확장 가능한 아카이브 파일 형식",
  "description":"PKG 파일 형식과 PKG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## .PKG 파일이란?

확장자가 .pkg인 파일은 macOS에 소프트웨어를 설치하는 데 사용되는 설치 프로그램 패키지 파일입니다. Macintosh 컴퓨터 외에도 iPhone에서도 사용됩니다. 내장된 Apple 설치 프로그램을 사용하여 PKG 파일의 내용을 설치할 수 있습니다. PKG 파일은 소프트웨어 설치를 위해 Windows 운영 체제에서 사용되는 MSI 파일과 유사합니다. 설치하는 동안 이러한 패키지 파일은 이 패키지에 의해 설치되는 추가 항목에 대한 아이디어를 제공하는 메시지를 기록할 수 있습니다.

## PKG 파일 형식

PKR은 전체 파일 크기를 줄이기 위해 압축된 이진 파일입니다. OSX 10.5부터 단일 설치 프로그램 파일이 포함된 플랫 패키지가 Apple에서 도입되었습니다. 이는 단일 파일이 아닌 번들로 제공되는 이전 패키징 형식과 다릅니다. 이러한 번들 패키지에는 일부 색인 파일을 통한 검색을 용이하게 하는 방식으로 파일을 저장하는 구조화된 디렉토리 계층 구조가 포함되어 있습니다. 플랫 PKG 파일 형식은 실제로 다음을 포함하는 [XAR](/ko/compression/xar/) 아카이브입니다.

* 헤더 - 크기, 체크섬 및 버전 정보를 정의합니다.
* 목차 - XML 문서는 UTF-8로 인코딩되어야 하며 파일의 시작 부분에 저장되므로 아카이브를 쉽게 스캔하여 개별 파일을 추출할 수 있습니다.
* 힙 - TOC에서 참조하는 구조화되지 않은 데이터 힙

## 참고문헌

* [플랫 패키지 파일 형식](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - 위키백과](https://en.wikipedia.org/wiki/.pkg)

