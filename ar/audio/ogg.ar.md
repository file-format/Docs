---
date: 2019-12-13
keywords: ogg , تنسيق ملف ogg , امتداد .ogg , تنسيق صوت ogg
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "تعرف على تنسيق ملف OGG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات OGG وفتحها."
title: ملف OGG - ملف صوتي Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## ما هو ملف OGG؟

OGG هو ملف صوتي مضغوط Ogg Vorbis يتم حفظه بامتداد .ogg. تُستخدم ملفات OGG لتخزين البيانات الصوتية ويمكن أن تتضمن معلومات الفنان والمسار والبيانات الوصفية أيضًا. OGG هو تنسيق حاوية مجاني ومفتوح تحتفظ به مؤسسة Xiph.Org Foundation.

## تاريخ موجز لتنسيق ملف OGG

بدأ مشروع Ogg كجزء من مشروع أكبر في عام 1993 وتم تسميته Squish ولكن بسبب علامة تجارية موجودة ، تمت إعادة تسميته إلى OggSquish. تم وصفها بأنها محاولة لإنشاء تنسيق صوتي مضغوط مرن لتطبيقات الصوت الحديثة. تم فصل مرجع OGG عن Vorbis في 2 سبتمبر 2000.

تم إنشاء OGM في عام 2002 بسبب نقص دعم الفيديو الرسمي في OGG. سمح هذا بتضمين فيديو من إطار عمل Microsoft DirectShow في غلاف مستند إلى OGG. بحلول عام 2006 ، كان OGG مدعومًا من قبل العديد من محركات ألعاب الفيديو وكان يستخدم بشكل شائع لتشفير المحتوى المجاني. بدأت مؤسسة البرمجيات الحرة حملة في 15 مايو 2007 لزيادة استخدام Vorbis كبديل ممتاز لـ MP3. بحلول 30 يونيو 2009 ، كان OGG هو تنسيق الحاوية الوحيد الذي يدعمه تطبيق HTML5 لمتصفح Firefox 3.5.

## تنسيق ملف OGG

يتكون تنسيق OGG من أجزاء من البيانات. كل جزء يسمى صفحة Ogg. تبدأ كل صفحة بـ "OggS" لتحديد تنسيق Ogg. يحتوي العنوان على الرقم التسلسلي ورقم الصفحة الذي يعرّف كل صفحة كجزء من سلسلة. تتكون الصفحة من المكونات التالية.

- **رأس الصفحة**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| بت | القيمة | الوصف |
| --- | --- | --- |
| 0 | 0x01 | يشير إلى أن الحزمة الأولى من الصفحة هي استمرار للحزمة السابقة في تدفق البت المنطقي. |
| 1 | 0x02 | يشير إلى أن هذه الصفحة هي الأولى في تدفق البت المنطقي. |
| 2 | 0x04 | يشير إلى أن هذه الصفحة هي الأخيرة في تدفق البت المنطقي. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- ** البيانات الوصفية **: VorbisComment هي الآلية الأكثر دعمًا لتخزين البيانات الوصفية. تشمل الآليات الأخرى ما يلي:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## مراجع ##

- [OGG - ويكيبيديا] (https://en.wikipedia.org/wiki/Ogg)

