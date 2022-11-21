{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف KEY وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات KEY وفتحها." ,
  "title" :"تنسيق ملف KEY - ملف مفتاح خاص للبريد المحسن للخصوصية" ,
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
} ,
  "lastmod" : "2022-07-04"
}

## ما هو ملف KEY؟

ملف KEY هو الجزء الخاص من آلية الأمان التي يتم حفظها على القرص بتنسيق ملف Privacy-Enhanced Mal (PEM). يتم استخدامه لفك تشفير المعلومات المتبادلة بين متصفح الويب وخادم الويب الذي يخدم طلبات التصفح. يحتوي ملف KEY على سلاسل مشفرة غير مجدية للعين البشرية ولكنها جوهر تشفير / فك تشفير تبادل المعلومات كجزء من شهادة SSL على خوادم الويب. يتم إنشاء ملفات KEY تلقائيًا ويتم تثبيتها في نهاية العميل.

يمكنك فتح ملفات ** KEY ** باستخدام أي محرر نصوص مثل Microsoft Notepad (Windows) أو Apple TextEdit (Mac) أو GitHub Atom (عبر الأنظمة الأساسية). تشبه ملفات KEY تنسيقات ملفات [CRT] (/ar/ web / crt /) و [CER] (/ar/ web / cer /).

## تنسيق الملف الرئيسي - مزيد من المعلومات

يتم تخزين ملفات KEY على القرص كملفات نصية عادية ولكنها سلاسل مشفرة ليست سهلة القراءة. من الناحية العملية ، لا يفهم المستخدمون السلاسل عند فتحها في محرر نصوص. شهادة المفتاح الخاص سرية ولا يجب مشاركتها مع أي شخص. تتضمن العملية الكاملة لتأمين تبادل المعلومات عبر الإنترنت ما يلي:

* ** المفتاح العام ** - يستخدم لتشفير معلومات المستخدم لتبادل البيانات بين المتصفح وخوادم الويب
* ** مفتاح خاص ** - يستخدم لفك تشفير المعلومات كما يتم تلقيها بواسطة خادم الويب

شهادات SSL ، المعروفة أيضًا باسم شهادات X.509 ، فريدة لكل موقع ويب. ملفات KEY باستخدام بناء الجملة التالي:

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

### مثال ملف رئيسي

فيما يلي مثال على ملف المفتاح الخاص.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## مراجع

* [المفاتيح العمومية والمفاتيح الخاصة والشهادات] (https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

