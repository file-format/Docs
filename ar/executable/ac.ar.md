{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "تنسيق ملف AC - ملف البرنامج النصي Autoconf",
  "title" : "تنسيق ملف AC - ملف البرنامج النصي Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## ما هو ملف AC؟

ملف AC هو ملف البرنامج النصي Autoconf. **Autoconf** عبارة عن حزمة قابلة للتوسيع من وحدات الماكرو M4 التي تنتج نصوص برمجية لتكوين حزم التعليمات البرمجية المصدرية للبرامج تلقائيًا. يمكن لهذه البرامج النصية تكييف الحزم مع أنواع كثيرة من الأنظمة المشابهة لنظام UNIX دون تدخل يدوي من المستخدم. يقوم Autoconf بإنشاء برنامج نصي لتكوين حزمة من ملف قالب يسرد ميزات نظام التشغيل التي يمكن أن تستخدمها الحزمة، في شكل استدعاءات ماكرو M4.

Producing configuration scripts using Autoconf requires GNU M4. يجب عليك تثبيت GNU M4 (الإصدار 1.4.6 على الأقل، على الرغم من أنه يوصى باستخدام 1.4.13 أو أحدث) قبل تكوين Autoconf، حتى يتمكن البرنامج النصي لتكوين Autoconf من العثور عليه. تعتبر نصوص التكوين التي ينتجها Autoconf مستقلة بذاتها، لذا لا يحتاج مستخدموها إلى Autoconf (أو GNU M4).

## كيفية فتح ملف AC؟

يشير AC إلى التكوين التلقائي. إنه برنامج نصي تم إنشاؤه بواسطة GNU Autoconf والذي يمكّن من تكييف كود مصدر البرنامج مع أنظمة مختلفة تشبه Posix عن طريق اختبار الميزات الضرورية في الحزمة. يسمى البرنامج النصي ملف AC.

## مكونات الأدوات الآلية الرئيسية

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools عبارة عن مجموعة من الحزم المترابطة والتي، عند استخدامها معًا، تزيل الكثير من الصعوبات التي ينطوي عليها إنشاء البرامج المحمولة. تُستخدم هذه الأدوات، جنبًا إلى جنب مع عدد قليل نسبيًا من ملفات الإدخال المقدمة من المنبع، لإنشاء نظام إنشاء الحزمة.

**نظرة عامة أساسية حول كيفية توافق مكونات الأدوات التلقائية الرئيسية معًا.**

!{{رابط تشعبي1}}

في إعداد بسيط:

- يقوم برنامج `autoconf` بإنتاج نص تكوين من `configure.in` أو `configure.ac`.
- يقوم برنامج automake بإنتاج ملف Makefile.in من ملف Makefile.am.
- يتم تشغيل البرنامج النصي configure لإنتاج ملف Makefile واحد أو أكثر من ملفات Makefile.in.
- يستخدم برنامج make ملف Makefile لتجميع البرنامج.

## مراجع
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [أساسيات الأدوات التلقائية](https://devmanual.gentoo.org/general-concepts/autotools/index.html)