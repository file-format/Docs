{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "파일", "확장자", "파일 형식", "Excel Open XML 매크로", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLTM 파일과 이를 생성하고 열 수 있는 API가 무엇인지 알기 위한 파일 형식 가이드",
  "title" :"XLTM 파일이란?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLTM 파일이란?

XLTM 파일 확장자는 Microsoft Excel에서 매크로 사용 템플릿 파일로 생성된 파일을 나타냅니다. XLTM 파일은 구조가 [XLTX](/ko/spreadsheet/xltx/)와 비슷하지만 나중에 매크로를 사용하여 템플릿 파일 생성을 지원하지 않습니다. 이러한 템플릿 파일은 유사한 XLSX 파일을 쉽게 생성할 수 있도록 매크로와 함께 레이아웃, 서식 및 기타 설정을 생성하고 설정하는 데 사용됩니다.

## 간략한 역사 ##

Microsoft가 **Office Open XML** 표준을 수용하기 위해 변경하기로 결정한 것은 2000년 초였습니다. 이 새로운 표준에 따라 다양한 유형의 문서는 확장자에 "X"를 추가하여 식별했습니다. 여기서 "X"는 XML용입니다. 2007년에 이 새로운 파일 형식은 Office 2007의 일부가 되었으며 새 버전의 Microsoft Office에서도 계속 사용됩니다. 새 파일 형식은 파일 크기가 작고 손상이 적고 이미지 형식이 잘 표현된다는 장점이 추가되었습니다.

## XLTM 파일 형식 사양 ##

XLTM 파일은 Office OpenXML 파일 형식을 기반으로 하며 XML 및 [ZIP](/ko/Compression/ZIP/)를 사용하여 파일 크기를 줄입니다. 파일을 두 번 클릭하여 Microsoft Excel로 열 수 있습니다. XLTM 파일 형식의 파일 구성은 파일 이름을 ZIP으로 바꾼 다음 디스크에 내용을 추출하여 관찰할 수 있습니다.

### [콘텐츠 유형].xml ###

이것은 zip 압축을 풀 때 기본 수준에서 발견되는 유일한 파일입니다. 패키지 내 부품의 콘텐츠 유형을 나열합니다. 패키지에 포함된 XML 파일에 대한 모든 참조는 이 XML 파일에서 참조됩니다.

### \\rels(폴더) ###

패키지 수준 관계를 저장하는 단일 XML 파일이 포함된 관계 폴더입니다. Xltx 파일의 주요 부분에 대한 링크는 이 파일에 URI로 포함됩니다. 이러한 URI는 패키지에 대한 각 핵심 부분의 관계 유형을 식별합니다. 여기에는 xl/workbook.xml에 있는 기본 사무실 문서와 핵심 adn 확장 속성으로 docProps 내의 다른 부분과의 관계가 포함됩니다.

### docProps ###

이 폴더에는 전체 문서 속성이 들어 있습니다. 여기에는 핵심 속성 집합, 확장 또는 응용 프로그램별 속성 집합 및 문서의 축소판 미리 보기가 포함됩니다. 빈 통합 문서에는 이 폴더에 app.xml 및 core.xml이라는 두 개의 파일이 있습니다. core.xml에는 작성자, 생성 및 저장 날짜, 수정된 날짜와 같은 정보가 포함되어 있습니다. App.xml에는 파일 내용에 대한 정보가 포함되어 있습니다.

### xl(폴더) ###

통합 문서 내용에 대한 모든 세부 정보가 포함된 기본 폴더입니다. 기본적으로 다음 폴더가 있습니다.

* \_rels
* 주제
* 워크시트

다음 xml 파일:

* 스타일.xml
* 워크북.xml

## 참조 ##

* [MS-XLSX 파일 형식](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [오픈오피스 XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

