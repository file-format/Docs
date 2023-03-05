{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف PYC وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PYC وفتحها." ,
  "title" :"تنسيق ملف PYC- ملف مترجم Python" ,
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2022-05-09"
}

## ما هو ملف PYC؟

ملف PYC هو ملف إخراج مجمع تم إنشاؤه من شفرة المصدر المكتوبة بلغة برمجة Python. عند تشغيل ملف PY باستخدام مترجم Python ، يتم تحويله إلى رمز بايت للتنفيذ. في الوقت نفسه ، يتم أيضًا حفظ الرمز الثانوي المترجم كملف .pyc لإعادة استخدامه من ذاكرة التخزين المؤقت في وقت لاحق إذا كان ذلك ممكنًا.

## هيكل تنسيق ملف PYC

ملفات PYC موجودة في رمز بايت ولا تتوفر مواصفات تنسيق الملفات الخاصة بها للجمهور. ومع ذلك ، يُظهر التحقيق من قبل بعض المصادر أن [بنية ملف PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc٪20file٪20is٪20a٪20binary،A٪ 20marshalled٪ 20code٪ 20object.) يتكون من:

* `4 بايت سحري numbe`r - ببساطة 2 بايت تتغير مع كل تغيير في كود التنظيم ، ثم 2 بايت من 0d0a.
* "طابع زمني لتعديل أربعة بايت" - طابع زمني لتعديل نظام Unix للملف المصدر الذي أنشأ ملف .pyc ، بحيث يمكن إعادة تجميعه إذا تغير المصدر.
* `A marshalled code object` - ناتج marshal.dump لكائن التعليمات البرمجية الناتج عن تجميع الملف المصدر.

## مراجع

* [بنية ملفات .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc٪20file٪20is٪20a٪20binary،A٪20marshalled٪20code٪20object.)

