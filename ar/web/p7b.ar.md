{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - ملف شهادة PKCS 7" ,
  "description":"تعرف على تنسيق ملف P7C وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات P7C وفتحها." ,
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف P7B؟

ملف P7B هو ملف شهادة أمان يحتوي على شهادة رقمية آمنة لمصادقة شخص أو جهاز. على غرار ملف شهادة [.cer](/ar/web/cer/) ، يمكن تثبيت ملف P7B باستخدام خيار "تثبيت الشهادة" باستخدام خيار النقر بزر الماوس الأيمن على الملف. يستخدم P7B خيار تنسيق مختلفًا عن تنسيق ملف CER. يحتوي على ملف أو أكثر من ملفات الشهادات الرقمية X.509 التي تستخدم ترميز base64 (ASCII). يتم استلام ملفات P7B كملف [ZIP](/ar/compression/zip/) أو استلامها من المرجع المصدق.

## تنسيق ملف P7B

يتم تخزين ملفات P7B كملفات ASCII عادية يمكن فتحها في أي محرر نصوص. يحتوي على المفتاح العام وهو عبارة عن سلسلة مشفرة لا معنى لها من وجهة نظر المقروئية.

### مثال تنسيق ملف P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## مراجع ##

* [تشفير المفتاح العام](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [كيف تنشئ ملف P7C؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

