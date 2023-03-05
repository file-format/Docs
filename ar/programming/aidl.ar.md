{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف AIDL - ملف لغة تعريف واجهة Android" ,
  "description":"تعرف على ما هو تنسيق ملف AIDL مع أمثلة وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات AIDL وفتحها." ,
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-10-30"
}

## ما هو ملف AIDL؟

يسمح ملف AIDL (لغة تعريف واجهة Android) لمطوري Android بإنشاء اتصال بين التطبيقات المختلفة. بناءً على واجهة البرمجة ، يوافق كل من العميل والخدمة على التواصل باستخدام الاتصال بين العمليات (IPC). يحتوي ملف AIDL على كود مصدر [Java](/ar/ برمجة / جافا /) لتحديد هذه الواجهات وعقود الاتصال بين التطبيقات.

يمكنك فتح ملفات AIDL باستخدام Google Android Studio أو أي محرر نصوص مثل Microsoft Notepad و Notepad ++.

## تنسيق ملف AIDL - مزيد من المعلومات

AIDL هي ملفات نصية تحتوي على واجهات للاتصال بين التطبيقات. لا يسمح نظام التشغيل Android لعملية واحدة بالوصول إلى ذاكرة عملية أخرى. يؤدي هذا إلى تقسيم العمليات إلى عناصر أولية لفهم نظام التشغيل الأساسي وإنشاء عملية هياكل الاتصال للمطور.

### ما هي أنواع البيانات التي يدعمها AIDL؟

يدعم AIDL أنواع البيانات التالية بشكل افتراضي.

* جميع الأنواع البدائية في لغة برمجة Java (مثل int ، و long ، و char ، و boolean ، وما إلى ذلك)
* سلسلة
* CharSequence
* قائمة
* خريطة

## مثال على ملف AIDL

فيما يلي مثال لملف AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## مراجع

* [لغة تعريف واجهة Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

