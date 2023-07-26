
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ APK - ไฟล์ APK Set",
  "description":"เรียนรู้เกี่ยวกับไฟล์ APKS คืออะไร",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## ไฟล์ APKS คืออะไร?

ไฟล์ที่มีนามสกุล .apks คือไฟล์เก็บถาวรที่เป็นชุดของไฟล์ **APK** ของแพ็กเกจ Android ไฟล์ APK แต่ละไฟล์ในไฟล์ APKS ถูกสร้างขึ้นโดยคำนึงถึงแง่มุมต่างๆ ของอุปกรณ์ ซึ่งรวมถึงสถาปัตยกรรม ภาษา ความหนาแน่นของหน้าจอ และคุณสมบัติอื่นๆ ของอุปกรณ์ ไฟล์ APKS สร้างโดย **bundletool** ใช้เพื่อสร้าง Android App Bundle และแปลง App Bundle เป็น APK ที่แตกต่างกันสำหรับการปรับใช้บนอุปกรณ์

## รูปแบบไฟล์ APKS - ข้อมูลเพิ่มเติม

ไฟล์ APKS ถูกบันทึกเป็นไฟล์บีบอัดโดยใช้รูปแบบไฟล์ [ZIP](/th/compression/zip/)

## จะสร้างไฟล์ APKS ได้อย่างไร?

เมื่อ Android App Bundle (AAB) พร้อมแล้ว จะสามารถทดสอบลักษณะการทำงานใน Google Play Store เพื่อปรับใช้กับอุปกรณ์ได้ สามารถสร้างไฟล์ APKS จากไฟล์ AAB และติดตั้งในอุปกรณ์ทดสอบโดยใช้ Android [bundletool] ของ Google (https://developer.android.com/tools/bundletool) ของ Google มีเครื่องมือบรรทัดคำสั่งเพื่อสร้างไฟล์เก็บถาวร APKS จาก APK โดยใช้คำสั่งต่อไปนี้

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

ในการปรับใช้ APK บนอุปกรณ์ สามารถลงนามไฟล์ APKS ด้วยข้อมูลการลงนามอุปกรณ์ดังนี้

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## อ้างอิง

* [bundletool - commandline](https://developer.android.com/tools/bundletool)

