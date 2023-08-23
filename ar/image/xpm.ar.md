{
  "date" : "2019-10-11",
  "keywords" :["ملف xpm" , "تنسيق ملف xpm" , "ما هو ملف xpm" , "ملف" , "مثال xpm" , "امتداد ملف xpm" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف XPM - X PixMap" ,
  "description":"تعرف على تنسيق ملف XPM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XPM وفتحها." ,
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف XPM؟

الملف ذو الامتداد .xpm هو تنسيق ملف صورة تم استخدامه بواسطة نظام X Windows. وهو يدعم وحدات البكسل الشفافة وعادة ما يستهدف إنشاء خرائط بكسل للأيقونات. وهو يدعم البيانات أحادية اللون ، وتدرج الرمادي ، واللون pixmap. تم تصميمها لتكون قابلة للتحرير يدويًا ويمكن تضمينها في كود [C](/ar/programming/c/). لهذا الغرض ، تكون ملفات XPM بتنسيق ملف نصي عادي وتتبع بناء جملة لغة البرمجة C. يمكن فتح ملفات XPM باستخدام مجموعة متنوعة من تطبيقات عرض الصور مثل
CorelDRAW Graphics Suite 2020 و Corel PaintShop Pro و IrfanView و Canvas X.

## تنسيق ملف XPM

يستخدم تنسيق ملف XPM بناء جملة C من أجل دمجها في برامج C و C ++. يتكون من الأقسام الستة التالية.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

المقاطع هي في الواقع مجموعة من السلاسل على النحو التالي.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
فيما يلي تفاصيل كل قسم.

"<Values> "- هذا القسم عبارة عن سلسلة تحتوي على أربعة أو ستة أعداد صحيحة في الأساس 10 وتتوافق مع:

* عرض وارتفاع خريطة بيكسل
* عدد الألوان
* عدد الأحرف لكل بكسل
* إحداثيات نقطة اتصال اختيارية وعلامة XPMEXT

"<Colors> "- يحتوي هذا القسم على عدد من الخيوط يساوي عدد الألوان. كل سلسلة كالتالي:

""
<chars>{<key><color> } +
""
"<Pixels> "- هذا القسم مكون من<height> سلاسل و<width> \ *<chars_per_pixel> الشخصيات. كل<chars_per_pixel> يجب أن تكون سلسلة الطول إحدى المجموعات المحددة مسبقًا في ملف<Colors> الجزء.

"<Extension> "- يجب تسمية قسم الامتداد ، إذا لم يكن فارغًا ، في<Values> الجزء. قد تتكون من عدة<Extension> الأقسام الفرعية التي قد تكون من النوعين التاليين:

* سلسلة واحدة مستقلة تتكون على النحو التالي: XPMEXT<extension-name><extension-data>
* أو كتلة مكونة من عدة سلاسل: XPMEXT<extension-name><related extension-data composed of several strings>

## مراجع

* [XPM - ويكيبيديا](https://en.wikipedia.org/wiki/X_PixMap)
* [دليل XPM](http://www.xfree86.org/current/xpm.pdf)

