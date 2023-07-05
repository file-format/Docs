
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف APKS - أرشيف مجموعة APK" ,
  "description":"تعرف على ما هو ملف APKS؟" ,
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-02-06"
}

## ما هو ملف APKS؟

الملف بامتداد .apks هو ملف أرشيف عبارة عن مجموعة من ملفات حزمة Android ** APK **. يتم إنشاء كل ملف APK فردي في ملف APKS مع مراعاة الجوانب المختلفة للأجهزة. يتضمن ذلك الهندسة المعمارية واللغة وكثافة الشاشة وميزات الجهاز الأخرى. يتم إنشاء ملفات APKS بواسطة ** bundletool **. يتم استخدامه لإنشاء حزمة تطبيقات Android وتحويل حزمة التطبيقات إلى ملفات APK مختلفة للنشر على الأجهزة.

## تنسيق ملف APKS - مزيد من المعلومات

يتم حفظ ملفات APKS كملفات مضغوطة باستخدام تنسيق ملف [ZIP](/ar/compression/zip/).

## كيف يتم إنشاء ملف APKS؟

عندما تكون حزمة تطبيقات Android (AAB) جاهزة ، يمكن اختبار سلوكها على متجر Google Play للنشر على الجهاز. يمكن إنشاء ملفات APKS ، لهذا الغرض ، من ملفات AAB وتثبيتها على أجهزة الاختبار باستخدام Android [bundletool] من Google (https://developer.android.com/studio/command-line/bundletool). يوفر أدوات سطر الأوامر لإنشاء ملف أرشيف APKS من ملفات APK باستخدام الأمر التالي.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

لنشر ملفات APK على جهاز ، يمكن توقيع ملف APKS باستخدام معلومات توقيع الجهاز على النحو التالي.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## مراجع

* [bundletool - commandline](https://developer.android.com/studio/command-line/bundletool)

