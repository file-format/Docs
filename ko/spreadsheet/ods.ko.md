{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "파일", "확장자", "파일 형식", "OpenDocument 스프레드시트"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ODS 파일과 이를 생성하고 열 수 있는 API가 무엇인지 알기 위한 파일 형식 가이드",
  "title" :"ODS 파일이란? ",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .ODS 파일이란?

확장자가 .ods인 파일은 사용자가 편집할 수 있는 OpenDocument 스프레드시트 문서 형식을 나타냅니다. 데이터는 ODF 파일 내부에 행과 열로 저장됩니다. XML 기반 형식이며 ODF(Open Document Formats) 제품군의 여러 하위 유형 중 하나입니다. 형식은 OASIS에서 게시 및 유지 관리하는 ODF 1.2 사양의 일부로 지정됩니다. Windows 및 기타 운영 체제의 여러 응용 프로그램에서 Microsoft Excel, NeoOffice 및 LibreOffice를 포함하여 편집 및 조작을 위해 ODS 파일을 열 수 있습니다. ODS 파일은 다른 응용 프로그램에서 [XLS](/ko/spreadsheet/xls/), [XLSX](/ko/spreadsheet/xlsx/) 및 기타와 같은 다른 스프레드시트 형식으로 변환할 수도 있습니다.

## 간략한 역사 ##

ODS 파일 형식 사양은 ODF 사양으로 개발된 표준을 기반으로 합니다. 이러한 사양은 OASIS에서 다음과 같이 개발 및 게시한 세 가지 버전의 형태로 과거에 발전했습니다.

`2005년` - 버전 1.0은 2005년 5월에 게시되었습니다.

`2007` - 버전 1.1은 2007년 2월에 게시되었습니다.

`2011' - 버전 1.2는 2011년 9월에 게시되었습니다.

ODF 1.0에서 1.1 버전으로의 전환에는 약간의 변경이 있었습니다. [ODF 1.2 버전](https://www.oasis-open.org/standards#opendocumentv1.2)은 ODF 사양의 최신 버전으로, ODS 읽기/쓰기 관련 애플리케이션 개발은 개발자들과 협의해야 한다.

## ODS 파일 형식 ##

OpenDocument 형식은 [ZIP](/ko/compression/zip/) 아카이브로 패키지 내의 여러 하위 문서 모음뿐만 아니라 단일 XML 문서로 문서 표현을 지원합니다. ZIP 아카이브의 각 파일은 전체 문서의 일부를 저장합니다. 각 하위 문서는 문서의 특정 측면을 저장합니다. 예를 들어, 한 하위 문서에는 스타일 정보가 있고 다른 하위 문서에는 문서의 내용이 들어 있습니다. 일반적인 ODF 문서에는 다음 구성 요소가 있습니다.

* `content.xml` – 문서 콘텐츠 및 콘텐츠에 사용된 자동 스타일.
* `styles.xml` – 문서 내용에 사용되는 스타일 및 스타일 자체에 사용되는 자동 스타일.
* `meta.xml` – 작성자 또는 마지막 저장 작업 시간과 같은 문서 메타 정보입니다.
* `settings.xml` – 창 크기 또는 프린터 정보와 같은 응용 프로그램별 설정입니다.

이 외에도 패키지에는 문서 축소판, 이미지 등과 같은 다른 많은 하위 문서가 있을 수 있습니다.

스프레드시트 문서 파일은 콘텐츠(시트)가 content.xml 하위 문서에 저장되는 ODF 파일의 하위 집합입니다.

## 참조 ##

* [OpenDocument - 위키피디아 작성](https://en.wikipedia.org/wiki/OpenDocument)

