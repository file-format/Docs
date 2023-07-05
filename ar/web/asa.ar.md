{
  "date" : "2021-12-09",
  "keywords" :["asa" , ". asa" , "تنسيق الملف" , "نوع الملف" , "ما هو ملف .asa"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ملف تكوين ASP" ,
  "description" :"تعرف على ما هو ملف ASA وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASA وفتحها." ,
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-12-09"
}

## ما هو ملف ASA؟

ملف ASA هو ملف تكوين ، تم إنشاؤه لمشاريع [ASP](/ar/web/asp/) / ASP.NET. يحتوي على إعلانات للمتغيرات ، ويحتوي على وظائف من المفترض أن تكون متاحة على المستوى العالمي في التطبيق. يمكن لجميع صفحات المشروع الوصول إلى هذه المتغيرات والوظائف ، وبالتالي تجنب الحاجة إلى إعادة كتابتها. أحد الأمثلة على ذلك هو صفحة Global.asa المخزنة في الدليل الجذر ليتم الوصول إليها بواسطة صفحات موقع ويب ASP الأخرى. ملفات Global.asa اختيارية ، ولكن إذا تم استخدامها ، يمكن أن يحتوي كل تطبيق على ملف Global.asa واحد فقط.

## تنسيق ملف ASA - مزيد من المعلومات

ملفات ASA هي ملفات نصية عادية بالمعلومات التالية.

* أحداث التطبيق
* أحداث الدورة
* \<object> الإعلانات
* إعلانات TypeLibrary
* # تضمين التوجيه

## مثال على ملف ASA

يمكن أن يبدو ملف Global.asa مثل هذا.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## مراجع

* [ملف ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

