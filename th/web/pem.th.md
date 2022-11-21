{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ PEM - รูปแบบไฟล์จดหมายรับรองความเป็นส่วนตัวที่ปรับปรุงแล้ว",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PEM และ API ที่สามารถสร้างและเปิดไฟล์ PEM",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## ไฟล์ PEM คืออะไร??

ไฟล์ PEM เป็นไฟล์ใบรับรองความปลอดภัยที่ใช้เพื่อสร้างช่องทางการสื่อสารที่ปลอดภัยระหว่างเว็บเซิร์ฟเวอร์และเบราว์เซอร์ มีการเข้ารหัส Base64 และอาจมีคีย์ส่วนตัว ใบรับรองเซิร์ฟเวอร์ และ/หรือใบรับรองอื่นๆ รวมกัน ไฟล์ PEM คล้ายกับไฟล์ใบรับรอง .der ในแง่ของการใช้งาน แต่จัดเก็บเป็นข้อความที่เข้ารหัส Base64 แทนที่จะเป็นข้อมูลไบนารี รูปแบบไฟล์ใบรับรองอื่นๆ ที่คล้ายกัน ได้แก่ ไฟล์ [.cer](/th/web/cer/) และ [.crt](/th/web/crt/)

แอปพลิเคชันที่สามารถ **เปิดไฟล์ PEM** รวมถึงโปรแกรมแก้ไขข้อความ เช่น Microsoft Notepad และ Apple TextEdit

## รูปแบบไฟล์ PEM

PEM เป็นรูปแบบไฟล์คอนเทนเนอร์ที่กำหนดโครงสร้างและประเภทการเข้ารหัสของไฟล์ที่ใช้เก็บข้อมูล ไฟล์ PEM ถูกจัดเก็บไว้ในดิสก์เป็นรูปแบบไฟล์ที่เข้ารหัส Base64 ซึ่งมนุษย์ไม่สามารถอ่านได้ มาตรฐานกำหนดว่าไฟล์ PEM เริ่มต้นด้วย:

```
-----BEGIN <type>-----
```
และลงท้ายด้วย:
```
-----END <type>-----
```

เนื้อหาอื่นๆ ภายในเหล่านี้เข้ารหัสด้วยเลขฐาน 64 (ตัวพิมพ์ใหญ่และตัวพิมพ์เล็ก ตัวเลข + และ /) ไฟล์ PEM ไฟล์เดียวสามารถประกอบด้วยหลายบล็อกซึ่งโปรแกรมอื่นๆ สามารถนำไปใช้ได้ หากไฟล์ PEM มีใบรับรองหลายรายการ ใบรับรองแต่ละรายการจะถูกคั่นด้วยบล็อกแต่ละบล็อกดังต่อไปนี้:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### ตัวอย่างไฟล์ PEM

ไฟล์ PEM ที่มีบล็อก CERTIFICATE มักจะมีลักษณะดังนี้:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

ไฟล์ PEM ที่มี RSA เริ่มต้นดังต่อไปนี้

```
-----BEGIN RSA PRIVATE KEY-----
```

## อ้างอิง ##

* [การเข้ารหัสคีย์สาธารณะ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [วิธีสร้างไฟล์ P7C](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

