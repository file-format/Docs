{
  "date" : "2019-10-11",
  "keywords" :[ "odp 파일", "odp 파일 형식", "odp 파일이란", "파일", "odp 예", "odp 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - 오픈오피스 프레젠테이션 파일 형식",
  "description":"ODP 파일 형식과 ODP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .ODP 파일이란?

확장자가 .odp인 파일은 OASISOpen 표준에서 OpenOffice.org에서 사용하는 프레젠테이션 파일 형식을 나타냅니다. 프레젠테이션 파일은 각 슬라이드가 텍스트, 이미지, 서식, 애니메이션 및 기타 미디어로 구성될 수 있는 슬라이드 모음입니다. 이 슬라이드는 사용자 지정 프레젠테이션 설정이 포함된 슬라이드쇼 형태로 청중에게 제공됩니다. ODP 파일은 OpenDocument 형식을 준수하는 응용 프로그램(예: OpenOffice 또는 StarSuite)에서 열 수 있습니다.

## 약력

ODP 파일 형식 사양은 ODF 사양으로 개발된 표준을 기반으로 합니다. 이러한 사양은 OASIS에서 다음과 같이 개발 및 게시한 세 가지 버전의 형태로 과거에 발전했습니다.

`2005` - 버전 1.0은 2005년 5월에 게시되었습니다.
`2007` - 버전 1.1은 2007년 2월에 게시되었습니다.
`2011' - 버전 1.2는 2011년 9월에 게시되었습니다.

ODF 1.0에서 1.1 버전으로의 전환에는 약간의 변경이 있었습니다. [ODF 1.2 버전](https://www.oasis-open.org/standards#opendocumentv1.2)은 ODF 사양의 최신 버전으로, ODS 읽기/쓰기 관련 애플리케이션 개발은 개발자들과 협의해야 한다.

## 파일 형식 사양

OpenDocument 형식은 [ZIP](https://docs.fileformat.com/compression/zip/) 아카이브로 패키지 내 여러 하위 문서 모음뿐만 아니라 단일 XML 문서로 문서 표현을 지원합니다. ZIP 아카이브의 각 파일은 전체 문서의 일부를 저장합니다. 각 하위 문서는 문서의 특정 측면을 저장합니다. 예를 들어, 한 하위 문서에는 스타일 정보가 포함되어 있고 다른 하위 문서에는 문서 내용이 포함되어 있습니다. 일반적인 ODF 문서에는 다음 구성 요소가 있습니다.

* `content.xml` – 문서 콘텐츠 및 콘텐츠에 사용되는 자동 스타일.
* `styles.xml` – 문서 내용에 사용되는 스타일 및 스타일 자체에 사용되는 자동 스타일.
* `meta.xml` – 작성자 또는 마지막 저장 작업 시간과 같은 문서 메타 정보입니다.
* `settings.xml` – 창 크기 또는 프린터 정보와 같은 응용 프로그램별 설정입니다.

이 외에도 패키지에는 문서 축소판, 이미지 등과 같은 다른 많은 하위 문서가 있을 수 있습니다.

스프레드시트 문서 파일은 콘텐츠(시트)가 content.xml 하위 문서에 저장되는 ODF 파일의 하위 집합입니다.

## 참고문헌

* [OpenDocument - 위키피디아 작성](https://en.wikipedia.org/wiki/OpenDocument)

