
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML 파일 - Microsoft 지원 마크업 언어 파일",
  "description":"AML 파일이 무엇이며 AML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft 지원 마크업 언어 파일

## .AML 파일이란?

AML(Assistance Markup Language) 파일은 MAML(Microsoft Assistance Markup Language)로 생성된 XML 파일입니다. Microsoft Windows OS에 대한 온라인 도움말을 제공하기 위해 Microsoft에서 개발했습니다. 이전에는 컴파일된 HTML [CHM](/ko/web/chm/) 파일 형식으로 Windows 도움말을 사용할 수 있었습니다. AML 파일은 애플리케이션이 소스 코드 및 지원 도움말 페이지를 생성할 수 있도록 하는 구조화된 문서를 제공합니다. 이를 통해 문서와 문서의 구성 요소를 컨텍스트별로 정의할 수 있습니다. AML 도움말 파일은 온라인으로 게시되며 온라인으로 제공되는 패키지 업데이트에서 업데이트되도록 구성할 수 있습니다.

## MAML 파일 구조

MAML을 사용하여 생성된 AML 파일은 [XML](/ko/web/xml/) 파일로 저장되어 다양한 활성 개념을 표현하는 데 사용할 수 있습니다. 또한 단계별 마법사를 사용하여 도움말 파일을 대화형으로 만드는 안내 도움말(액티브 콘텐츠 마법사)을 제공할 수 있습니다.

MAML을 사용하여 생성된 AML 파일은 다음과 같은 세그먼트로 나눌 수 있는 제작 구조를 따릅니다.

* 개념적
* 자주하는 질문
* 용어 사전
* 절차
* 참조
* 재사용 가능한 콘텐츠
* 일
* 문제 해결 및
* 튜토리얼

## MAML 파일을 만드는 방법은 무엇입니까?

다음 방법 중 하나를 사용하여 MAML 파일을 만들 수 있습니다.

* Sandcastle 사용 - 스키마 및 프로그램 실행 파일을 활용하여 도움말 파일을 생성합니다. 그러나 이 도구는 중단되었습니다.
* DocProject 사용 - 도움말 콘텐츠를 생성하기 위해 Microsoft Visual Studio 내에서 실행할 수 있는 Microsoft Visual Studio 플러그인.

MAML 파일은 .XSL 스키마 및 프로그램 실행 파일 모음인 Sandcastle을 사용하여 만들 수 있습니다. 또한 Microsoft Visual Studio 도움말 작성 도구 추가 기능인 DocProject를 사용하여 만들 수도 있습니다.

## 참고문헌

* [PlayyPS를 사용하여 XML 기반 도움말 만들기](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
* [Microsoft 지원 마크업 언어](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - 아크 매크로 언어 파일

## ARC 매크로 AML 파일이란?

AML(ARC 매크로 언어) 파일은 ArcInfo Workstation GIS 애플리케이션으로 생성된 스크립팅 파일입니다. 이것은 ArcInfo에서 GIS 애플리케이션을 생성하기 위한 독점적인 고급 알고리즘 언어인 ARC 매크로 언어로 작성되었습니다. AML은 1986년 ESRI에서 설계했으며 명령줄 ARCINFO GIS 시스템에서 응용 프로그램을 만드는 목적으로 사용되었습니다. 스크립팅 파일인 AML 파일에는 사용자 인터페이스 구성 요소 생성 및 지도 데이터 조작과 같은 여러 작업을 수행하는 스크립트 명령이 포함될 수 있습니다.

## AML 파일 형식 - 추가 정보

스크립트 파일인 AML은 정보를 일반 텍스트 파일로 디스크에 저장합니다. PRIMOS 운영 체제의 CPL 셸 언어를 기반으로 하는 AML 구문을 따릅니다. AML 언어는 ArcGIS 제품군의 일부인 ESRI의 지오프로세싱 프레임워크로 대체되었으며 ArcObjects를 사용하여 VBA 또는 Python을 통해 프로그래밍 지원을 제공합니다.

## 참고문헌

* [ARC 매크로 언어](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [스크립트 도구와 함께 AML 사용](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

