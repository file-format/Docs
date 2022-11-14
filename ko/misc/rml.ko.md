{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir 보고서 템플릿 파일",
  "description":"RML 파일을 만들고 열 수 있는 RML 파일 및 API에 대해 알아보세요.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## .RML 파일이란?

RML 파일은 [Elixir Repertoire](https://elixirtech.com/repertoire-2/) 보고 엔진이 포함된 보고 템플릿 파일입니다. 템플릿 파일은 Elixir FileSystem에 연결된 데이터 소스로 보고서를 생성하는 데 사용됩니다. 데이터는 RML 템플릿 파일에서 읽고 채워지며 [PDF](/ko/pdf/), [RTF](/ko/word-processing/rtf/) 및 스프레드시트 [XLS]와 같은 다양한 파일 형식으로 내보낼 수 있습니다. (/ko/스프레드시트/xls/). Elixir Repertoire 보고 엔진은 다양한 JDBC 데이터 소스에 연결할 수 있습니다.

## RML 파일 형식

RML 파일 형식의 내부 파일 구조 세부 정보는 공개적으로 사용할 수 없습니다. 파일은 Elixir Repertoire 애플리케이션에 의해 내부적으로 생성 및 저장되어 연결된 데이터 소스에서 채워진 데이터로 보고서를 생성합니다. RML 템플릿 파일에는 데이터에서 생성될 최종 보고서의 전체 레이아웃 및 자리 표시자 정보가 포함됩니다.

## 템플릿 파일을 어떻게 RML합니까?

Elixir Repertoire에서 RML 템플릿을 생성하기 위해 다음 단계를 따를 수 있습니다.

1. JDBC 데이터 소스를 파일 시스템에 연결합니다.
1. 보고서 템플릿 마법사 시작
1. 소프트웨어를 사용하여 데이터 소스 .ds 파일 찾기
1. 내보내기 선택으로 표 형식의 보고서를 선택합니다.
1. 보고서 템플릿에 포함할 필드 선택
1. 마지막으로 Finish 버튼을 클릭하면 First report.rml이 리포지토리에 추가되고 Layout 탭이 표시되도록 열립니다.

## 참고문헌

* [엘릭서 레퍼토리](https://elixirtech.com/repertoire-2/)

