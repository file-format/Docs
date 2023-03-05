{
  "date" : "2019-10-11",
  "keywords" :["xbrl" , "ملف xbrl" , "تنسيق ملف xbrl" , "نوع ملف xbrl" , "ملف" , "النوع" , "ما هو ملف xbrl"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - تنسيق ملف التقارير المالية والتجارية" ,
  "description":"تعرف على تنسيق ملف XBRL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XBRL وفتحها." ,
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
} ,
  "lastmod" : "2021-02-25"
}

## ما هو ملف XBRL؟

يعد الملف بامتداد .xbrl (لغة إعداد التقارير التجارية الموسعة) إطارًا عالميًا متاحًا مجانًا لتبادل معلومات الأعمال. يتم استخدامه الآن على نطاق واسع كأحد تنسيقات المعايير التي حلت محل التقارير الورقية القديمة بسجلات رقمية أكثر فائدة ودقة. تتضمن البيانات المتبادلة باستخدام ملفات XBRL دفاتر الأستاذ والتفاصيل المالية والميزانية العمومية. وهو يدعم علامات البيانات التي تسمح بمعالجة البيانات من الإعداد حتى مرحلة التحليل لمعلومات الأعمال بجميع أنواعها. يمكن فتح ملفات XBRL باستخدام برنامج مثل Rivet Software Dragon View XBRL Viewer و APIs مثل [Aspose.Finance](https://products.aspose.com/finance).

## تنسيق ملف XBRL

XBRL هو معيار دولي مفتوح لتقارير الأعمال الرقمية المستخدمة على نطاق واسع على مستوى العالم. إنها لغة قائمة على [XML](/ar/ web / xml /) تستخدم عناصر XBRL ، والمعروفة باسم العلامات ، لوصف كل عنصر من عناصر بيانات الأعمال لصياغة البيانات لفرز التقارير وتحليلها. تم تطوير مواصفات تنسيق ملف XBRL ونشرها بواسطة شركة XBRL International، Inc ، مع [XBRL الإصدار 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) حاليًا متاح للمستخدمين.

### هيكل مستند XBRL

معلومات كاملة حول [علامات XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) يمكن للمبرمجين الرجوع إليه لكتابة تطبيقات للعمل بتنسيق الملف هذا. يتكون XBRL من مثيل XBRL ومجموعة من التصنيفات.

** `XBRL Instance` ** - يبدأ مثيل XBRL بامتداد<xbrl> عنصر الجذر. يمكن أن تحتوي وثيقة XML الكبيرة على أكثر من نسخة XBRL مضمنة فيها.

** "تصنيف XBRL" ** - [تصنيف XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 + تصحيح-errata-2013-02-20.html # _5) يُعرّف على أنه بنية مخطط XML ومجموعة من عناصر الارتباطات الخارجية المُشار إليها مباشرةً. مخطط التصنيف القابل للتوسع يعرض مراجع قاعدة الارتباط كما يلي.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## مراجع ##

* [XBRL - بواسطة Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [لغة تقارير الأعمال الموسعة (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- Errata-2013-02-20.html)

