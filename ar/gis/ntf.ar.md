{
  "date" : "2021-07-28",
  "keywords" :["ntf file", "ntf file format", "what is a ntf file", "file", "ntf example", "ntf file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - ملفات تنسيق النقل الوطني" ,
  "description":"تعرف على تنسيق ملف NTF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات NTF وفتحها." ,
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2021-07-28"
}

## ما هو ملف NTF؟
تسمى الملفات ذات الامتداد .ntf ملفات ** National Transfer Format (NTF) ** Files ؛ تستخدم في الغالب من قبل هيئة مسح الذخائر في المملكة المتحدة (OS) ؛ على وجه التحديد لنقل البيانات الجغرافية المكانية. تدار من قبل مؤسسة المعايير البريطانية. لقد أصبح تنسيق النقل القياسي للبيانات الرقمية لمسح الذخائر. يحتفظ إسقاط الشبكة الوطنية في المملكة المتحدة ، وهو نوع من Transverse Mercator ، بجميع المعلومات ذات المرجعية الجغرافية لملفات NTF.

## تنسيق ملف NTF
تنسيق ملف NTF مملوك لشركة Ordnance Survey في المملكة المتحدة ؛ بدعم من مكتبة GDB للاستيراد. الإصدار الحالي من تنسيق ملف NTF هو 2.0. تم تقديم تنسيق الملف هذا لمعالجة قيود مقطع متجه ** PCIDSK ** الذي يحتوي على حقل سمة واحد فقط لكل بنية ، ولكن هناك مجموعة متنوعة من السمات التي يمكن استخراجها باستخدام بيانات المتجه. للالتفاف حول تنسيق ملف NTF يتكون من جزأين. يتكون كل مقطع من نفس المتجهات ، ولكن بسمات مختلفة. يحتوي الجزء الأول من ملف متجه NTF على المتجهات مع رقم رمز الميزة كسمة. يحتوي المقطع الثاني على المتجهات مع القيمة كسمة.

### تنسيق نظام الإحالة
تمثل مكتبة GDB البيانات النقطية والمتجهية بخصائص إسقاط TM المناسبة:

- خط الطول المرجعي: 49.0
- خط العرض المرجعي: 2.0
- الشرق الكاذب: 400000
- الشمال الكاذب: -100000
- مقياس: 0.9996012717
- الإليبسويد: Airy 1830 (E009)
لا يتوفر دعم لتحديث ملفات NTF أو كتابتها ، ولا يمكن ربط ملفات DTM بها.

### مثال Ogrinfo
المثال التالي يستخدم ** ogrinfo ** على ملف NTF لاسترداد أرقام الطبقة:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## مراجع

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [رسم خرائط الويب - مصور بواسطة تايلر ميتشل](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

