{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","xsd 파일이란","xsd 파일을 여는 방법", "확장자", "파일", "xsd 파일","xsd 파일 형식", ".xsd 확장자" ,"xsd 파일 예"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XSD 파일 형식과 XSD 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"XSD 파일 형식 - XML 스키마 정의 파일",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## XSD 스키마 파일이란?

XSD 파일은 XML 문서의 일부가 될 수 있는 요소와 속성을 지정하는 정의 파일입니다. 이렇게 하면 데이터가 올바르게 해석되고 오류가 포착되어 적절한 XML 유효성 검사가 수행됩니다. XSD 파일은 입력된 데이터가 파일에 정의된 것과 동일한 구조를 따르도록 합니다. XSD 파일은 [XML](/ko/web/xml/) 파일 형식으로 저장되며 Microsoft 메모장, 메모장++ 또는 [Microsoft XML 메모장](https://microsoft.github.io)과 같은 텍스트 편집기에서 열거나 편집할 수 있습니다. /Xml메모장/).

## XSD 파일 형식

XSD 파일은 사람이 읽을 수 있는 일반 텍스트 파일 형식으로 디스크에 저장됩니다. XSD는 인코딩될 실제 데이터와 관련하여 문서에서 사용할 수 있는 요소를 정의합니다.

## XSD 파일의 예

구매 주문 스키마가 있는 간단한 XSD 파일은 다음 [Microsoft XSD 예제](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file)와 같이 태그를 사용하여 요소를 정의합니다. -simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

여기에서는 다음 태그를 사용합니다.

* `xs:element` - 요소를 정의합니다.
* `xs:sequence` - 자식 요소가 언급된 순서대로만 나타남을 나타냅니다.
* `xs:complexType` - 다른 요소가 포함되어 있음을 나타냅니다.
* `xs:simpleType` - 다른 요소를 포함하지 않음을 나타냅니다.
* `유형` - 문자열, 십진수, 정수, 부울, 날짜, 시간,

## 참조 ##

- [마이크로소프트 XML 메모장](https://microsoft.github.io/XmlNotepad/)
- [XSD 샘플 예시](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

