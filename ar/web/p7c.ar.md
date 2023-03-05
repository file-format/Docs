{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - ملف شهادة PKCS 7" ,
  "description":"تعرف على تنسيق ملف P7C وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات P7C وفتحها." ,
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف P7C؟

يعد ملف P7C ، مثل ملفات شهادة الأمان الأخرى ، شهادة رقمية تُستخدم لمصادقة الهوية عبر الشبكة. تقوم التطبيقات التي تستخدم الشهادات بمصادقة الهوية باستخدام المفتاح العام المضمن في ملفات الشهادات هذه. يستخدم تشفير المفتاح العام ، أو التشفير غير المتماثل ، زوجًا من المفاتيح أحدهما هو المفتاح العام والآخر يُعرف بالمفتاح الخاص. يتم الاحتفاظ بالمفتاح الخاص آمنًا لتحقيق أمان فعال ، بينما يمكن مشاركة المفتاح العام مع الآخرين. تتضمن تنسيقات ملفات الشهادات الشائعة الأخرى [CRT](/ar/ web / crt /) و DER و PEM.

## تنسيق ملف P7C - مزيد من المعلومات

يتم حفظ ملفات P7C على القرص كملفات ثنائية وتتضمن معلومات المفتاح العام التي تم إنشاؤها باستخدام خوارزميات التشفير بناءً على المشكلات الرياضية. يمكن فتحها في أي محرر نصوص ولكن محتواها ليس في شكل يمكن للبشر قراءته. تتضمن بعض التطبيقات التي يمكنها فتح ملفات P7C ، Apple Keychain Access و Adobe Acrobat Reader DC و Microsoft Certificate Manager و Microsoft Windows Contacts.

### مثال تنسيق ملف P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## مراجع ##

* [تشفير المفتاح العام](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [كيف تنشئ ملف P7C؟](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

