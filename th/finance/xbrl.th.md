{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","ไฟล์ xbrl", "รูปแบบไฟล์ xbrl", "ประเภทไฟล์ xbrl", "ไฟล์", "ประเภท", "ไฟล์ xbrl คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - รูปแบบไฟล์รายงานธุรกิจและการเงิน",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XBRL และ API ที่สามารถสร้างและเปิดไฟล์ XBRL",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## ไฟล์ XBRL คืออะไร??

ไฟล์ที่มีนามสกุล .xbrl (eXtensible Business Reporting Language) เป็นเฟรมเวิร์กทั่วโลกที่ใช้งานได้ฟรีสำหรับการแลกเปลี่ยนข้อมูลทางธุรกิจ ปัจจุบันมีการใช้กันอย่างแพร่หลายเป็นรูปแบบมาตรฐานรูปแบบหนึ่งที่แทนที่รายงานแบบกระดาษแบบเก่าด้วยบันทึกดิจิทัลที่มีประโยชน์และแม่นยำกว่า ข้อมูลที่แลกเปลี่ยนโดยใช้ไฟล์ XBRL รวมถึงบัญชีแยกประเภท รายละเอียดทางการเงิน และงบดุล รองรับแท็กข้อมูลที่อนุญาตให้ประมวลผลข้อมูลตั้งแต่การเตรียมจนถึงขั้นตอนการวิเคราะห์ข้อมูลทางธุรกิจทุกประเภท ไฟล์ XBRL สามารถเปิดได้โดยใช้ซอฟต์แวร์เช่น Rivet Software Dragon View XBRL Viewer และ API เช่น [Aspose.Finance] (https://products.aspose.com/finance)

## รูปแบบไฟล์ XBRL

XBRL เป็นมาตรฐานสากลแบบเปิดสำหรับการรายงานธุรกิจดิจิทัลที่ใช้กันอย่างแพร่หลายทั่วโลก เป็นภาษาที่ใช้ [XML](/th/web/xml/) ซึ่งใช้องค์ประกอบ XBRL หรือที่เรียกว่าแท็ก เพื่ออธิบายข้อมูลธุรกิจแต่ละรายการเพื่อกำหนดข้อมูลสำหรับการจัดเรียงและการวิเคราะห์รายงาน ข้อกำหนดรูปแบบไฟล์ XBRL ได้รับการพัฒนาและเผยแพร่โดย XBRL International, Inc โดยมี [XBRL เวอร์ชัน 2.1] (https:// specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) ในปัจจุบัน มีให้สำหรับผู้ใช้

### โครงสร้างเอกสาร XBRL

ข้อมูลที่สมบูรณ์เกี่ยวกับ [แท็ก XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) สามารถอ้างอิงโดยโปรแกรมเมอร์เพื่อเขียนแอปพลิเคชันสำหรับการทำงานรูปแบบไฟล์นี้ XBRL ประกอบด้วยอินสแตนซ์ XBRL และชุดอนุกรมวิธาน

**`XBRL Instance`** - อินสแตนซ์ XBRL เริ่มต้นด้วย<xbrl> องค์ประกอบราก เอกสาร XML ขนาดใหญ่สามารถมีอินสแตนซ์ XBRL ฝังอยู่ในนั้นได้มากกว่าหนึ่งรายการ

**`XBRL Taxonomy`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) ถูกกำหนดเป็นโครงสร้างสคีมา XML และชุดขององค์ประกอบลิงก์ภายนอกที่อ้างอิงโดยตรง สคีมาอนุกรมวิธานที่ปรับขนาดได้ซึ่งแสดงการอ้างอิงลิงค์เบสมีดังต่อไปนี้

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


## อ้างอิง ##

* [XBRL - โดย Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [ภาษาการรายงานทางธุรกิจที่ขยายได้ (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- ผิดพลาด-2013-02-20.html)

