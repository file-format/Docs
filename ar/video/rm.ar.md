---
date: 2019-10-11
keywords: rm , .rm , تنسيق ملف rm , تنسيق ملف .rm , امتداد .rm , تنسيق ملف RealMedia
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "تعرف على تنسيق ملف RM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RM وفتحها."
title: تنسيق ملف RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## ما هو ملف RM؟ ##

RealMedia هو تنسيق حاوية وسائط متعددة مملوك تم تطويره بواسطة RealNetworks يستخدم الامتداد .rm. يتم استخدامه مع مزيج من [RealAudio (RA)](/ar/ audio / ra /) و [RealVideo (RV)](/ar/ video / rv /) للبث عبر الإنترنت. هذه التدفقات ذات معدل بت ثابت. بالنسبة لمعدل البت المتغير ، طورت RealNetworks تنسيق RealMedia Variable Bitrate (RMVB). يعد RealMedia مناسبًا لبث المحتوى عبر الإنترنت ويمكن استخدامه لبث البث التلفزيوني المباشر على سبيل المثال.

## هيكل ملف RealMedia ##

يتكون ملف RealMedia من سلسلة من الأجزاء ، لكل منها الهيكل التالي:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

فيما يلي أنواع الأجزاء الموجودة في ملف RealMedia:

- ** رأس ملف RealMedia (.RMF) **: يجب أن يكون هذا الجزء الأول في ملف RealMedia. يوجد مقطع RMF واحد فقط في ملف واحد. يحتوي على معلومات حول عدد الرؤوس.
- ** عنوان خصائص الملف (PROP) **: يحتوي على معلومات حول الخصائص العامة لملف RealMedia. يوجد جزء واحد فقط من هذا النوع في كل ملف RealMedia.
- ** رأس خصائص الوسائط (MDPR) **: تحتوي هذه القطعة على معلومات حول خصائص الدفق. يحتوي على معلومات حول نوع الدفق وبرنامج الترميز المستخدم. يوجد جزء MDPR واحد لكل دفق في الملف.
- ** رأس وصف المحتوى (CONT) **: تحتوي هذه القطعة على معلومات نصية مثل العنوان أو مؤلف المحتوى الموجود في ملف RealMedia. هذا الجزء لأغراض إعلامية فقط.
- ** رأس البيانات (DATA) **: تحتوي هذه القطعة على مجموعة من حزم البيانات.
- ** رأس الفهرس (INDX) **: تأتي هذه القطعة بعد كل أجزاء البيانات وتحتوي على مدخلات الفهرس. يمكن أن يحتوي الملف الواحد على أكثر من قطعة INDX.

## تنسيقات الصوت والفيديو المدعومة ##

### تنسيقات الصوت ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: برنامج RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: سيبرو
- طباخ: طبخ
- atrc: ATRAC3
- رالف: RealAudio Lossless Format
- رااك: LC-AAC
- راكب: HE-AAC

### تنسيقات الفيديو ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263 + ، RV20
- RV30: السلائف H.264
- RV40: السلائف H.264 ، RV40
- RVTR: H.263 + (RV20)

## مراجع ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

