{
  "date" : "2021-07-12",
  "keywords" :["cmd file", "what is a cmd file", "file", "cmd example", "cmd file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف CMD وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CMD وفتحها." ,
  "title" :"CMD - تنسيق ملف أوامر Windows" ,
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-07-12"
}

## ما هو ملف CMD؟
يتكون ملف CMD من برنامج نصي يحتوي على أمر واحد أو عدة أوامر في شكل نص عادي يتم تشغيلها من أجل تنفيذ المهام المختلفة. إنه مشابه لملف [BAT] (/ar/ قابل للتنفيذ / bat /) ، والذي يستخدم أيضًا بشكل عام لتخزين مجموعة من الأوامر القابلة للتنفيذ. تستخدم ملفات CMD على نطاق واسع في نظام التشغيل Microsoft Windows. تم تقديم هذه الملفات في التسعينيات تقريبًا ولكنها لا تزال مستخدمة في أحدث نظام تشغيل Windows. تتم كتابة هذه الملفات بشكل عام لتنفيذ أكثر من أمر واحد في تسلسل.

## تنسيق ملف CMD
CMD هو تنسيق ملف تستخدمه البرامج التنفيذية على غرار CP / M. يمكن مقارنته عمومًا بـ [COM] (/ar/ قابل للتنفيذ / com /) في CP / M-80 و [EXE] (/ar/ قابل للتنفيذ / exe /) في DOS. يحتوي ملف CMD على 1 إلى 8 مجموعات من التعليمات البرمجية أو البيانات ورأس 128 بايت. يمكن أن يصل حجم كل مجموعة إلى 1 ميغابايت. يمكن أن تحتوي ملفات CMD أيضًا على معلومات النقل وامتدادات النظام المقيم (RSXs) في إصداراتها الأحدث. CMD هو وافد جديد بالمقارنة مع ملف [BAT] (/ar/ قابل للتنفيذ / بات /) ؛ تستخدم لـ MS-DOS قبل إصدار windows في MS-DOS. على الرغم من أنه لا يزال بإمكانك حفظ الملفات بامتداد .bat اليوم ، إلا أن العديد من الأشخاص يستخدمون الامتداد .cmd لحفظ البرامج النصية القابلة للتنفيذ.

### مواصفات تنسيق CMD

تحتوي بداية الرأس على قائمة المجموعات الموجودة في الملف مع أنواعها. يمكن استخدام كل نوع مرة واحدة على الأكثر. هذه الأنواع هي:

- شفرة
- بيانات
- إضافي
- كومة
- المستخدم 1
- المستخدم 2
- المستخدم 3
- المستخدم 4
- كود مشترك

وبالمثل بادئة جزء البرنامج في DOS ، فإن أول 256 بايت من مجموعة البيانات هي صفر. سيتم ملؤها بواسطة CP / M-86 بصفحة الصفر. إذا لم تكن هناك مجموعة بيانات ، فسيتم استخدام أول 256 بايت من مجموعة التعليمات البرمجية بدلاً من ذلك.
## مثال على ملف CMD
فيما يلي مثال على برنامج نصي CMD لإظهار معلومات الأنظمة.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## مراجع

* [كيفية كتابة نص CMD] (https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [ملف CMD (CP / M) - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/CMD_file_ (CP / M))

