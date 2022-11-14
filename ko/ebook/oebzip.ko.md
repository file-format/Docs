{
  "date" : "2021-03-23",
  "keywords" :[ "OEBZIP", "전자책 출판 구조 열기", "확장", "형식", "전자책", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"OEBZIP 파일을 만들고 열 수 있는 OEBZIP 파일 형식과 API에 대해 알아보세요.",
  "title" :"OEBZIP - 압축 공개 전자책 출판 구조",
  "linktitle" : "OEBZIP",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .OEBZIP 파일이란? ##

OEBZIP 파일은 국제 디지털 출판 포럼(**IDPF**)에서 소개되었습니다. 마찬가지로 [OEB](/ko/ebook/oeb/), 이러한 파일은 전자 책의 구조, 내용 및 표시에 대한 XML 기반 사양이지만 압축 또는 zip 형식입니다.

## OEBZIP 파일 형식의 기술적 세부 사항 ##

OEBZIP은 무엇보다도 마크업 어휘(현재는 XHTML 1.1의 기본 하위 집합)의 개선 및 광범위하게 확장된 CSS 지원을 포함하여 렌더링 제어 영역에서 더 많은 새로운 기능을 제공했습니다. 지속 가능성 요소는 이전 버전에서 변경되지 않았습니다.

OEBZIP 파일 형식은 다른 모든 구성 요소 파일을 나열하는 매니페스트를 포함하는 필수 패키지 파일과 논리적 읽기 순서를 나타내는 스파인을 포함하는 파일 집합으로 구성됩니다. 또한 [XML](/ko/web/xml/)의 텍스트를 보려면 OEBZIP 파일용 리더기가 [JPEG](/ko/image/jpeg/) 및 [PNG](/ko/image/png/) 형식의 이미지를 렌더링할 수 있어야 합니다. . 다른 형식의 콘텐츠 구성 요소가 통합될 수 있지만 대체 콘텐츠는 기본 OEB 형식 중 하나로 제공되어야 합니다.
  

파일의 OEBZIP 번들은 주로 중간 상태 형식으로 사용되었으며, 최종 사용자에 대한 출판은 다양한 eBook 뷰어에 적합한 형식으로 eBook을 제공한 출판사 또는 수집자를 통해 관리되었습니다. 후속 버전인 [EPUB](/ko/ebook/epub/)는 최종 사용자에게 최종 사용자에게 도달할 가능성이 높을 뿐만 아니라 중간 형식으로도 사용할 수 있습니다.

## 참고문헌

* [OEBPS(Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [전자책 열기](https://en.wikipedia.org/wiki/Open_eBook)


