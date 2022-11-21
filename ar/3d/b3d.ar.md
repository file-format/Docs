{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف B3D ؛ المستخدم في ألعاب blitz3d وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات B3D." ,
  "title" :"ملف نموذج كيان B3D - Blitz3D" ,
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2021-04-19"
}

## ما هو ملف B3D؟

الملف ذو الامتداد .b3d هو ملف نموذج يستخدمه Blitz3D والذي قد يحتوي على نماذج ألعاب فيديو للشخصيات والمباني والتضاريس وغيرها من الكائنات. Blitz3D هي لغة برمجة تُستخدم لإنشاء ** ألعاب blitz3d **. Blitz3D هي لغة برمجة قوية ومرنة وسهلة الاستخدام مصممة لغرض وحيد هو كتابة ألعاب الفيديو. يمكن للمطورين إنشاء ألعاب ثلاثية الأبعاد مليئة بالإثارة ، وألغاز ثنائية الأبعاد ، ومغامرات ، و RPGS ، وأيًا كان باستخدام Blitz3D.

يعتمد Blitz3D على لغة البرمجة الأساسية ؛ وهو أيضًا سهل التعلم والاستخدام. كل هذه الحقائق تجعل Blitz مثالية للمبتدئين والمبرمجين الأكثر خبرة على حد سواء. على الرغم من أن ميزاتها تعتبر قديمة إلى حد ما مما هو موجود في معظم المحركات ثلاثية الأبعاد الحديثة ، إلا أن Blitz3D لا يزال يستخدم من قبل العديد من مبرمجي الألعاب في جميع أنحاء العالم.

## تاريخ موجز لـ Blitz3D

تم إصدار Blitz3D أساسًا لنظام التشغيل Microsoft Windows في سبتمبر 2001 ، للتنافس مع لغات تطوير الألعاب المماثلة الأخرى. كان Blitz3D نسخة مطورة على المحرك ثنائي الأبعاد السابق BlitzBasic ، والذي وسع مجموعة الأوامر الخاصة به مع إضافة واجهة برمجة تطبيقات لمحرك ثلاثي الأبعاد قائم على DirectX 7. يجب على مستخدمي Blitz3D أيضًا مقارنة BlitzMax ، وهو محرك لاحق من BlitzBasic. BlitzMax هو إصدار معقد ولكنه أكثر قوة من Blitz3D ، والذي يدعم لغات البرمجة الموجهة للكائنات. إنها واجهة برمجة تطبيقات رسومات محدثة لتناسب بشكل أفضل أحرف Unicode و OpenGL والتصدير إلى OSX و Linux بدلاً من Windows فقط.

## مثال B3D
سيبدو ملف b3d الذي يحتوي على 1 TEXS chunk و 1 BRUS chunk و 1 NODE chunk كما يلي:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
ستبدو الشبكة البسيطة وغير المتحركة وغير المنسوجة بالشكل التالي:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## مراجع
* [B3D] (https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC] (https://en.wikipedia.org/wiki/Blitz_BASIC)

