{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl 파일", "xbrl 파일 형식", "xbrl 파일 형식", "파일", "유형", "xbrl 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - 비즈니스 및 재무 보고 파일 형식",
  "description":"XBRL 파일 형식과 XBRL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## .XBRL 파일이란?

확장자가 .xbrl(eXtensible Business Reporting Language)인 파일은 비즈니스 정보를 교환하기 위해 무료로 사용할 수 있는 글로벌 프레임워크입니다. 이제는 더 유용하고 정확한 디지털 기록으로 오래된 종이 기반 보고서를 대체하는 표준 형식 중 하나로 널리 사용됩니다. XBRL 파일을 사용하여 교환되는 데이터에는 원장, 재무 세부 정보 및 대차 대조표가 포함됩니다. 각종 비즈니스 정보의 준비부터 분석 단계까지 데이터 처리가 가능한 데이터 태그를 지원합니다. XBRL 파일은 Rivet Software Dragon View XBRL Viewer와 같은 소프트웨어와 [Aspose.Finance](https://products.aspose.com/finance/)와 같은 API를 사용하여 열 수 있습니다.

## XBRL 파일 형식

XBRL은 전 세계적으로 널리 사용되는 디지털 비즈니스 보고를 위한 개방형 국제 표준입니다. 태그라고 하는 XBRL 요소를 사용하여 비즈니스 데이터의 각 항목을 설명하여 보고서 정렬 및 분석을 위한 데이터를 공식화하는 [XML](/ko/web/xml/) 기반 언어입니다. XBRL 파일 형식 사양은 현재 [XBRL 버전 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html)과 함께 XBRL International, Inc에서 개발 및 게시합니다. 사용자가 사용할 수 있습니다.

### XBRL 문서 구조

[XBRL 2.1 태그]에 대한 전체 정보(https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) 이 파일 형식을 작업하기 위한 응용 프로그램을 작성하기 위해 프로그래머가 참조할 수 있습니다. XBRL은 XBRL 인스턴스와 분류 모음으로 구성됩니다.

**`XBRL 인스턴스`** - XBRL 인스턴스는<xbrl> 루트 요소. 큰 XML 문서에는 하나 이상의 XBRL 인스턴스가 포함될 수 있습니다.

**`XBRL 분류법`** - [XBRL 분류법](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31) +corrected-errata-2013-02-20.html#_5)는 XML 스키마 구조 및 직접 참조되는 외부 링크 요소 집합으로 정의됩니다. 링크베이스 참조를 보여주는 확장 가능한 분류 스키마는 다음과 같습니다.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## 참조 ##

* [XBRL - 위키피디아 작성](https://en.wikipedia.org/wiki/XBRL)
* [XBRL(Extensible Business Reporting Language) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

