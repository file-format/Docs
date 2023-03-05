{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CON File - مفهوم تنسيق ملف مصدر التطبيق" ,
  "description" :"تعرف على ما هو ملف CON و APIs التي يمكنها إنشاء ملفات CON وفتحها." ,
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
} ,
  "lastmod" : "2022-08-24"
}

## CON ما هو ملف CON؟

ملف CON هو ملف شفرة مصدر لتطبيق تم تطويره من أجل ** Concept Application Server **. يتم استخدامه لكتابة التطبيقات لتبادل البيانات بين الخادم والمستخدم. يمكن الوصول إلى ملفات CON المستضافة على الخادم من خلال مستعرض ويب بشرط تثبيت Concept Client على طرف المستخدم. خادم تطبيق Concept Application هو خادم ويب مع لغة برمجة صغيرة الحجم والتي قد تحتوي على محرك قاعدة بيانات مجموعة فرعية [SQL](/ar/ database / sql /) (TinDB).

يمكن فتح / تشغيل ملفات CON باستخدام خادم تطبيق مفهوم RadGs.

## تنسيق ملف CON - مزيد من المعلومات

تتم استضافة ملفات CON على الخادم ويتم الوصول إليها باستخدام متصفح الويب على جهاز المستخدم. يختلف المفهوم [URLs](/ar/ web / url /) عن عناوين HTTP العادية ويبدأ بـ ** concept: // **.

### مثال لعنوان URL لملف CON

يمكن الوصول إلى ملف CON المستضاف على Concept Application Server عبر متصفح الويب باستخدام عناوين URL مثل:

```
concept://domain.server.com/web_application/main.con.
```
## مراجع

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

