{
  "date" : "2019-10-11",
  "keywords" :["ملف gml" , "ما هو ملف gml" , "ملف" , "gml example" , "امتداد ملف gml" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"GML - تنسيق ملف لغة توصيف الجغرافيا" ,
  "description":"تعرف على تنسيق ملف GML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات GML وفتحها." ,
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف GML؟

يرمز GML إلى لغة ترميز الجغرافيا التي تستند إلى مواصفات XML التي طورها الاتحاد الجغرافي المكاني المفتوح (OGC). يستخدم التنسيق لتخزين ميزات البيانات الجغرافية للتبادل بين تنسيقات الملفات المختلفة. إنها بمثابة لغة نمذجة للأنظمة الجغرافية بالإضافة إلى تنسيق تبادل مفتوح للمعاملات الجغرافية على الإنترنت.

## تنسيق ملف GML ##

كما هو الحال مع معظم القواعد النحوية المستندة إلى XML ، هناك جزأين للقواعد - المخطط الذي يصف المستند ومستند المثيل الذي يحتوي على البيانات الفعلية. يتم وصف مستند GML باستخدام مخطط GML. يتيح ذلك للمستخدمين والمطورين وصف مجموعات البيانات الجغرافية العامة التي تحتوي على نقاط وخطوط ومضلعات. باستخدام مخططات التطبيق ، يمكن للمستخدمين الرجوع إلى الطرق والطرق السريعة والجسور بدلاً من النقاط والخطوط والمضلعات.

تجدر الإشارة إلى أنه لا ينبغي تفسير GML لتمثيل البيانات المكانية على الخرائط. يختلف تمثيل محتوى GML عن الغرض الذي تم إنشاء GML من أجله. باختصار ، يشبه GML XML من حيث أنه يستخدم فقط للاحتفاظ بالمحتويات المكانية التي يمكن استخدامها عن طريق تعيين التطبيقات لغرض العرض.

### تكوين المحتوى في GML ###

تمثل GML البيانات المكانية باستخدام الميزات وهي قائمة بالخصائص والأشكال الهندسية. الخاصية لها اسم ونوع ووصف قيمة. تتكون الأشكال الهندسية من لبنات بناء هندسية أساسية مثل:

* نقاط
* خطوط
* المنحنيات
* sufraces و
* المضلعات

تم التخطيط للإصدارات المستقبلية من GML لدعم الهندسة ثلاثية الأبعاد بالإضافة إلى العلاقات الطوبولوجية بين الميزات.

يسمح ترميز GML بالفعل بميزات معقدة للغاية. يمكن أن تتكون الميزة على سبيل المثال من ميزات أخرى. وبالتالي ، قد تتكون ميزة واحدة مثل المطار من ميزات أخرى مثل طرق سيارات الأجرة والممرات والشماعات والمحطات الجوية. يمكن أيضًا أن تتكون هندسة المعالم الجغرافية من العديد من العناصر الهندسية. وبالتالي يمكن أن تتكون الميزة المعقدة هندسيًا من مزيج من أنواع الهندسة بما في ذلك النقاط وسلاسل الخطوط والمضلعات.

### أمثلة ###

يقوم GML 1.0 و 2.0 بترميز كائنات Polygons و Points و LineString على النحو التالي:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## مراجع ##

* [مواصفات GML] (http://www.opengeospatial.org/standards/gml)
* [GML - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/Geography_Markup_Language)
