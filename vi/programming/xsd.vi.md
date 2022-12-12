{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","tệp xsd là gì","cách mở tệp xsd", "phần mở rộng", "tệp", "tệp xsd","định dạng tệp xsd", "phần mở rộng .xsd", "ví dụ về tệp xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Tìm hiểu về định dạng tệp XSD và các API có thể tạo và mở tệp XSD.",
  "title" :"Định dạng tệp XSD - Tệp định nghĩa lược đồ XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Tệp Lược đồ XSD là gì?

Tệp XSD là tệp định nghĩa chỉ định các phần tử và thuộc tính có thể là một phần của tài liệu XML. Điều này đảm bảo rằng dữ liệu được giải thích chính xác và các lỗi được phát hiện, dẫn đến xác thực XML phù hợp. Các tệp XSD đảm bảo rằng dữ liệu được nhập tuân theo cùng một cấu trúc như được xác định trong tệp. Các tệp XSD được lưu trữ ở định dạng tệp [XML](/vi/web/xml/) và có thể được mở hoặc chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào như Microsoft Notepad, Notepad++ hoặc [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Định dạng tệp XSD

Các tệp XSD được lưu vào đĩa ở định dạng tệp văn bản thuần túy mà con người có thể đọc được. XSD xác định các thành phần có thể được sử dụng trong tài liệu, liên quan đến dữ liệu thực mà nó sẽ được mã hóa.

## Ví dụ về tệp XSD

Một tệp XSD đơn giản có lược đồ đơn đặt hàng xác định các thành phần bằng cách sử dụng các thẻ như trong [ví dụ XSD của Microsoft] sau đây (https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

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

Ở đây, các thẻ sau được sử dụng.

* `xs:element` - Định nghĩa một phần tử.
* `xs:sequence` - Biểu thị các phần tử con chỉ xuất hiện theo thứ tự đã nêu.
* `xs:complexType` - Biểu thị nó chứa các phần tử khác.
* `xs:simpleType` - Biểu thị chúng không chứa các phần tử khác.
* `type` - chuỗi, số thập phân, số nguyên, boolean, ngày, giờ,

## Người giới thiệu ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Ví dụ mẫu XSD](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

