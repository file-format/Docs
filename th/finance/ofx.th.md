{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - รูปแบบไฟล์การแลกเปลี่ยนทางการเงินแบบเปิด",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OFX และ API ที่สามารถสร้างและเปิดไฟล์ OFX",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## ไฟล์ OFX คืออะไร??

ไฟล์ OFX (Open Financial Exchange) เป็นรูปแบบไฟล์ทางการเงินที่ใช้สำหรับการแลกเปลี่ยนข้อมูลทางการเงินระหว่างโปรแกรมซอฟต์แวร์และสถาบันการเงิน ด้วยวิวัฒนาการของโซลูชันซอฟต์แวร์สำหรับการเก็บบัญชีการเงินภายในองค์กร โปรแกรมซอฟต์แวร์ได้รับการพัฒนาที่สามารถเชื่อมต่อกับธนาคารของคุณและนำเข้าหรือส่งออกข้อมูลทางการเงินกับธนาคารได้ ซึ่งรวมถึงข้อมูลทางการเงิน เช่น ธุรกรรม ข้อมูลบัญชี และการชำระบิล โปรแกรมซอฟต์แวร์เช่น QuickBooks, Microsoft Money, Intuit และ Quicken บันทึกข้อมูลที่นำเข้าเป็นไฟล์ OFX

ประเภทสื่ออินเทอร์เน็ตสำหรับรูปแบบไฟล์ OFX คือ application/x-ofx

## รูปแบบไฟล์ OFX

ไฟล์ OFX จะถูกบันทึกในรูปแบบไฟล์ XML (Extensible Markup Language) และใช้แท็กเพื่อจัดโครงสร้างข้อมูล ไฟล์ [XML](/th/web/xml/) จะถูกจัดเก็บในรูปแบบที่มนุษย์สามารถอ่านได้ และสามารถเปิดและแก้ไขได้ในโปรแกรมแก้ไขข้อความใดๆ เช่น Notepad, Notepad++ หรือ Apple TextEdit ข้อมูลที่จัดเก็บไว้ในไฟล์ OFX เป็นไปตามมาตรฐาน **SGML (Standard Generalized Markup Language)** ข้อมูลที่เก็บไว้ในไฟล์ OFX โดยทั่วไปจะประกอบด้วย:

* ข้อมูลที่เกี่ยวข้องกับธนาคาร
* ข้อมูลบัตรเครดิตและเดบิต
* ข้อมูลบัญชีและการลงทุน
* ธุรกรรมทางการเงินอื่น ๆ

### ตัวอย่างรูปแบบไฟล์ OFX

ต่อไปนี้เป็นโครงสร้างข้อมูลภายในและข้อมูลตัวอย่างของไฟล์ OFX ตัวอย่าง

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

ไฟล์ OFX ตัวอย่างนี้มีข้อมูลต่อไปนี้:

* ข้อมูลบัญชีธนาคาร เช่น ชื่อธนาคาร หมายเลขบัญชี และยอดเงินคงเหลือ
* รายการรายการ รวมถึงวันที่ ประเภท และจำนวนรายการแต่ละรายการ

ข้อมูลทั้งหมดนี้สามารถนำเข้ามาในโปรแกรมซอฟต์แวร์การเงินส่วนบุคคลเพื่อติดตามธุรกรรมทางบัญชีและค่าใช้จ่าย

## ข้อมูลอ้างอิง ##

* [Open Financial Exchange - โดย Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [มาตรฐาน ISO สำหรับการแลกเปลี่ยนข้อมูลทางอิเล็กทรอนิกส์](https://en.wikipedia.org/wiki/ISO_20022)

