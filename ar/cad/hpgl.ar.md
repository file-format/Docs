{
  "date" : "2020-07-28",
  "keywords" :["HPGL" , "تنسيق الملف" , "فتح" , "قراءة" , "إنشاء" , "CAD"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف HPGL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات HPGL وفتحها." ,
  "title" :"تنسيق ملف HPGL - تعلم من خبراء تنسيق الملفات!" ,
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
} ,
  "lastmod" : "2020-07-28"
}

## ما هو ملف HPGL؟

يحتوي ملف HPGFL (Hewlett-Packard Graphics Language) على مجموعة تعليمات للتحكم في الراسمة بواسطة HP. يستخدم الراسمون من HP هذا الملف لرسم وطباعة المحتوى المتجه والنقطي على الورق.

### قيادة HPGL

يتكون أمر HPGL مما يلي.
* قسم أوامر الأبجدية المكونة من حرفين
* قسم المعلمة
* قسم المنهي

يجب تقسيم كل معلمة في الملف بفاصل في حالة وجود معلمات متعددة.

### مثال قيادة HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### نظام الإحداثيات

تتألف أنظمة الإحداثيات من مؤشرات قياس ثنائية الأبعاد لتحديد موقع أي موقع محدد. يستخدم HPGL كلاً من إحداثيات الراسمة ونظام إحداثيات المستخدم لهذا الغرض.

#### نظام تنسيق الراسمة

يستخدم نظام التنسيق هذا لرسم الرسومات بناءً على حركة الراسمة. وحدة XY النموذجية ذات الحد الأدنى لحركة الراسمة هي 0.025 مم. النطاق المحتمل لرسم التغييرات مع أنواع الراسمة.

#### نظام إحداثيات المستخدم

يمكن إعداد نظام إحداثيات محدد من قبل المستخدم باستخدام المقياس والأصل. يتم تحويلها إلى إحداثيات الراسمة باستخدام الأمر IP وأمر SC. تُستخدم إحداثيات نظام الراسمة افتراضيًا إذا لم يتم تنفيذ هذا التحويل.

## تنسيق ملف HPGL
تكون ملفات HPGL بتنسيق ASCII (ملف نصي) وتبدأ ببعض أوامر الإعداد. يقوم هذا بإعداد معلمات معينة للراسم للتخطيط. يبدو ملف HPGL النموذجي على النحو التالي.

| الأمر | المعنى
---|---|
| IN؛ | تهيئة ، بدء عمل تخطيطي |
| IP ؛ | اضبط نقاط القياس (P1 و P2) على مواقعها الافتراضية |
| SP1 ؛ | حدد القلم 1 |
| PU0،0؛ | ارفع القلم لأعلى وانتقل إلى نقطة البداية للإجراء التالي |
| PD100،0،100،100،0،100،0،0 ؛ | ضع القلم لأسفل وانتقل إلى المواقع التالية (ارسم مربعًا حول الصفحة) |
| PU50،50؛ | Pen Up وانتقل إلى إحداثيات X و Y 50،50 |
| CI25 ؛ | ارسم دائرة نصف قطرها 25 |
| SS ؛ | حدد مجموعة الأحرف القياسية |
| DT *، 1؛ | اضبط مُحدِّد النص على علامة النجمة ولا تطبعه (1 ، الذي يعني "صواب") |
| PU20،80 ؛ | ارفع القلم وانتقل إلى 20،80 |
| LBHello World * ؛ | ارسم تسمية |

## مراجع
* [HPGL بواسطة Wikipedia] (https://en.wikipedia.org/wiki/HP-GL)
* [دليل مرجعي HPGL] (https://www.isoplotec.co.jp/HPGL/eHPGL.htm)
