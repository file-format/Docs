{
  "date" : "2019-10-11",
  "keywords" :[ "crt","ไฟล์ crt", "รูปแบบไฟล์ crt", "ประเภทไฟล์ crt", "ไฟล์", "ประเภท", "ไฟล์ crt คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - รูปแบบไฟล์ใบรับรองความปลอดภัย",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CRT และ API ที่สามารถสร้างและเปิดไฟล์ CRT",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ CRT คืออะไร??

ไฟล์ที่มีนามสกุล .crt คือไฟล์ใบรับรองความปลอดภัยที่ใช้โดยเว็บไซต์ที่ปลอดภัยเพื่อสร้างการเชื่อมต่อที่ปลอดภัยจากเว็บเซิร์ฟเวอร์ไปยังเบราว์เซอร์ เว็บไซต์ที่ปลอดภัยทำให้สามารถโอนข้อมูล เข้าสู่ระบบ ทำธุรกรรมบัตรชำระเงินได้อย่างปลอดภัย และให้การเรียกดูไซต์ที่ได้รับการป้องกัน หากคุณเปิดเว็บไซต์ที่ปลอดภัย คุณจะเห็นไอคอน "ล็อค" ในแถบที่อยู่ หากคุณคลิกที่มัน คุณสามารถดูรายละเอียดของใบรับรองที่ติดตั้ง บริษัทระหว่างประเทศ เช่น Verisign และ Thawte จัดจำหน่ายใบรับรอง SSL เหล่านี้

## รูปแบบไฟล์ CRT

ไฟล์ CRT อยู่ในรูปแบบ ASCII และสามารถเปิดได้ในโปรแกรมแก้ไขข้อความเพื่อดูเนื้อหาของไฟล์ใบรับรอง เป็นไปตามมาตรฐานการรับรอง X.509 ที่กำหนดโครงสร้างของใบรับรอง กำหนดฟิลด์ข้อมูลที่ควรจะรวมอยู่ในใบรับรอง SSL CRT เป็นของใบรับรองรูปแบบ PEM ที่เป็นไฟล์เข้ารหัส Base64 ASCII

### โครงสร้างไฟล์ PEM

ไฟล์ PEM สามารถมีใบรับรองได้หลายใบ ในกรณีดังกล่าว ใบรับรองแต่ละรายการในไฟล์ PEM จะเป็นไปตามโครงสร้างต่อไปนี้

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

### ตัวอย่างรูปแบบไฟล์ CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## อ้างอิง ##

* [คีย์สาธารณะ คีย์ส่วนตัว และใบรับรอง](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

