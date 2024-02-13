{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - تغيير تنسيق ملف OpenStreetMap",
  "description":"OSC - تغيير تنسيق ملف OpenStreetMap",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## ما هو ملف OSC؟

ملف OSC هو ملف تغيير التنسيق الذي يحتوي على بيانات خريطة الشارع المعدلة لخريطة شارع .osm موجودة. فهو يحتوي على معلومات حول التغييرات التي سيتم إجراؤها على [OSM file](/gis/osm/). يمكن أن يحتوي ملف OSC على ثلاثة أنواع محتملة من عمليات التعديل على بيانات OSM، مثل إدراج أو تعديل أو حذف. تُستخدم ملفات التغيير هذه بشكل شائع لتصدير البيانات من محرر OSM واستيرادها إلى محرر آخر.

يمكنك فتح ملفات OSC باستخدام برنامج Merkaartar وosmchange.

## تنسيق ملف OSC

يتم حفظ ملفات OSC بشكل شائع بتنسيق ملف JOSM حيث يتم تمثيل التغييرات بالعلامات. يبدأ بعلامة osmChange التي تشير إلى بداية الملف. تحدد العلامات الفرعية ما إذا كانت عملية إدراج أو تعديل أو حذف سيتم تنفيذها على العقدة المقابلة في ملف OSM. تحتوي محتويات العقدة بالفعل على محتويات علامة osm.

### مثال على تنسيق ملف OSC

فيما يلي مثال على عملية التعديل على العقدة. يجب أن يكون لكل عنصر معرف مجموعة التغييرات ورقم الإصدار.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## مراجع

* [تنسيق ملف JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


