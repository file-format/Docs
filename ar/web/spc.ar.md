---
date: 2021-07-05
keywords: spc , .spc , تنسيق ملف spc , كيفية فتح ملفات spc , ملف شهادة ناشر البرنامج
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - ملف شهادة ناشر البرنامج
linktitle: SPC
description: "تعرف على ما هو تنسيق ملف SPC وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SPC وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## ما هو ملف SPC؟

الملف بامتداد .spc هو ملف شهادة أمان رقمي تم إنشاؤه بتنسيق PKCS # 7. العديد من التطبيقات ، قم بإنشاء ملفات الشهادات هذه لتبادل آمن للمعلومات. قليل من هذه التطبيقات تشمل OpenSSL وتطبيق Signcode.exe المضمن في Microsoft .NET Framework. مثل ملفات الشهادات الأخرى مثل [.cer] (/ar/ web / cer /) و [.p7c] (/ar/ web / p7c /) و [. ssp] (/ar/ web / ssp /) ، تحتوي ملفات SPC على المفتاح العام المعلومات المشفرة بمفتاح خاص. يمكن مشاركة هذا المفتاح العام مع المستخدمين علنًا مع الحفاظ على سرية المفتاح الخاص.

## تنسيق ملف SPC - مزيد من المعلومات

يتم حفظ ملفات SPC على القرص كملفات ثنائية يمكن فتحها في أي محرر نصوص ولكنها ليست قابلة للقراءة البشرية. تستند هذه إلى أحدث إصدار من PKCS # 7 المتوفر [RFC 2315] (https://datatracker.ietf.org/doc/html/rfc2315).

## مراجع

* [PKCS 7] (https://en.wikipedia.org/wiki/PKCS_7)
* [مرجع SSP] (https://scalate.github.io/scalate/documentation/ssp-reference.html)

