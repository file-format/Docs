{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","什么是 xsd 文件","如何打开 xsd 文件","扩展名","文件","xsd 文件","xsd 文件格式",".xsd 扩展名" ,"xsd 文件示例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" 了解 XSD 文件格式和可以创建和打开 XSD 文件的 API。",
  "title" :"XSD 文件格式 - XML 模式定义文件",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## 什么是 XSD 架构文件？

XSD 文件是一个定义文件，它指定可以成为 XML 文档的一部分的元素和属性。这可确保正确解释数据并捕获错误，从而进行适当的 XML 验证。 XSD 文件确保输入的数据遵循文件中定义的相同结构。 XSD 文件以 [XML](/zh/web/xml/) 文件格式存储，可以在任何文本编辑器中打开或编辑，例如 Microsoft Notepad、Notepad++ 或 [Microsoft XML Notepad](https://microsoft.github.io /Xml记事本/）。

## XSD 文件格式

XSD 文件以人类可读的纯文本文件格式存储到光盘中。 XSD 定义了可以在文档中使用的元素，这些元素与要编码的实际数据相关。

## XSD 文件示例

具有采购订单架构的简单 XSD 文件使用标签定义元素，如以下 [Microsoft 的 XSD 示例](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022）。

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

在这里，使用了以下标签。

* `xs:element` - 定义一个元素。
* `xs:sequence` - 表示子元素仅按提到的顺序出现。
* `xs:complexType` - 表示它包含其他元素。
* `xs:simpleType` - 表示它们不包含其他元素。
* `type` - 字符串、十进制、整数、布尔值、日期、时间、

## 参考 ＃＃

- [微软 XML 记事本](https://microsoft.github.io/XmlNotepad/)
- [XSD 示例示例](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

