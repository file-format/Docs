{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف BML - ملف لغة ترميز الفول" ,
  "description":"تعرف على تنسيق ملف BML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات BML وفتحها." ,
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-08-12"
}

## ما هو ملف BML؟

الملف بامتداد .bml هو ملف Bean Markup Language يخزن فئات Java لدعم تطبيقات Java. يسمح هذا بالوصول إلى كائنات وطرق Java ، ولا يحتاج إلى إنشاء وظائف جديدة باستخدام فئات Java. يحدد كيفية اتصال المكونات ببعضها البعض لأداء مهام مفيدة. تم تطوير BML بواسطة IBM alphaWorks لوصف العلاقات بين الهياكل والمكونات. يمكن فتح ملفات BML وعرضها باستخدام أي محرر نصوص مثل متصفحات الويب و Microsoft Notepad و Notepad ++.

## تنسيق ملف BML

قدم موقع ويب IBM alphaworks عمليتي تطبيق لـ BML. التنفيذ الأول هو مترجم يقوم "بتشغيل" نص BML لإنشاء التسلسل الهرمي المطلوب للفول. التنفيذ الثاني هو مترجم يقوم بترجمة أي نص برمجي BML إلى كود Java خالٍ من الانعكاس. هذا مفيد بمعنى أنه يسمح بالتقاط البنية بين المكونات للتطبيق باستخدام لغة مصممة لهذا الغرض المحدد مع القدرة الإضافية على تجميعها في كود Java "عادي".

## علامات BML

فيما يلي شرح لبعض العلامات المستخدمة في لغة BML:

### ال<bean> بطاقة شعار:

ال<bean> يُستخدم العنصر لإنشاء حبوب جديدة أو للبحث عن حبوب بالاسم. ال<bean> العلامة بالتنسيق:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
يرتبط "المعرف" في العلامة بسجل الكائن لـ JavaBean.

### ال<string> بطاقة شعار

هناك طريقتان لاستخدام علامة السلسلة:

1. لإنشاء سلسلة غير فارغة:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. لإنشاء سلسلة فارغة:

```
<string/>
```
## مراجع

* [الرسائل الموجهة للكائنات باستخدام XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [لغة الترميز المادية](http://web.mit.edu/mecheng/pml/standards.htm)
* [The Bean Markup Language](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

