{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - تنسيق ملف مجموعة TrueType" ,
  "description":"يجمع ملف TrueType Collection (TTC) عدة خطوط في ملف واحد. استخدمت كل من Apple و Microsoft TTF على أنظمة تشغيل Mac و Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
} ,
  "lastmod" : "2021-02-25"
}

## ما هو ملف TTC؟
يتم اختصار TTC لأن مجموعة TrueType هي امتداد لتنسيق True Type. يمكن لملف TTC دمج ملفات الخطوط المتعددة فيه. هذه الملفات مفيدة لدمج العديد من الخطوط التي تشترك في العديد من الحروف الرسومية المشتركة. قبل Windows 2000 ، تم استخدام ملفات TTC في الإصدارات الصينية واليابانية والكورية من النوافذ ولكن فيما بعد كان الدعم متاحًا لجميع المناطق.


## هيكل ملف مجموعة الخطوط
يتكون ملف TTC من جدول TTC Header ودلائل الجدول وجداول OpenType متعددة. يجب العثور على رأس TTC في بداية الملف. يجب أن يكون هناك دليل جدول كامل لكل خط. يجب أن يكون تنسيق TableDirectory مشابهًا لما هو موجود في ملف ليس مجموعة. يتم حساب عدد الجدول في جميع الدلائل داخل ملف TTC من بداية ملف TTC.
تتم الإشارة إلى الجداول الموجودة في ملف TTC من خلال دليل الجدول للخطوط الخاصة بها. يجب أن تظهر بعض جداول OpenType عدة مرات ، مرة واحدة لكل خط مضاف في TTC. في حين يمكن مشاركة الجداول الأخرى بواسطة خطوط متعددة في ملف TTC.

### رأس TTC
يتوفر نسختان من جدول TTC Header حتى الآن:
- يستخدم الإصدار 1.0 لملفات TTC بدون توقيعات رقمية.
- يمكن استخدام الإصدار 2.0 لملفات TTC بتوقيعات رقمية أو بدونها.
فيما يلي جداول رأس TTC لكلا الإصدارين:

** إصدار رأس TTC 1.0: **

| النوع | الاسم | الوصف |
---|---|---|
| TAG | ttcTag | سلسلة معرف مجموعة الخط: 'ttcf' (تُستخدم للخطوط ذات مخططات CFF أو CFF2 بالإضافة إلى مخططات TrueType) |
| uint16 | majorVersion | الإصدار الرئيسي من رأس TTC ، = 1. |
| uint16 | MinorVersion | إصدار ثانوي من رأس TTC ، = 0. |
| uint32 | numFonts | عدد الخطوط في TTC |
| Offset32 | tableDirectoryOffsets [numFonts] | صفيف من الإزاحات إلى TableDirectory لكل خط من بداية الملف |

** إصدار رأس TTC 2.0: **

| النوع | الاسم | الوصف |
---|---|---|
| TAG | ttcTag | سلسلة معرف مجموعة الخط: 'ttcf' |
| uint16 | mainVersion | الإصدار الرئيسي من رأس TTC ، = 2. |
| uint16 | MinorVersion | إصدار ثانوي من رأس TTC ، = 0. |
| uint32 | numFonts | عدد الخطوط في TTC |
| Offset32 | tableDirectoryOffsets [numFonts] | صفيف من الإزاحات إلى TableDirectory لكل خط من بداية الملف |
| uint32 | dsigTag | علامة تشير إلى وجود جدول DSIG ، 0x44534947 ('DSIG') (خالية إذا لم يكن هناك توقيع) |
| uint32 | dsigLength | الطول (بالبايت) لجدول DSIG (فارغ إذا لم يكن هناك توقيع) |
| uint32 | dsigOffset | الإزاحة (بالبايت) لجدول DSIG من بداية ملف TTC (خالية إذا لم يكن هناك توقيع) |

## مراجع
* [ملف خط OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [تروتايب (ويكيبيديا)](https://en.wikipedia.org/wiki/TrueType)

