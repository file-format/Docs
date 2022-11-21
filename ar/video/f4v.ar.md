---
date: 2019-10-11
keywords: f4v , .f4v , تنسيق ملف f4v , تنسيق ملف .f4v , امتداد .f4v , امتداد f4v , تنسيق فيديو f4v , كيفية فتح ملفات f4v , ما هي ملفات f4v
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "تعرف على تنسيق ملف F4V وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات F4V وفتحها"
title: تنسيق ملف F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## ما هو ملف F4V؟ ##

F4V (Flash MP4 Video File) هو ملف فيديو محفوظ بامتداد .f4v. يعتمد على تنسيق ملف الوسائط الأساسي ISO (MPEG-4 الجزء 12). إنه مشابه جدًا لـ [MP4] (/ar/ video / mp4 /) ولهذا السبب يشار إليه أيضًا باسم Flash MP4 بشكل غير رسمي. [FLV] (/ar/ video / flv /) كانت لها قيود عند دفق محتويات H.264 / ACC مما أدى إلى قيام Adobe Systems بإنشاء تنسيق F4V الجديد. يمكن لبرنامج Flash Player تشغيل ملفات F4V منذ إصدار Flash Player 9 Update 3.

## هيكل ملفات F4V ##

يعتمد تنسيق ملف F4V على تنسيق ملف الوسائط الأساسي ISO (MPEG-4 الجزء 12) وهو مشابه جدًا لتنسيق MP4. للحصول على تفاصيل بشأن الهيكل ، يرجى الاطلاع على صفحة [MP4] (/ar/ video / mp4 /). يتمثل الاختلاف الرئيسي بين F4V و MP4 في تنسيقات البيانات الوصفية التي يمكن لـ F4V تخزينها. فيما يلي قائمة بتنسيقات البيانات الوصفية التي يدعمها تنسيق F4V.

- ** مربع العلامات **: أربعة مربعات علامات اختيارية إضافية (المصادقة ، العنوان ، dscp ، cprt) داخل مربع الفيلم (موف).
- ** XMP Metadata box **: يأتي هذا المربع بعد مربع Movie (moov) مباشرة. باستخدام هذا ، يمكن للملف توصيل بيانات XMP الأولية إلى فيلم SWF من خلال ActionScript.
- ** المربع الأول **: يظهر هذا المربع داخل مربع التعريف (Meta) ويمكن أن يحتوي على عدد من علامات البيانات الوصفية. يتم توفير أنواع البيانات المدعومة أدناه.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- ** مربع البيانات الوصفية لتتبع النص **: عينات النص (نص أو tx3g) داخل Media Databox (mdat). يمكن أن تحتوي على مربعات البيانات الوصفية التالية.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## مراجع ##

- [Flash Video - Wikipedia] (https://en.wikipedia.org/wiki/Flash_Video)

