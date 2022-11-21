{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ใบรับรอง P7C - PKCS 7",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ P7C และ API ที่สามารถสร้างและเปิดไฟล์ P7C",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ P7C คืออะไร??

ไฟล์ P7C เช่นเดียวกับไฟล์ใบรับรองความปลอดภัยอื่นๆ คือใบรับรองดิจิทัลที่ใช้ในการตรวจสอบตัวตนผ่านเครือข่าย แอปพลิเคชันที่ใช้ใบรับรองจะตรวจสอบตัวตนโดยใช้คีย์สาธารณะที่รวมอยู่ในไฟล์ใบรับรองเหล่านี้ การเข้ารหัสคีย์สาธารณะหรือการเข้ารหัสแบบอสมมาตร ใช้คีย์คู่หนึ่งซึ่งคีย์หนึ่งเป็นคีย์สาธารณะและอีกคีย์หนึ่งเรียกว่าคีย์ส่วนตัว คีย์ส่วนตัวจะถูกเก็บไว้อย่างปลอดภัยเพื่อการรักษาความปลอดภัยที่มีประสิทธิภาพ ในขณะที่คีย์สาธารณะสามารถแชร์กับผู้อื่นได้ รูปแบบไฟล์ใบรับรองทั่วไปอื่นๆ ได้แก่ [CRT](/th/web/crt/), DER และ PEM

## รูปแบบไฟล์ P7C - ข้อมูลเพิ่มเติม

ไฟล์ P7C ถูกบันทึกลงดิสก์เป็นไฟล์ไบนารีและรวมข้อมูลคีย์สาธารณะที่สร้างขึ้นโดยใช้อัลกอริทึมการเข้ารหัสตามปัญหาทางคณิตศาสตร์ สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ แต่เนื้อหาไม่ได้อยู่ในรูปแบบที่มนุษย์สามารถอ่านได้ แอปพลิเคชั่นบางตัวที่สามารถเปิดไฟล์ P7C ได้แก่ Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager และ Microsoft Windows Contacts

### ตัวอย่างรูปแบบไฟล์ P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## อ้างอิง ##

* [การเข้ารหัสคีย์สาธารณะ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [วิธีสร้างไฟล์ P7C](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

