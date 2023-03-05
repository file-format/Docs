---
date: 2022-01-06
keywords: vtt , .vtt , تنسيق ملف vtt , تنسيق ملف .vtt , امتداد vtt , امتداد vtt
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "تعرف على ملف .vtt وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VTT وفتحها."
title: تنسيق ملف VTT - ملف مسارات نص فيديو ويب
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## ما هو ملف VTT؟

ملف VTT هو ملف نصي يحتوي على معلومات لعرض مسارات النص المحددة بوقت (مثل الترجمة أو التسميات التوضيحية) باستخدام تنسيق Web Video Text Tracks (WebVTT). تتضمن مسارات النص المحددة بوقت معلومات مثل الترجمة أو التسميات التوضيحية. الغرض من ملف VTT هو إضافة تراكبات نصية إلى ملف<video> . التنسيق مشابه إلى حد ما لملفات SRT. يتم ترميز الملفات النصية المستندة إلى WebVTT باستخدام UTF-8. يحتوي ملف VTT على معلومات مثل الترجمة والأوصاف والتعليقات التوضيحية والأوصاف والفصول والبيانات الوصفية. نظرًا لكونها ملفات نصية عادية ، يمكن فتح ملفات VTT باستخدام برامج تحرير النصوص مثل Microsoft Notepad و Apple TextEdit و Notepad ++.

## تنسيق ملف VTT - مزيد من المعلومات

تستخدم ملفات VTT تنسيق ملف WebVTT لحفظ معلومات مسارات النص المتسلسل. يتكون كل مسار نصي محدد بوقت من سطر واحد أو عدة أسطر ، تُعرف أيضًا باسم "جديلة" كما هو موضح في المثال التالي.

### مثال ملف VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### بنية ملف VTT

فيما يلي متطلبات الهيكل لملف VTT.

* علامة اختيارية لترتيب البايت (BOM).
* السلسلة "WEBVTT".
* رأس نص اختياري على يمين WEBVTT.
* سطر فارغ ، أي ما يعادل سطرين جديدين متتاليين.
* صفر أو أكثر من الإشارات أو التعليقات.
* صفر أو أكثر من الأسطر الفارغة.

## مراجع

* [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

