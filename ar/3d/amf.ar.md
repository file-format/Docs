{
  "date" : "2019-10-11",
  "keywords" :["amf" , "ملف amf" , "تنسيق ملف amf" , "تنسيق الملف" , "3d"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف AMF وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات AMF." ,
  "title" :"AMF - ملف التصنيع الإضافي" ,
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف AMF؟
يتكون ملف AMF من إرشادات لوصف الكائنات حتى يتم استخدامها بواسطة عمليات التصنيع المضافة. يحتوي على فتحة<amf> علامة XML وتنتهي بامتداد</amf> عنصر. يسبق ذلك سطر إعلان XML يحدد إصدار XML وتشفير الملف. يمكن أن تتضمن الإعلانات معلومات وحدات القياس ، وفي حالة عدم وجود مثل هذه المعلومات ، يتم استخدام المليمترات كوحدة افتراضية.


## تنسيق ملف AMF

يحدد تنسيق ملف التصنيع الإضافي (** AMF **) المعايير المفتوحة لوصف الكائنات من أجل استخدامها من خلال عمليات التصنيع المضافة مثل الطباعة ثلاثية الأبعاد. تستخدم برامج CAD تنسيق ملف AMF من خلال الاستفادة من المعلومات مثل الهندسة واللون والمواد الخاصة بالكائنات. يختلف AMF عن تنسيق STL لأن الجانب الجانبي لا يدعم الألوان والمواد والشبكات والأبراج.

### عناصر ملف AMF

عناصر المستوى الأعلى الخمسة المحددة بامتداد<AMF> العلامات على النحو المفصل أدناه. يجب أن يكون وجود عنصر كائن واحد في ملف AMF كامل الوظائف.

"<object> `- يحدد عنصر الكائن حجمًا أو أحجامًا من المواد ، يرتبط كل منها بمعرف مادة للطباعة. يجب أن يكون هناك عنصر كائن واحد على الأقل في الملف. الكائنات الإضافية اختيارية.

"<material> `- يحدد عنصر المادة الاختياري مادة واحدة أو أكثر للطباعة بمعرف المادة المصاحب. إذا لم يتم تضمين أي عنصر مادي ، فيتم افتراض مادة افتراضية واحدة.

"<texture> "- يحدد عنصر النسيج الاختياري صورة أو نسيجًا واحدًا أو أكثر لتعيين اللون أو النسيج ، ولكل منها معرف نسيج مرتبط.

"<constellation> "- يدمج عنصر الكوكبة الاختياري بشكل هرمي الكائنات والمجموعات النجمية الأخرى في نمط نسبي للطباعة.

"<metadata> `- يحدد عنصر البيانات الوصفية الاختياري معلومات إضافية حول الكائن (العناصر) والعناصر الموجودة في الملف.

## مثال AMF

فيما يلي مثال لملف AMF الذي يمكن نسخه إلى ملف [text](/ar/word-processing/txt/) وحفظه كملف مضغوط [zip](/ar/compression/zip/) للفتح.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## مراجع

* [AMF - ويكيبيديا](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [مواصفات AMF على ISO](https://www.iso.org/standard/67472.html)

