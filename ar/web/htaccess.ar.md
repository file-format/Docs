{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف HTACCESS - تنسيق ملف Apache HTACCESS" ,
  "description" :"دليل تنسيق الملف الخاص بك لمعرفة ما هو ملف HTACCESS" ,
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف HTACCESS؟

ملف HTACCESS هو ملف تكوين Apache يوفر آلية للسماح بتغييرات التكوين لمجلدات / أدلة مختلفة لموقع ويب. يتضمن توجيهات التكوين التي تنطبق على الدليل والأدلة الفرعية.

ينفذ ملف HTACCESS عددًا من عمليات التحقق مثل تحديد صفحة الفهرس الخاصة بموقع ويب ، أو سرد صفحة الخطأ 404 (لم يتم العثور على الصفحة) ، أو إجراء عمليات إعادة توجيه 301 أو 302 صفحة ، أو حظر الوصول من عنوان IP محدد أو مواقع ويب أخرى. وبالتالي ، يؤدي استخدام ملفات .htaccess إلى إبطاء الأداء العام لخادم Apache [HTTP](/ar/web/http/).

## تنسيق ملف HTACCESS

يتم تخزين ملفات HTACCESS على قرص بتنسيق ملف نصي عادي. هذا يعني أنه يمكنك فتح هذه الملفات وتحريرها في أي محرر نصوص. لا يوجد اسم قبل "." في ملف .htaccess ، مما يوضح أنه ملف مخفي داخل المجلد.

## الاستخدامات الشائعة لملف HTACCESS

فيما يلي خمسة استخدامات شائعة لملف HTACCESS.

### تعديل_إعادة الكتابة

يمكن استخدام ملف HTACCESS لتعيين وتغيير كيفية عرض عناوين URL وصفحات الويب على موقع الويب للمستخدمين.

### المصادقة

يمكن تحقيق المصادقة باستخدام .htaccess عن طريق إنشاء ملف passowrd يسمى .htpasswd. يتيح ذلك لزوار الموقع تقديم كلمة مرور إذا كانوا يرغبون في زيارة قسم معين من صفحة الويب.

### صفحات خطأ مخصصة

يمكنك إنشاء صفحات خطأ مخصصة مثل 400 Bad Request و 401 Authorization Required و 403 Forbidden Page و 404 File not found و 500 Internal Error with .htaccess file. ومع ذلك ، سيؤدي ذلك إلى إبطاء الأداء حيث سيتم تنفيذ جميع عمليات التحقق هذه أثناء الوصول إلى الصفحات.

### أنواع MIME

يمكن تعديل ملفات Apache HTACCESS لتشمل أنواع ملحقات بريد الإنترنت متعدد الأغراض (MIME). يتيح ذلك لخادمك دعم تسليم ملفات التطبيق التي لم يدعمها الموقع.

### مباحث أمن الدولة

تتضمن Server Side Includes (SSI) دورًا رائعًا في توفير الوقت على موقع الويب. يمكن تمكين SSI عن طريق إدخال الكود التالي hte في ملف htaccess الخاص بك.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## مثال على ملف Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## مراجع

* [البرنامج التعليمي لخادم Apache HTTP: ملفات .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

