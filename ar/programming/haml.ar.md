{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف HAML - ملف رمز مصدر Haml" ,
  "description":"تعرف على تنسيق ملف HAML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف HAML وفتحه." ,
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-04-07"
}

## ما هو ملف HAML؟

ملف HAML هو ملف لغة ترميز HTML يحتوي على كود مصدر مكتوب بلغة [Haml](https://haml.info/). يمكن استخدامه كبديل لـ ERB (نصوص قوالب روبي). يحتوي ملف HAML على شفرة مصدر نموذجية لتوليد HTML لمستند ويب. يمكن استبدال ملفات ERB ببساطة عن طريق استبدال هذه الملفات في مجلد التطبيق / العروض إلى Haml عن طريق تغيير امتداد الملف. يمكن فتح ملفات HAML باستخدام أي محرر نصوص مثل Microsoft Notepad و Notepad ++ و Apple TextEdit و

## تنسيق ملف HAML

ملفات HAML هي ملفات مصدر محفوظة على القرص كملفات نصية عادية. يحتوي على رمز مكتوب بلغة HAML. يستبدل HAML العلامات ** <> ** بعلامة **٪ ** لجعل الكود أبسط وأسهل. يمكن استبدال ملفات ERB بواسطة HAML كما هو موضح في المثال البسيط التالي.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### مثال HAML

فيما يلي مثال على Hello World مثال على HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
مما يؤدي إلى إخراج HTML التالي.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## مراجع

* [HAML - Github](https://github.com/haml/haml)

