{
  "date" : "2019-10-11",
  "keywords" :[ "fodg 파일", "fodg 파일 형식", "fodg 파일이란", "파일", "fodg 예제", "fodg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument 도면 파일 형식",
  "description":"FODG 파일을 만들고 열 수 있는 FODG 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .FODG 파일이란?

.fodg 확장자를 가진 파일은 도면 요소를 저장하기 위한 Apache OpenOffice 도면 파일 형식입니다. OASIS(구조 정보 표준의 발전)에서 설명한 파일 형식 사양을 기반으로 합니다. OpenOffice 그래픽의 또 다른 유사한 파일 형식은 그리기 요소를 벡터 이미지로 저장하는 [ODG](/ko/image/odg/)입니다. FODG 파일은 OpenOffice 및 LibreOffice에서 열 수 있습니다. 예를 들어 OpenOffice에서 지원하는 다른 파일 형식에는 [ODT](/ko/word-processing/odt/), ODF, [ODP](/ko/presentation/odp/) 및 [ODS](/ko/spreadsheet/ods/)가 있습니다.

## FODG 파일 형식

FODG는 OASIS OpenDocument 형식 ISO/IEC 26300을 준수하는 OpenDocument의 XML 파일 형식을 기반으로 합니다. 인터넷 미디어 유형 application/vnd.oasis.opendocument.graphics가 있으며 org.oasis-open.opendocument public.composite-content도 준수합니다. . XML 구조는 스프레드시트, 도면 파일 및 텍스트 문서와 같은 모든 문서 유형에 공통입니다. OpenOffice 문서는 콘텐츠, 스타일, 메타데이터 및 응용 프로그램 설정을 4개의 개별 XML 파일로 분리하여 관심사 분리를 활용합니다.

`<office:document-content>` - 문서 내용과 내용에 사용된 자동 스타일.
`<office:document-styles>` - 문서 내용에 사용된 스타일과 스타일 자체에 사용되는 자동 스타일.
`<office:document-meta>` - 작성자 또는 마지막 저장 작업 시간과 같은 문서 메타 정보.
`<office:document-settings>` - 창 크기 또는 프린터 정보와 같은 응용 프로그램별 설정입니다.

## 참조 ##
* [v 1.3 표준화를 위한 향후 사양 ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [오아시스 사무용 오픈 문서 형식](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 형식 - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

