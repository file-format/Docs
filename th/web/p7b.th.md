{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ใบรับรอง P7B - PKCS 7",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ P7C และ API ที่สามารถสร้างและเปิดไฟล์ P7C",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ P7B คืออะไร??

ไฟล์ P7B เป็นไฟล์ใบรับรองความปลอดภัยที่มีใบรับรองดิจิทัลที่ปลอดภัยสำหรับตรวจสอบบุคคลหรืออุปกรณ์ คล้ายกับไฟล์ใบรับรอง [.cer](/th/web/cer/) ไฟล์ P7B สามารถติดตั้งได้โดยใช้ตัวเลือก "ติดตั้งใบรับรอง" โดยใช้ตัวเลือกคลิกขวาที่ไฟล์ P7B ใช้ตัวเลือกการจัดรูปแบบที่แตกต่างจากรูปแบบไฟล์ CER ประกอบด้วยไฟล์ใบรับรองดิจิทัล X.509 อย่างน้อยหนึ่งไฟล์ที่ใช้การเข้ารหัส base64 (ASCII) ไฟล์ P7B ได้รับเป็นไฟล์ [ZIP](/th/compression/zip/) หรือได้รับจากผู้ออกใบรับรอง

## รูปแบบไฟล์ P7B

ไฟล์ P7B ถูกจัดเก็บเป็นไฟล์ ASCII ธรรมดาที่สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ มันมีรหัสสาธารณะที่เป็นสตริงที่เข้ารหัสซึ่งไม่มีความหมายจากมุมมองที่อ่านได้

### ตัวอย่างรูปแบบไฟล์ P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## อ้างอิง ##

* [การเข้ารหัสคีย์สาธารณะ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [วิธีสร้างไฟล์ P7C](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

