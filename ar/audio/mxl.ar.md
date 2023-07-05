---
date: 2022-03-20
keywords: mxl , تنسيق ملف Musepack , امتداد mxl
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "تعرف على تنسيق ملف MXL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MXL وفتحها."
title: تنسيق ملف MXL - ملف MusicXML مضغوط
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## ما هو ملف MXL؟

ملف MXL هو الشكل المضغوط لتنسيق ملف MusicXML وهو تنسيق قياسي مفتوح لتبادل الموسيقى الرقمية. تكون ملفات MusicXML ذات النص العادي كبيرة الحجم وقد تأثر استخدام مثل هذه الملفات كتنسيق توزيع الورقة بحجم الملف الكبير. تمت معالجة هذه المشكلات باستخدام [MusicXML](https://www.musicxml.com/) 2.0 من خلال تقديم تنسيق ملف MXL الذي يضغط الملفات بدرجة كافية لتقليل حجم الملف المماثل لحجم ملفات MIDI الأصلية. نوع الوسائط الموصى به لملفات MXL هو application / vnd.recordare.musicxml.

## تنسيق ملف MXL

يتم تخزين ملفات MXL كملفات [ZIP](/ar/compression/zip/) مضغوطة [XML](/ar/web/xml/) بامتداد ملف .mxl. يتم ضغط ملفات MXL باستخدام خوارزمية DEFLATE كما هو محدد في [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### هيكل ملف MXL

يحتوي كل ملف MXL على تنسيق XML مستند إلى ZIP ويجب أن يحتوي على ملف META-INF / container.xml يصف نقطة البداية لإصدار MusicXML من الملف. لا يوجد ملف .xsd مطابق معرّف لتنسيق ملف MXL.

يحتوي ملف Container.xml البسيط على محتويات على النحو التالي. هذا المثال مأخوذ من ملف Dichterliebe01.mxl المتاح على موقع ويب MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
في هذا المثال ، فإن ملف<container> العنصر هو عنصر المستند. ال<rootfiles> يمكن أن يحتوي العنصر على واحد أو أكثر<rootfile> العناصر ، مع الأول<rootfile> عنصر يصف جذر MusicXML. يتم استخدام ملف MusicXML كملف<rootfile> قد يملك<score-partwise> و<score-timewise> ، أو<opus> كعنصر وثيقته.

## مراجع

* [ملفات MXL المضغوطة](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

