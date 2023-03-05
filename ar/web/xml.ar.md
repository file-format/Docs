{
  "date" : "2019-10-11",
  "keywords" :["xml" , "ملف" , "امتداد" , "تنسيق الملف" , "امتداد الملف" , "لغة الترميز الموسعة"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف XML" ,
  "description":"تعرف على تنسيق ملف XML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XML وفتحها." ,
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف XML؟

يرمز XML إلى لغة التوصيف الموسعة التي تشبه ** [HTML](/ar/ web / html /) ** ولكنها تختلف في استخدام العلامات لتعريف الكائنات. كانت الفكرة الكاملة وراء إنشاء تنسيق ملف XML هي تخزين البيانات ونقلها دون الاعتماد على أدوات البرامج أو الأجهزة. تعود شعبيته إلى كونه مقروءًا بواسطة الإنسان والآلة. يتيح ذلك إنشاء بروتوكولات بيانات مشتركة في شكل كائنات يتم تخزينها ومشاركتها عبر الشبكة مثل شبكة الويب العالمية (WWW). علامة "X" في XML قابلة للتوسعة مما يعني أن اللغة يمكن أن تمتد إلى أي عدد من الرموز وفقًا لمتطلبات المستخدم. من أجل هذه الميزات ، تستفيد منه العديد من تنسيقات الملفات القياسية مثل Microsoft Open XML و LibreOffice OpenDocument و ** [XHTML](/ar/ web / xhtml /) ** و ** [SVG](/ar/ page-description-language / svg /) **.

## تنسيق ملف XML

يعتمد تنسيق ملف XML على نموذج كائن مستند XML (DOM) وهو واجهة برمجة تطبيقات برمجية لمستندات HTML و XML. يحدد XML DOM طريقة قياسية للوصول إلى عناصر مستند XML ومعالجتها. يقوم بعمل عرض لهيكل الشجرة لمستند XML يمكن استخدامه للوصول إلى جميع العناصر من خلال شجرة DOM. يمكن تعديل / حذف العناصر الموجودة وكذلك يمكن إنشاء عناصر جديدة في شجرة XML. يُطلق على كل عنصر في مستند XML عقدة. XML DOM كما هو موضح في الصورة التالية.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### مقاربة عالمية لـ XML

قوة XML تجعلها لغة عالمية لاتصالات البيانات عبر الشبكة عن طريق تبسيط نقل البيانات وتغييرات النظام الأساسي. هذا أيضًا يضمن إمكانية تبادل البيانات بين الأنظمة غير المتوافقة عن طريق تخزين البيانات بتنسيق نص عادي. HTML مخصصة لتمثيل البيانات عبر الويب ، بينما XML مخصصة لتبادل البيانات. تحدد أزواج علامات التمييز المستخدمة داخل XML العناصر الأساسية للهيكل الذي سيتم استخدامه من خلال قراءة التطبيقات.

## مثال XML

فيما يلي مثال مبسط لفهرس الأقراص المضغوطة حيث يحتوي كل سجل على معلومات حول الأقراص المضغوطة مثل الفنان والبلد والشركة والسعر وسنة الإنتاج.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## مراجع

* [XML - بواسطة Wikipedia](https://en.wikipedia.org/wiki/XML)

