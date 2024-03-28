{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "확장자", "파일", "형식", "시스템", "Windows 캐비닛 파일", "Microsoft", "설치 프로그램", "설정", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows 캐비닛 파일",
  "description":"CAB 파일을 만들고 열 수 있는 CAB 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .CAB 파일이란? ##

확장자가 .cab인 파일은 시스템 파일 범주에 속하는 Windows 캐비닛 파일에 속합니다. [LZX](/ko/compression/lzx/), Quantum, [ZIP](/ko/compression/zip/) 등 압축 데이터 알고리즘을 지원하는 Microsoft Windows 버전에서 아카이브 파일 형식으로 저장되는 파일입니다.  이 파일은 사용자 또는 개발자가 소프트웨어 설치 데이터 및 파일을 포함하고 공유하려고 할 때 매우 중요합니다. 이러한 파일에 포함된 무손실 데이터 압축 및 디지털 인증 기능으로 인해 이 파일은 이러한 파일을 저장하고 공유하는 데 적합합니다. Device Installer, SetUp API 및 AdvPak과 같은 다양한 Microsoft 설치 프로그램을 지원합니다.

## 간략한 역사 ##

CAB 파일은 Microsoft에서 개발한 데이터 압축 파일 형식입니다. 처음에는 "다이아몬드"라고 불렸지만 나중에 "캐비닛"이라는 단어의 줄임말인 CAB 파일로 널리 알려지게 되었습니다.

## 기술 사양 ##

CAB 파일에는 일반적으로 최대 65535개의 폴더가 포함될 수 있으며, 각 폴더에는 최대 65536개의 파일이 포함될 수 있습니다. CAB 파일 저장 메커니즘은 각 파일을 개별적으로 압축하여 저장하는 대신 각 폴더를 압축 블록으로 저장하므로 시간과 공간이 효율적입니다. 빈 폴더는 CAB 보관 폴더에 저장할 수 없습니다. CAB 파일은 Microsoft에 의해 처음 개발되었으며 약간 다른 형식의 InstallShield와 같은 다양한 설치 프로그램에서 사용됩니다. CAB 파일은 일반적으로 자동 압축 풀기 프로그램에 연결됩니다. Microsoft CAB 파일은 형식을 식별하는 데 도움이 되는 고유한 마커로 인해 쉽게 인식할 수 있습니다. 모든 Microsoft CAB 파일의 고유 마커는 4단어 접두어인 MSCF입니다. 이 코드를 보고 사용자는 Microsoft CAB 파일을 다른 파일과 쉽게 구별하고 그에 따라 압축기 또는 버전에서 사용할 수 있습니다. 더 많은 소프트웨어 설치 데이터로 파일을 압축하거나 올바른 소프트웨어를 사용하여 현재 데이터의 압축을 풀 수 있습니다.


## CAB 예 ##

다음 예는 CAB 파일 구조에서 파일과 폴더 간의 관계를 보여줍니다.

{{< figure src="../cab.png" alt="CAB 파일 형식" >}}

## 참조 ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
