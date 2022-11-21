{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ KEY และ API ที่สามารถสร้างและเปิดไฟล์ KEY",
  "title" :"รูปแบบไฟล์ KEY - ไฟล์คีย์ส่วนตัวของ Mail ที่ปรับปรุงความเป็นส่วนตัว",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## ไฟล์ KEY คืออะไร?

ไฟล์ KEY เป็นส่วนส่วนตัวของกลไกความปลอดภัยที่บันทึกลงดิสก์ในรูปแบบไฟล์ Privacy-Enhanced Mal (PEM) ใช้เพื่อถอดรหัสข้อมูลที่แลกเปลี่ยนระหว่างเว็บเบราว์เซอร์และเว็บเซิร์ฟเวอร์ที่ให้บริการคำขอการสืบค้น ไฟล์ KEY มีสตริงที่เข้ารหัสซึ่งไม่มีประโยชน์สำหรับสายตามนุษย์ แต่เป็นสาระสำคัญของการเข้ารหัส/ถอดรหัสการแลกเปลี่ยนข้อมูลซึ่งเป็นส่วนหนึ่งของใบรับรอง SSL บนเว็บเซิร์ฟเวอร์ ไฟล์ KEY จะถูกสร้างขึ้นโดยอัตโนมัติและติดตั้งที่ส่วนท้ายของไคลเอนต์

คุณสามารถเปิดไฟล์ **KEY** ด้วยโปรแกรมแก้ไขข้อความใดก็ได้ เช่น Microsoft Notepad (Windows), Apple TextEdit (Mac) หรือ GitHub Atom (ข้ามแพลตฟอร์ม) ไฟล์ KEY คล้ายกับรูปแบบไฟล์ [CRT](/th/web/crt/) และ [CER](/th/web/cer/)

## รูปแบบไฟล์ KEY - ข้อมูลเพิ่มเติม

ไฟล์ KEY ถูกจัดเก็บไว้ในดิสก์เป็นไฟล์ข้อความธรรมดา แต่เป็นสตริงที่เข้ารหัสซึ่งไม่เป็นมิตรกับมนุษย์ในการอ่าน ในทางปฏิบัติ ผู้ใช้ไม่มีความเข้าใจเกี่ยวกับสตริงเมื่อเปิดในโปรแกรมแก้ไขข้อความ ใบรับรองคีย์ส่วนตัวเป็นความลับและไม่ควรแบ่งปันกับใคร กระบวนการที่สมบูรณ์ในการรักษาความปลอดภัยการแลกเปลี่ยนข้อมูลทางอินเทอร์เน็ตเกี่ยวข้องกับ:

* **คีย์สาธารณะ** - ใช้เพื่อเข้ารหัสข้อมูลของผู้ใช้เพื่อแลกเปลี่ยนข้อมูลระหว่างเบราว์เซอร์และเว็บเซิร์ฟเวอร์
* **คีย์ส่วนตัว** - ใช้เพื่อถอดรหัสข้อมูลที่เว็บเซิร์ฟเวอร์ได้รับ

ใบรับรอง SSL หรือที่เรียกว่าใบรับรอง X.509 นั้นไม่ซ้ำกันสำหรับแต่ละเว็บไซต์ ไฟล์ KEY โดยใช้ไวยากรณ์ต่อไปนี้:

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### ตัวอย่างไฟล์ KEY

ต่อไปนี้เป็นตัวอย่างของไฟล์คีย์ส่วนตัว
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## อ้างอิง

* [คีย์สาธารณะ คีย์ส่วนตัว และใบรับรอง](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

