{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ملف لغة ترميز ColdFusion" ,
  "description" :"تعرف على ما هو ملف CFML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CFML وفتحها." ,
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-08-19"
}

## ما هو ملف CFML؟

الملف ذو الامتداد .cfml هو ملف ColdFusion Markup Language يُستخدم لإنشاء صفحة ويب. يشير إلى مجموعة من القواعد المستخدمة لتحديد كيفية تطوير تطبيق ColdFusion بواسطة المبرمج. ColdFusion هي لغة برمجة تُستخدم لإنشاء تطبيقات ويب من جهة أخرى بسرعة وبأقل من التقنيات الأخرى مثل [ASP](/ar/web/asp/) ، [PHP](/ar/programming/php/) ، إلخ. من التطبيقات التي يمكنها فتح ملفات CML تشمل Adobe ColdFusion 2018 و Adobe ColdFusion Builder و Adobe Dreamweaver.

## تنسيق ملف CFML - مزيد من المعلومات

ملفات CFML هي ملفات ترميز وتحتوي على عناصر ويب في شكل علامات. هذه ملفات نصية يمكن فتحها وتحريرها في أي محرر نصوص. تتكون ملفات CFML من عدة علامات مشابهة لـ [HTML](/ar/web/html/) وعادة ما تتكون من علامة فتح وإغلاق. يمكن أن تحتوي هذه العلامات أيضًا على سمة واحدة أو أكثر.

### الكلمات الدلالية النحو

فيما يلي الصيغة العامة لعلامات CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

تقبل معظم العلامات سمات ويتم تعريفها على أنها تتبع.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

تقبل بعض هذه العلامات أيضًا سمات متعددة بالصيغة التالية.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## مثال رمز CFML

فيما يلي مثال يستخدم علامة CFML فعلية - علامة `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## مراجع

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

