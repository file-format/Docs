{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - ملف مرجعي ماكرو Microsoft Office" ,
  "description":"تعرف على ملف MSO وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MSO وفتحها." ,
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
} ,
  "lastmod" : "2022-03-12"
}

## ما هو ملف MSO؟

ملف MSO هو تنسيق ملف حاوية بيانات يتم إنشاؤه عند إرسال رسالة HTML باستخدام Microsoft Outlook. يحدث هذا في الغالب مع تطبيقات Microsoft Office 2000. في معظم الحالات ، يتم إرفاق رسالة البريد الإلكتروني باسم ملف ** Oledata.mso **. يمكن لمستلم البريد الإلكتروني ، عند فتح مثل هذا البريد الإلكتروني ، عرض الملف بشكل صحيح حتى إذا لم يكن لديهم نفس البرنامج المثبت. تشير ملفات MSO إلى [تنسيق ملف مستند Microsoft المركب (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## تنسيق ملف Microsoft MSO

يتم حفظ ملفات MSO بتنسيق Microsoft Compound Document File Format (MCDF) والذي يُعرف أيضًا باسم تنسيق ملف تنفيذ ملف ثنائي مركب للتخزين المركب لربط الكائنات وتضمينها (OLE) أو نموذج كائن المكون (COM).

### هيكل تنسيق ملف MSO

هيكل تنسيق الملف الداخلي لتنسيق ملف MSO محدد جيدًا في [الهياكل](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) قسم وثائق MCDF. يدير جدول تخصيص الملفات (FAT) تخصيص القطاعات وسلاسل القطاعات. يحتوي على مجموعة من أرقام القطاعات 32 بت. يمثل كل فهرس في المصفوفة رقم قطاع بينما تمثل قيمته القطاع التالي في السلسلة أو قيمة خاصة.

## مراجع

* [التخزين المهيكل COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [تنسيق ملف مستند Microsoft المركب (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

