{
  "date" : "2021-03-23",
  "keywords" :[ "OEB", "전자책 출판 구조 열기", "확장", "형식", "전자책", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"OEB 파일 형식과 OEB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"OEB - 오픈 전자책 출판 구조",
  "linktitle" : "OEB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .OEB 파일이란?

OEB 파일은 국제 디지털 출판 포럼(**IDPF**)에서 소개되었습니다. 보다 공식적으로 OEB 파일은 **OEBPS**라고도 합니다. 이 파일은 전자 책의 구조, 내용 및 표시를 위한 XML 기반 사양입니다. 이 파일 형식은 [EPUB](/ko/ebook/epub/) 형식으로 대체되었습니다.

## OEB 파일 형식의 기술적 세부 사항

OEB 파일 형식은 다른 모든 구성 요소 파일을 나열하는 매니페스트를 포함하는 필수 패키지 파일과 논리적 읽기 순서를 나타내는 스파인을 포함하는 파일 집합으로 구성됩니다. 또한 [XML](/ko/web/xml/)의 텍스트를 보려면 OEB 파일용 리더기가 [JPEG](/ko/image/jpeg/) 및 [PNG](/ko/image/png/) 형식의 이미지를 렌더링할 수 있어야 합니다. . 다른 형식의 콘텐츠 구성 요소가 통합될 수 있지만 대체 콘텐츠는 기본 OEB 형식 중 하나로 제공되어야 합니다.

OEBPS 1.2는 이전 버전(OEBPS 1.0.1)에 대한 긴밀하게 결합된 업데이트였습니다. 이는 무엇보다도 마크업 어휘의 향상(현재 XHTML 1.1의 진정한 하위 집합)과 크게 확장된 CSS 지원을 포함하여 렌더링 제어 영역에서 현대적인 기능을 제공했습니다. 지속 가능성 요소는 이전 버전에서 변경되지 않았습니다.
  

파일의 OEB 번들은 주로 중간 상태 형식으로 사용되었으며, 최종 사용자에 대한 출판은 다양한 전자책 뷰어에 적합한 형식으로 전자책을 제공한 출판사 또는 수집자를 통해 관리되었습니다. 후속 버전인 [EPUB](/ko/ebook/epub)는 최종 사용자에게 최종 상태 형식으로 제공될 뿐만 아니라 중간 상태 형식으로 제공될 가능성이 더 큽니다.

## 참고문헌

* [OEBPS(Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [전자책 열기](https://en.wikipedia.org/wiki/Open_eBook)


