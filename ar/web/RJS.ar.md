{
  "date" : "2021-05-24",
  "keywords" :["rjs" , "ملف" , "امتداد" , "تنسيق الملف" , "امتداد الملف" , "RJS" , "ملف جافا سكريبت روبي"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - ملف Ruby Javascript" ,
  "description":"تعرف على ما هو تنسيق ملف RJS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RJS وفتحها." ,
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-24"
}

## ما هو ملف RJS؟

الملف ذو الامتداد .rjs هو مزيج من كود Ruby و JavsScript الذي يسمح لمطوري Rails باستخدام Ruby لإنتاج كود JavaScript ديناميكي. يتم تضمين كود روبي في وظائف جافا ويتم تجميعه على خادم الويب الذي يتطلب تشغيل محرك روبي على الخادم. RJS مشابه لـ [RHTML](/ar/web/rhtml/) ؛ الاختلاف الوحيد هو أن الجانب الجانبي يحتوي على كود روبي في [HTML](/ar/web/html/) بينما يحتوي على كود روبي في وظائف جافا سكريبت.

## تنسيق ملف RJS

يتم ترميز ملفات RJS بنص عادي مثل أي لغة برمجة أو برمجة أخرى. عندما يطلب العميل مثل هذه الصفحة ، يتم تنفيذ كود روبي على الخادم ، ويتم إرجاع كود HTML وجافا سكريبت فقط إلى متصفح العميل. يتشابه بناء جملة ملف RJS مع تركيبة بناء جملة Ruby و JavaScript بحيث يتم تضمين كود Ruby فقط في وظائف JavaScript.

### مثال RJS

يوضح المثال التالي رمز Ruby البسيط بشكل مستقل ثم يتم تضمينه في وظيفة JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
وفيما يلي RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## مراجع

* [RJS](https://github.com/makevoid/rjs)

