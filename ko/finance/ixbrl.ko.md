{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","ixbrl 파일", "ixbrl 파일 형식", "ixbrl 파일 형식", "파일", "유형", "ixbrl 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - 비즈니스 및 재무 보고 파일 형식",
  "description":"IXBRL 파일 형식 및 IXBRL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## .iXBRL 파일이란?

iXBRL(ilnine XBRL) 파일 형식을 사용하면 [XBRL](/ko/finance/xbrl/) 데이터를 HTML 파일에 포함하여 기계와 사람이 읽을 수 있습니다. 실제로 XBRL 태그를 사용하는 [xHTML](/ko/web/xhtml/) 파일이며 영국 HMRC의 요구 사항을 충족하기 위해 XBRL International에서 개발했습니다. iXBRL을 사용하면 원본 문서의 레이아웃을 그대로 유지하면서 재무제표를 생성할 수 있습니다. iXBRL 파일은 Windows 운영 체제의 메모장 및 MacOS의 TextEdit와 같은 모든 텍스트 편집기에서 열 수 있습니다.

## iXBRL 파일 형식

iXBRL 내부에서 XBRL의 내용은 XML 태그를 사용하는 xHTML 파일 형식으로 래핑됩니다. XBRL처럼,<xbrl> iXBRL 파일의 루트 요소입니다. XHTML 형식은 그 내용을 다양한 문서 유형 및 모듈의 모음으로 나타냅니다. XHTML의 모든 파일은 XML 파일 형식을 기반으로 하며 XML 문서 표준을 따릅니다. XHTML은 종속 [HTML](/ko/web/html/) 문서 개체 모델(DOM) 또는 [XML](/ko/web/xml/) 문서 개체 모델의 운영 활용을 위한 필수 사용 형식입니다. 외부 세계의 경우 iXBRL은 [xHTML](/ko/web/xhtml/) 파일 형식 사양을 따릅니다.

### iXBRL 대 XBRL

XBRL은 다음 요소에 따라 iXBRL과 비교할 수 있습니다.

* 복잡성
* 서식 옵션
* 파일 형식/확장자
* 렌더링 옵션
* 제출 절차

다음 표는 이러한 차이점을 보여줍니다.

|매개변수|XBRL|iXBRL|
---|---|---|
|복잡성|iXBRL보다 복잡함|기존의 XHTML 구성 방식으로 인해 덜 복잡함|
|포맷 옵션|제한된 유연성|콘텐츠 서식을 위한 높은 유연성|
|파일 형식/확장자|공식적으로 .xml 확장자로 저장됨|보통 .html 또는 .xhtml 확장자로 저장됨|
|렌더링 옵션|이것을 보려면 XBRL 뷰어가 필요합니다|브라우저에서 볼 수 있는 사람이 읽을 수 있는 콘텐츠|
|제출과정| XBRL(기계 판독 가능) 및 HTML(사람 판독 가능) 인스턴스 문서는 별도로 보관됩니다.|사람이 읽을 수 있는 형식과 기계가 읽을 수 있는 형식을 모두 단일 인스턴스 문서에서 사용할 수 있습니다.|

## 참고문헌

* [XBRL - 위키피디아 작성](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

