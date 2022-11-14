{
  "date" : "2019-10-11",
  "keywords" :[ "odg 파일", "odg 파일 형식", "odg 파일이란", "파일", "odg 예", "odg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG 파일 형식",
  "description":"ODG 파일을 만들고 열 수 있는 ODG 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .ODG 파일이란?

ODG 파일 형식은 Apache OpenOffice의 그리기 응용 프로그램에서 그리기 요소를 벡터 이미지로 저장하는 데 사용됩니다. OASIS(구조 정보 표준의 발전)에서 설명하는 XML 기반 파일 형식 사양을 따릅니다. ODG는 점, 선 및 곡선을 사용하여 도면을 벡터 이미지로 나타냅니다. OpenOffice 외에도 LibreOffice 및 기타 응용 프로그램은 ODG 파일 형식 작업을 지원합니다. 예를 들어 OpenOffice에서 지원하는 다른 형식에는 [ODT](/ko/word-processing/odt/), ODF, [ODP](/ko/presentation/odp/) 및 [ODS](/ko/spreadsheet/ods/)가 있습니다.


## ODG 파일 형식 사양

ODG 파일 형식은 스키마가 잘 정의된 구조화된 XML 문서 형식인 OpenDocument 형식을 기반으로 합니다.
OpenDocument 형식의 각 구조 구성 요소는 연결된 속성이 있는 요소로 표시됩니다. XML 기반 구조는 텍스트 문서, 스프레드시트 또는 도면 파일과 같은 모든 문서 유형에 공통입니다. 문서에는 다양한 스타일이 포함될 수 있습니다. OpenDocument 파일 구조는 다음 요소로 구성됩니다.
* 문서 루트
* 문서 메타데이터
* 본문 요소 및 문서 유형
* 애플리케이션 설정
* 스크립트
* 폰트 페이스 선언
* 스타일
* 페이지 스타일 및 레이아웃

## 문서 루트 ##

문서 루트 요소는 전체 문서를 포함하며 OpenDocument 형식의 파일의 기본 요소입니다. 동일한 유형의 문서 루트 요소가 텍스트, 문서, 스프레드시트 및 도면 문서와 같은 모든 유형의 문서에 적용됩니다.

### 루트 요소 ###
단일 XML 문서는 자체 루트 요소로 표시됩니다. 지원되는 다섯 가지 루트 요소는 다음과 같습니다.

`<office:document> ` - singleXML 문서에서 완전한 사무용 문서.
`<office:document-content> ` - 문서 내용과 내용에 사용된 자동 스타일.
`<office:document-styles> ` - 문서 내용에 사용된 스타일과 스타일 자체에 사용되는 자동 스타일.
`<office:document-meta> ` - 작성자 또는 마지막 저장 작업 시간과 같은 문서 메타 정보.
`<office:document-settings> ` - 창 크기 또는 프린터 정보와 같은 응용 프로그램별 설정입니다.

### ODG 문서 메타데이터 ###
OpenDocument에는 \<office:meta> 요소. 문서에 대한 이 일반 정보는 문서 시작 부분에 포함되며 애플리케이션은 동일한 요소의 여러 인스턴스를 업데이트할 수 있습니다.

### 본문 요소 및 문서 유형 ###
문서 본문은 문서 유형 요소를 사용하여 문서에 포함된 콘텐츠의 유형을 나타냅니다. 이러한 문서 유형은 다음과 같습니다.
* 텍스트 문서
* 도면 문서
* 프레젠테이션 문서
* 스프레드시트 문서
* 차트 문서
* 이미지 문서

### 애플리케이션 설정 ###
Office 응용 프로그램에 대한 설정은 문서 구성 또는 문서의 시각적 모양과 관련된 다양한 설정을 나타냅니다. 각 카테고리는 `<config:config-item-set> `. 이러한 설정 범주의 예는 다음과 같습니다.
* 기본 프린터와 같은 문서 설정
* 확대/축소 수준과 같은 보기 설정

### 스크립트 ###
문서에는 여러 스크립트가 포함되어 있는 것이 일반적입니다. OpenDocument 파일의 각 스크립트는 `<office:script> ` 요소. 이러한 스크립트 요소는 단일 `<office:scripts> ` 요소. 문서가 로드되는 동안 스크립트는 문서를 업데이트하지 않습니다.
### 폰트 페이스 선언 ###

글꼴 선언에는 문서 작성자가 사용하는 글꼴에 대한 정보가 포함되어 있습니다. 이 정보는 다른 시스템에서 이러한 글꼴을 찾는 데 도움이 됩니다.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### 스타일 ###
다음 스타일은 OpenDocument 형식에서 지원됩니다.

'공통 스타일' - 이러한 스타일의 XML 표현을 스타일이라고 합니다.
'자동 스타일' - 문서의 사용자 인터페이스 보기에서 단락과 같은 개체에 할당되는 서식 속성을 포함합니다.
`Mater Styles` - 서식 정보 및 스타일이 적용될 때 문서 콘텐츠와 함께 표시되는 추가 콘텐츠가 포함된 공통 스타일입니다. 마스터 스타일의 예로는 마스터 페이지가 있습니다.

## 참조 ##
* [오아시스 사무용 오픈 문서 형식](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 형식 - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

