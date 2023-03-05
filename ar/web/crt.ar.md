{
  "date" : "2019-10-11",
  "keywords" :["crt" , "ملف crt" , "تنسيق ملف crt" , "نوع ملف crt" , "ملف" , "النوع" , "ما هو ملف crt"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - تنسيق ملف شهادة الأمان" ,
  "description":"تعرف على تنسيق ملف CRT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CRT وفتحها." ,
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف CRT؟

الملف ذو الامتداد .crt هو ملف شهادة أمان تستخدمه مواقع الويب الآمنة لتأسيس اتصالات آمنة من خادم الويب إلى المستعرض. تتيح مواقع الويب الآمنة تأمين عمليات نقل البيانات وتسجيلات الدخول ومعاملات بطاقات الدفع وتوفير تصفح آمن للموقع. إذا فتحت موقعًا آمنًا ، فسترى رمز "قفل" في شريط العناوين. إذا قمت بالنقر فوقه ، يمكنك عرض تفاصيل الشهادة المثبتة. تقوم الشركات الدولية مثل Verisign و Thawte بتوزيع شهادات SSL هذه.

## تنسيق ملف CRT

ملفات CRT بتنسيق ASCII ويمكن فتحها في أي محرر نصوص لعرض محتويات ملف الشهادة. وهي تتبع معيار الشهادة X.509 الذي يحدد هيكل الشهادة. يحدد حقول البيانات التي يجب تضمينها في شهادة SSL. ينتمي CRT إلى تنسيق PEM للشهادات التي هي ملفات مشفرة Base64 ASCII.

### بنية ملف PEM

يمكن أن يحتوي ملف PEM على شهادات متعددة. في مثل هذه الحالة ، تتبع كل شهادة في ملف PEM الهيكل التالي.

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

### مثال على تنسيق ملف CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## مراجع ##

* [المفاتيح العمومية والمفاتيح الخاصة والشهادات](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

