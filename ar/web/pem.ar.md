{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف PEM - تنسيق ملف شهادة البريد المحسن للخصوصية" ,
  "description":"تعرف على تنسيق ملف PEM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PEM وفتحها." ,
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2022-09-14"
}

## ما هو ملف PEM؟

ملف PEM هو ملف شهادة أمان يُستخدم لإنشاء قناة اتصال آمنة بين خادم الويب والمستعرض. إنه مشفر باستخدام Base64 وقد يحتوي على مفتاح خاص و / أو شهادة خادم و / أو مجموعة من الشهادات الأخرى. تشبه ملفات PEM ملفات شهادة .der من حيث الاستخدام ولكن يتم تخزينها كنص بترميز Base64 بدلاً من بيانات ثنائية. تتضمن تنسيقات ملفات الشهادات المماثلة الأخرى ملفات [.cer](/ar/web/cer/) و [.crt](/ar/web/crt/).

تتضمن التطبيقات التي يمكنها ** فتح ملفات PEM ** برامج تحرير النصوص مثل Microsoft Notepad و Apple TextEdit.

## تنسيق ملف PEM

PEM هو تنسيق ملف حاوية يحدد بنية ونوع الترميز للملف المستخدم لتخزين البيانات. يتم تخزين ملفات PEM على القرص كتنسيق ملف مشفر باستخدام Base64 غير قابل للقراءة من قبل الإنسان. يحدد المعيار أن ملف PEM يبدأ بـ:

```
-----BEGIN <type>-----
```
وينتهي بـ:
```
-----END <type>-----
```

جميع المحتويات الأخرى الموجودة بداخلها مشفرة بـ base64 (أحرف كبيرة وصغيرة وأرقام و + و /). يمكن أن يتكون ملف PEM واحد من عدة كتل يمكن استخدامها بواسطة برامج أخرى. إذا كان ملف PEM يحتوي على شهادات متعددة ، فسيتم فصل كل شهادة بكتل فردية على النحو التالي:

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

### مثال ملف PEM

عادةً ما يبدو ملف PEM مع كتلة CERTIFICATE كما يلي:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

يبدأ ملف PEM مع RSA كما يلي.

```
-----BEGIN RSA PRIVATE KEY-----
```

## مراجع ##

* [تشفير المفتاح العام](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [كيف تنشئ ملف P7C؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

