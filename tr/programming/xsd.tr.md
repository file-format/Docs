{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","xsd dosyası nedir","xsd dosyası nasıl açılır", "uzantı", "dosya", "xsd dosyası","xsd dosya formatı", ".xsd uzantısı" ,"xsd dosya örneği"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" XSD dosya formatı ve bir XSD dosyası oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"XSD Dosya Biçimi - XML Şema Tanımlama Dosyası",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## XSD Şema dosyası nedir?

Bir XSD dosyası, bir XML belgesinin parçası olabilecek öğeleri ve nitelikleri belirten bir tanım dosyasıdır. Bu, verilerin uygun şekilde yorumlanmasını ve hataların yakalanmasını sağlayarak uygun XML doğrulamasıyla sonuçlanır. XSD dosyaları, girilen verilerin dosyada tanımlanan yapıyla aynı olmasını sağlar. XSD dosyaları [XML](/tr/web/xml/) dosya formatında saklanır ve Microsoft Notepad, Notepad++ veya [Microsoft XML Notepad](https://microsoft.github.io) gibi herhangi bir metin düzenleyicide açılabilir veya düzenlenebilir /XmlNot Defteri/).

## XSD Dosya Biçimi

XSD dosyaları, insan tarafından okunabilen düz metin dosyası biçiminde diske kaydedilir. Bir XSD, kodlanacak gerçek verilerle ilgili olarak belgelerde kullanılabilecek öğeleri tanımlar.

## XSD Dosyası Örneği

Bir satınalma siparişi şemasına sahip basit bir XSD dosyası, aşağıdaki [Microsoft tarafından sunulan XSD örneğinde](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022) gösterildiği gibi etiketleri kullanan öğeleri tanımlar.

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

Burada aşağıdaki etiketler kullanılmaktadır.

* `xs:element` - Bir eleman tanımlar.
* `xs:sequence` - Alt öğelerin yalnızca belirtilen sırada göründüğünü belirtir.
* `xs:complexType` - Diğer öğeleri içerdiğini belirtir.
* `xs:simpleType` - Başka öğeler içermediklerini belirtir.
* `type` - string, ondalık, tamsayı, boolean, tarih, saat,

## Referanslar ##

- [Microsoft XML Not Defteri](https://microsoft.github.io/XmlNotepad/)
- [XSD Örnek Örneği](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

