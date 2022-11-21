{
  "date" : "2019-10-11",
  "keywords" :["ascx" , "ملف ascx" , "تنسيق ملف ascx" , "نوع ملف ascx" , "ملف" , "نوع" , "ما هو ملف ascx"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف ASCX" ,
  "description" :"تعرف على ما هو ملف ASCX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASCX وفتحها." ,
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف ASCX؟

الملف ذو الملحق .ascx هو عنصر تحكم مستخدم يتم استخدامه كمكون قابل لإعادة الاستخدام في صفحات الويب. تتم الإشارة إليه في أي موقع ويب ASP عن طريق سحبه من مربع التحكم إلى الصفحة. تتم إضافة عناصر تحكم مستخدمي ASCX إلى المشروع كمصدر مركزي ، مما ينتج عنه أي تغيير في تحكم المستخدم ينعكس عبر موقع الويب بالكامل. على عكس ملفات ASMX التي تحدد آلية للتواصل داخل كائنين عبر الإنترنت ، فإن ملفات ASCX هي عناصر تحكم المستخدم للتضمين في الصفحات أو موقع الويب.

## تنسيق ملف ASCX

يتم كتابة ملفات ASCX بتنسيق نص عادي ويمكنها استخدام رمز خلف ميزة مثل صفحات الويب التي تنتهي بـ .ascx.cs. يبدأ رمز الترميز لعناصر تحكم المستخدم بتوجيهControl كما هو موضح في المثال التالي.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

يمكن إعادة استخدام عنصر تحكم مستخدم الويب هذا في العديد من الصفحات مثل تذييل الصفحة أو رأس الصفحة أو نوع من التنقل في الموقع. تحتوي عناصر تحكم مستخدم الويب على خصائص وطرق وأحداث مثل أي contorl آخر مما يجعلها مفيدة في ضبط سلوكهم المرئي.

### مثال على تسجيل عناصر تحكم المستخدم في web.config

من أجل استخدام عنصر تحكم مستخدم واحد في العديد من الصفحات ، يمكن تسجيل عنصر تحكم الويب في web.config. يسمح هذا باستخدام التحكم في جميع مواقع الويب بدلاً من التسجيل في كل صفحة على حدة. يحدد نموذج التعليمات البرمجية التالي كيفية تسجيل عنصر تحكم ويب في web.config ليتم عرضه كتذييل على موقع الويب بالكامل.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## مراجع

* [ASCX مقابل ASMX] (https://forums.asp.net/t/1838934.aspx؟How+to+work+with+ascx+files+)
* [ASCX User Control] (http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

