{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف HTX - تنسيق ملف ملحق HTML" ,
  "description" :"دليل تنسيق ملفك للتعرف على ملف HTX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف HTX وفتحه." ,
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف HTX؟

ملف HTX هو في الواقع ملف HTML يحتوي على متغيرات البيانات لعرض نتائج استعلام قاعدة البيانات كصفحة ويب. يتم إنشاء ملفات HTX في الغالب باستخدام برنامج تطوير ويب Microsoft FrontPage ، ليتم حفظها في نفس المجلد مثل ملف Internet Database Connector (.IDC) المقابل.

يمكن فتح ملفات HTX باستخدام تطبيقات مثل Microsoft FrontPage وأي محرر نصوص مثل Notepad أو TextEdit أو Atom.

## تنسيق ملف HTX

يتم حفظ ملفات HTX كملف نص عادي مع رمز لاسترداد البيانات من قاعدة بيانات وحفظها في المتغيرات للعرض.


### مثال ملف HTX

مثال على ملف HTX هو على النحو التالي الذي يحدد رأس الصفحة لعرض قيود الاستعلام والمستندات المعروضة على الصفحة لعرضها على المستخدم.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

إخراج نموذج التعليمات البرمجية هذا كما يلي.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

كما يتضح ، فإن ملف HTX عبارة عن قالب يقوم بتنسيق كيفية إرجاع النتائج وعرضها للمستخدمين النهائيين. تمت كتابته بتنسيق HTML مع بعض ملحقات IIS وخدمة الفهرسة. تتضمن هذه الامتدادات أسماء متغيرة وأكواد أخرى لمعالجة النتائج.

## مراجع

* [تنسيق النتائج في ملف .Htx] (https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

