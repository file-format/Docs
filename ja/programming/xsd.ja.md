{
  "date" : "2022-02-06",
  "keywords" :[ "xsd",".xsd","xsd ファイルとは","xsd ファイルの開き方","拡張子","ファイル","xsd ファイル","xsd ファイル形式",".xsd 拡張子" ,"xsd ファイルの例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" XSD ファイル形式と,XSD ファイルを作成して開くことができる API について学びます。",
  "title" :"XSD ファイル形式 - XML スキーマ定義ファイル",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## XSD スキーマ ファイルとは何ですか?

XSD ファイルは、XML ドキュメントの一部となる要素と属性を指定する定義ファイルです。これにより、データが適切に解釈され、エラーが捕捉され、適切な XML 検証が行われます。 XSD ファイルは、入力されたデータがファイルで定義されているのと同じ構造に従うことを保証します。 XSD ファイルは [XML](/web/xml/) ファイル形式で保存され、Microsoft Notepad、Notepad++、または [Microsoft XML Notepad](https://microsoft.github.io) などの任意のテキスト エディターで開いたり編集したりできます。 /Xmlメモ帳/)。

## XSD ファイル形式

XSD ファイルは、人間が判読できるプレーン テキスト ファイル形式でディスクに保存されます。 XSD は、ドキュメントがエンコードされる実際のデータに関連して、ドキュメントで使用できる要素を定義します。

## XSD ファイルの例

注文書スキーマを持つ単純な XSD ファイルは、次の [Microsoft による XSD の例](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022) に示すように、タグを使用して要素を定義します。

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

ここでは、以下のタグを使用します。

* `xs:element` - 要素を定義します。
* `xs:sequence` - 子要素が記載された順序でのみ出現することを示します。
* `xs:complexType` - 他の要素が含まれていることを示します。
* `xs:simpleType` - 他の要素を含まないことを示します。
* `type` - 文字列、10 進数、整数、ブール値、日付、時刻、

## 参照 ##

- [Microsoft XML メモ帳](https://microsoft.github.io/XmlNotepad/)
- [XSD サンプルの例](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

