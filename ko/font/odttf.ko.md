{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODTTF 파일 - 난독 처리된 OpenType 글꼴 파일 형식",
  "description":"ODTTF 파일을 만들고 열 수 있는 ODTTF 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## .ODTTF 파일이란?

ODTTF 파일은 [.XPS](/ko/page-description-language/xps/) 및 Microsoft Office 2007 파일 형식에서 사용하는 글꼴 파일 형식입니다. 글꼴의 디자인 정보를 추출하거나 글꼴의 소스 코드를 리버스 엔지니어링하기 어렵게 수정한 난독화된 OpenType 글꼴이 포함되어 있습니다. ODTTF는 원본 문서에 사용된 글꼴을 기반으로 하지만 일반 형식이 아니며 글꼴 데이터를 추출하기 위해 타사 소프트웨어에서 읽을 수 없습니다.

Pagemark XpsViewer, Pagemark XpsPlugin이 있는 Apple Safari, Pagemark XpsPlugin이 있는 Mozilla Firefox를 사용하여 ODTTF 파일을 열 수 있습니다.
NiXPS 보기 및 NiXPS 편집.

## ODTTF 파일 형식

ODTTF 파일 형식의 내부 파일 형식 구조는 임베디드 난독화 형식으로 저장되므로 알 수 없습니다. 이들은 .PDF 또는 .DOCX와 같은 디지털 문서에 포함될 수 있습니다.

## 참조
* [Microsoft의 OpenType 글꼴 사양](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [트루타입 개요](https://learn.microsoft.com/en-us/typography/truetype/)

