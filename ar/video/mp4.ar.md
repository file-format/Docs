---
date: 2019-10-11
keywords: MP4 , ملف , امتداد , تنسيق , تنسيق فيديو , MPEG-4
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "تعرف على تنسيق ملف MP4 وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MP4 وفتحها."
title: تنسيق ملف MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## ما هو ملف MP4؟ ##

MP4 (اختصار MPEG-4 الجزء 14) هو تنسيق ملف يعتمد على ISO / IEC 14496-12: 2004 الذي يعتمد على تنسيق ملف QuickTime ولكنه يحدد رسميًا دعم واصفات الكائنات الأولية (IOD) وميزات MPEG الأخرى. يتم استخدامه في الغالب لتخزين الفيديو والصوت ولكن يمكن استخدامه أيضًا لتخزين الترجمة والصور الثابتة. يتم تخزين ملفات MP4 بامتداد .mp4. MP4 هو معيار دولي للترميز الصوتي والمرئي. على غرار معظم تنسيقات الحاويات الحديثة ، يدعم MP4 البث عبر الإنترنت. نظرًا للضغط العالي المستخدم في MP4 ، تكون الملفات الناتجة أصغر حجمًا مع الاحتفاظ بالجودة الأصلية تقريبًا.

## نبذة تاريخية ##

تم تطوير مواصفات MP4 بواسطة Moving Picture Experts Group (MPEG) واستندت إلى تنسيق QuickTime [MOV] (/ar/ video / mov /) الذي تم نشره في عام 2001. الإصدار الأول (ISO / IEC 14496-1: 2001) من MP4 كانت مراجعة MPEG-4 الجزء 1: مواصفات الأنظمة المنشورة في 1999. تم تعميم تنسيق ملف MP4 على تنسيق ملف الوسائط الأساسي ISO / IEC 14496-12: 2004 الذي حدد الهيكل العام لملفات الوسائط المستندة إلى الوقت. نتيجة لذلك ، يتم استخدامه كأساس لتنسيقات الملفات الأخرى.

## هيكل ملفات MP4 ##

MP4 هو ملف حاوية قابل للتوسيع ، مما يعني أنه لا يحدد بنية صارمة ويسمح بالهيكل والتسلسل الهرمي المخصص لكل نوع من أنواع الوسائط. تنقسم البيانات الموجودة في ملف MP4 إلى قسمين ، الأول يحتوي على البيانات المتعلقة بالوسائط والثاني يحتوي على البيانات الوصفية. تحتوي بيانات الوسائط على صوت أو فيديو وتشير البيانات الوصفية إلى أعلام للوصول العشوائي والطوابع الزمنية وما إلى ذلك.
يشار عادةً إلى الهياكل في MP4 باسم الذرات أو الصناديق. الحد الأدنى لحجم الذرة هو 8 بايت (تحدد أول 4 بايت الحجم وتحدد 4 بايت التالية النوع). فيما يلي قائمة بذرات مستوى الجذر الموجودة في ملفات MP:

- ** ftyp **: يحتوي على نوع الملف والوصف وهياكل البيانات الشائعة المستخدمة.
- ** pdin **: يحتوي على معلومات تحميل / تنزيل الفيديو التدريجي.
- ** موف **: حاوية لجميع البيانات الوصفية للفيلم.
- ** moof **: حاوية بها أجزاء فيديو.
- ** mfra **: الحاوية ذات الوصول العشوائي إلى جزء الفيديو
- ** mdat **: حاوية بيانات للوسائط.
- ** stts **: جدول عينة إلى وقت.
- ** stsc **: جدول من عينة إلى قطعة.
- ** stsz **: أحجام العينات (تأطير)
- ** meta **: الحاوية التي تحتوي على معلومات البيانات الوصفية.

فيما يلي قائمة بذرات المستوى الثاني المستخدمة في MP4:

- ** mvhd **: يحتوي على معلومات رأس الفيديو مع التفاصيل الكاملة للفيديو.
- ** trak **: حاوية بمسار فردي.
- ** udta **: الحاوية مع المستخدم وتتبع المعلومات.
- ** iods **: واصف ملف MP4

## مراجع ##

- [MP4 - ويكيبيديا] (https://en.wikipedia.org/wiki/MPEG-4_Part_14)
