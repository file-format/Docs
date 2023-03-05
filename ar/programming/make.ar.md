{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"Make File - Xcode Makefile Script File",
  "description":"تعرف على تنسيق XCode MakeFile وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MakeFile وفتحها." ,
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}


## ما هو ملف MAKE؟

ملف MAKE هو ملف نصي XCode ينظم تجميع التعليمات البرمجية. يتم استخدامه لتجميع وربط البرامج من ملفات التعليمات البرمجية المصدر المتعددة. يساعد هذا في تحديد أجزاء التطبيق الكبير المطلوب إعادة تجميعها عندما يحتاج التطبيق إلى التحديث. اجعل الملفات تستخدم سلسلة من الإرشادات للتشغيل بناءً على الملفات التي تم تغييرها.

## جعل مثال تنسيق الملف

يتم تنفيذ المحتويات التالية باستخدام الأداة المساعدة Make والمخرجات كما يلي.

```
hello:
	echo "hello world"
```
** جعل الإخراج **

```
$ make
echo "hello world"
hello world
```

## مراجع
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [دليل الكائن C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

