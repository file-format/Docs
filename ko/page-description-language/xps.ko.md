{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML 용지 사양", "파일", "확장자", "파일 형식", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - 페이지 레이아웃 파일 형식",
  "description":"XPS 파일을 만들고 열 수 있는 XPS 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## .XPS 파일이란? ##

XPS 파일은 Microsoft에서 만든 XML Paper Specification을 기반으로 하는 페이지 레이아웃 파일을 나타냅니다. EMF 파일 형식을 대체하기 위해 개발되었으며 [PDF](/ko/pdf/) 파일 형식과 유사하지만 문서의 레이아웃, 모양 및 인쇄 정보에 XML을 사용합니다. 사실 XPS는 PDF에 대한 시도이지만 여러 가지 이유로 PDF가 소유한 만큼의 인기를 얻지 못했다고 말하는 것이 더 타당합니다. Microsoft는 XPS 파일 생성을 위해 Windows 7부터 기본적으로 XPS Document Writer를 제공합니다. 문서를 인쇄하는 동안 "Microsoft XPS Document Writer"를 프린터로 선택하여 XPS 파일을 생성할 수 있습니다.

XPS 뷰어는 Windows Vista, Windows 7, Windows 8 및 Internet Explorer 6 이상의 일부로 통합되어 있습니다. XPS 파일은 생성되면 읽기 전용이 됩니다. 이것은 문서의 신뢰성을 위해 XPS로 전송된 수신 문서에 대한 사용자의 확신을 더합니다. XPS 문서에는 원본 문서에서 변환된 페이지가 하나 이상 포함될 수 있습니다.

## 간략한 역사 ##

Microsoft는 XPS 사양을 Ecma International에 제출했습니다. 2007년 6월 Ecma Technical Committee 46(TC46)은 OpenXPS Paper Specifications에 기반한 표준을 개발하기 위해 설립되었습니다. Ecma International은 2009년 6월 제97차 총회에서 Ecma 표준(ECMA-388)[XPS 사양](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)을 승인했습니다.

## XPS 파일 형식 ##

XPS 형식은 문서를 표시하거나 인쇄하기 위한 렌더링 규칙과 함께 문서의 구성과 각 페이지의 시각적 모양을 정의하는 XML 마크업으로 구성됩니다. 시스템에서 사용 가능한 리소스와 독립적으로 만드는 모든 시스템에서 문서를 재생성하기 위한 모든 정보를 보유합니다. 형식은 기본적으로 ZIP 아카이브이며 파일 확장자의 이름을 ZIP으로 바꾸면 문서 데이터가 포함된 구성 파일이 표시됩니다. 이러한 문서에는 다음이 포함됩니다.

* 문서 페이지 파일(.fpage) - 문서 내용 및 문서 형식 설정을 포함합니다. XPS 문서의 모든 페이지에는 하나의 FPAGE 파일이 있습니다.
* 문서 설정 파일(.fdoc) - XPS 아카이브에 포함된 설정을 저장합니다.
* 문서 조각 파일(.frag) - 실제 XPS 파일에 대한 설정을 정의하고 문서의 모든 페이지에는 고유한 .frag 파일이 있습니다.

{{< figure src="../XPS-1.png" alt="XPS 파일 형식" >}}

이러한 파일은 예를 들어 누군가 컴퓨터에 동일한 글꼴을 설치하지 않은 경우 XPS 뷰어에서 해당 원본 글꼴을 렌더링하는 방식으로 문서 내용을 유지합니다. 이것은 각각에 대한 XML 마크업 파일의 포함을 의미합니다:

* 페이지
* 텍스트
* 임베디드 글꼴
* 래스터 이미지
* 2D 벡터 그래픽
* 디지털 저작권 관리

XPS 문서 형식에는 문서의 특정 목적을 각각 충족하는 잘 정의된 부분 및 관계 세트가 포함되어 있습니다. 이 형식은 또한 디지털 서명, 축소판 및 인터리빙을 포함한 패키지 기능을 확장합니다.

일반적인 XPS 문서는 다음과 같으며 XPS 파일 형식사양에 비추어 분석할 수 있습니다.

{{< figure src="../XPS-2.png" alt="XPS 파일 형식" >}}


## 참조 ##

* [XPS 파일 형식 사양](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - 위키피디아 작성](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

