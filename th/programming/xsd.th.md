{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "ไฟล์ xsd คืออะไร", "วิธีเปิดไฟล์ xsd", "นามสกุล", "ไฟล์", "ไฟล์ xsd", "รูปแบบไฟล์ xsd", "นามสกุล .xsd" ,"ตัวอย่างไฟล์ xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" เรียนรู้เกี่ยวกับรูปแบบไฟล์ XSD และ API ที่สามารถสร้างและเปิดไฟล์ XSD",
  "title" :"รูปแบบไฟล์ XSD - ไฟล์นิยาม XML Schema",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## ไฟล์สคีมา XSD คืออะไร

ไฟล์ XSD เป็นไฟล์คำจำกัดความที่ระบุองค์ประกอบและคุณลักษณะที่สามารถเป็นส่วนหนึ่งของเอกสาร XML สิ่งนี้ทำให้มั่นใจได้ว่าข้อมูลถูกตีความอย่างถูกต้อง และตรวจพบข้อผิดพลาด ส่งผลให้มีการตรวจสอบความถูกต้องของ XML ที่เหมาะสม ไฟล์ XSD ช่วยให้มั่นใจได้ว่าข้อมูลที่ป้อนเป็นไปตามโครงสร้างเดียวกันกับที่กำหนดไว้ในไฟล์ ไฟล์ XSD จัดเก็บอยู่ในรูปแบบไฟล์ [XML](/th/web/xml/) และสามารถเปิดหรือแก้ไขในโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad, Notepad++ หรือ [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## รูปแบบไฟล์ XSD

ไฟล์ XSD ถูกจัดเก็บไว้ในดิสก์ในรูปแบบไฟล์ข้อความธรรมดาที่มนุษย์สามารถอ่านได้ XSD กำหนดองค์ประกอบที่สามารถใช้ในเอกสาร ซึ่งเกี่ยวข้องกับข้อมูลจริงที่จะเข้ารหัส

## ตัวอย่างไฟล์ XSD

ไฟล์ XSD อย่างง่ายที่มีสคีมาของใบสั่งซื้อจะกำหนดองค์ประกอบโดยใช้แท็กตามที่แสดงใน [ตัวอย่าง XSD โดย Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file) ต่อไปนี้ -simple-schema?view=vs-2022)

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

ที่นี่ใช้แท็กต่อไปนี้

* `xs:element` - กำหนดองค์ประกอบ
* `xs:sequence` - หมายถึงองค์ประกอบย่อยที่ปรากฏตามลำดับที่กล่าวถึงเท่านั้น
* `xs:complexType` - แสดงว่ามีองค์ประกอบอื่นๆ
* `xs:simpleType` - แสดงว่าไม่มีองค์ประกอบอื่น
* `type` - สตริง ทศนิยม จำนวนเต็ม บูลีน วันที่ เวลา

## อ้างอิง ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [ตัวอย่าง XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

