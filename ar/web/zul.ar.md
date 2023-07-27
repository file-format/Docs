{
  "date" : "2021-05-24",
  "keywords" :["zul" , "ملف" , "امتداد" , "تنسيق الملف" , "امتداد الملف" , "فتح"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف واجهة مستخدم ZUL - ZK" ,
  "description":"تعرف على تنسيق ملف ZUL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ZUL وفتحها." ,
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-24"
}

## ما هو ملف ZUL؟

الملف بامتداد .zul هو ملف ويب تم إنشاؤه باستخدام لغة تمييز واجهة المستخدم (ZUML) ويحتوي على تعريفات لعناصر واجهة المستخدم. تدعم فئات Ajax و Java استخدام ZUML المستند إلى [XML](/ar/web/xml/) لتطوير الملفات الجانبية للخادم. تم تطوير تنسيق ملف ZUL بواسطة ZK ، وهو إطار عمل لواجهة المستخدم يمكّنك من إنشاء تطبيقات الويب والجوال دون معرفة JavaScript أو AJAX.

## تنسيق ملف ZUL

ملفات ZUL مبنية على XML ، وتتكون من عناصر مختلفة لبناء واجهة المستخدم. يستخدم مُحمل ZK كل عنصر XML لإنشاء مكون. المعالجة الشاملة لعناصر الصفحة مثل عنوان الصفحة والوصف وما إلى ذلك موصوفة في كل تعليمات معالجة XML من ZUML.

### مثال ZUL

في المثال التالي لرمز ZUML ، يحدد السطر الأول عنوان الصفحة ، بينما يُنشئ السطر الثاني مكونًا جذرًا بالعنوان والحد ، ويقوم السطر الثالث بإنشاء زر مع تسمية ومستمع حدث.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
يمكن تنزيل مخطط ZUL من https://www.zkoss.org/2005/zul/zul.xsd.
## مراجع

* [ZUL - بواسطة ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [مخطط ZUL](https://www.zkoss.org/2005/zul/zul.xsd)

