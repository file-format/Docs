{
  "date" : "2023-01-11",
  "keywords" :["ac 파일", "aci 파일이란 무엇인가", "파일", "ac 파일 여는 방법", "ac 파일 확장자","확장자"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDB 파일을 만들고 열 수 있는 AC 파일 형식 및 API에 대해 알아봅니다.",
  "title" :"AC 파일 형식 - Autoconf 스크립트 파일",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## .AC 파일이란?

AC 파일은 Autoconf 스크립트 파일입니다. **Autoconf**는 소프트웨어 소스 코드 패키지를 자동으로 구성하는 셸 스크립트를 생성하는 확장 가능한 M4 매크로 패키지입니다. 이러한 스크립트는 수동 사용자 개입 없이 여러 종류의 UNIX 유사 시스템에 패키지를 적용할 수 있습니다. Autoconf는 패키지가 사용할 수 있는 운영 체제 기능을 나열하는 템플릿 파일에서 패키지에 대한 구성 스크립트를 M4 매크로 호출 형식으로 만듭니다.

Autoconf를 사용하여 구성 스크립트를 생성하려면 GNU M4가 필요합니다. Autoconf를 구성하기 전에 GNU M4(최소 버전 1.4.6, 1.4.13 이상이 권장됨)를 설치해야 Autoconf의 구성 스크립트에서 찾을 수 있습니다. Autoconf에 의해 생성된 구성 스크립트는 독립적이므로 사용자는 Autoconf(또는 GNU M4)를 가질 필요가 없습니다.

## AC 파일을 여는 방법?

AC는 자동 구성을 의미합니다. 패키지의 필수 기능을 테스트하여 소프트웨어 소스 코드를 다양한 Posix와 같은 시스템에 적용할 수 있도록 하는 GNU Autoconf에서 생성한 스크립트입니다. 스크립트를 AC 파일이라고 합니다.

## 주요 Autotools 구성 요소

GNU autotools(`automake`, `autoconf` 등)에 대한 이해는 ebuild로 작업할 때 유용할 수 있습니다.

Autotools는 함께 사용하면 이식 가능한 소프트웨어를 만드는 것과 관련된 많은 어려움을 제거하는 관련 패키지 모음입니다. 이러한 도구는 상대적으로 간단한 몇 가지 업스트림 제공 입력 파일과 함께 패키지의 빌드 시스템을 만드는 데 사용됩니다.

**주요 autotools 구성 요소가 어떻게 결합되는지에 대한 기본 개요입니다.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

간단한 설정:

- `autoconf` 프로그램은 `configure.in` 또는 `configure.ac`에서 구성 스크립트를 생성합니다.
- `automake` 프로그램은 Makefile.am에서 Makefile.in을 생성합니다.
- Makefile.in 파일에서 하나 이상의 Makefile 파일을 생성하기 위해 `configure` 스크립트가 실행됩니다.
- `make` 프로그램은 Makefile을 사용하여 프로그램을 컴파일합니다.

## 참조
* [Autoconf 소프트웨어](https://www.gnu.org/software/autoconf/)
* [Autotools의 기초](https://devmanual.gentoo.org/general-concepts/autotools/index.html)


