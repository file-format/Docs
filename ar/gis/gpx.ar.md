{
  "date" : "2019-10-11",
  "keywords" :["ملف gpx" , "ما هو ملف gpx" , "ملف" , "مثال gpx" , "امتداد ملف gpx" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - تنسيق ملف تبادل GPX" ,
  "description":"تعرف على تنسيق ملف GPX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات GPX وفتحها." ,
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف GPX؟

تمثل الملفات ذات امتداد GPX تنسيق تبادل GPS لتبادل بيانات GPS بين التطبيقات وخدمات الويب على الإنترنت. وهو عبارة عن تنسيق ملف XML خفيف الوزن يحتوي على بيانات GPS ، مثل إحداثيات ومسارات ومسارات يتم استيرادها والأحمر بواسطة برامج متعددة. تنسيق ملف GPX مفتوح ومدعوم من قبل مجموعة متنوعة من التطبيقات وأجهزة GPS. يمكن تحميل بيانات GPS من هذه الملفات لعرضها على تطبيقات الخرائط للأغراض الجغرافية المكانية.

## تنسيق ملف GPX ##

يتكون ملف GPX من بيانات موقع خطوط الطول والعرض وقيم الارتفاع وغيرها من المعلومات الوصفية الأخرى المحتملة. يتم التعبير عن بيانات الموقع بالدرجات العشرية ويتم التعبير عن الارتفاع بالأمتار. الوقت في ملف GPX هو بالتوقيت العالمي المنسق (UTC) باستخدام تنسيق ISO 8601. فوائد استخدام ملف GPX هي كما يلي:

* يسمح لك GPX بتبادل البيانات مع قائمة متزايدة من البرامج لأنظمة Windows و MacOS و Linux و Palm و PocketPC.
* يمكن تحويل GPX إلى تنسيقات ملفات أخرى باستخدام صفحة ويب بسيطة أو برنامج محول.
* يعتمد GPX على معيار XML ، لذا يمكن للعديد من البرامج الجديدة التي تستخدمها (Microsoft Excel ، على سبيل المثال) قراءة ملفات GPX.
* يجعل GPX من السهل على أي شخص على الويب تطوير ميزات جديدة تعمل على الفور مع برامجك المفضلة.

يعرض [مخطط GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) تمثيل تنسيق ملف GPX كمرجع.

### البيانات الأساسية ###

فيما يلي البيانات الأساسية التي تعد جزءًا من ملف GPX لتمثيل بيانات GPS.

* ** نقاط الطريق **: الإحداثية هي إحداثيات WGS84 (GPS) لنقطة وتمثل طبقة من ميزات نوع OGR wkbPoint
* ** الطرق **: تمثل طبقة ميزات من نوع OGR wkbLineString. وهي تتضمن قائمة بنقاط المسار ، وهي نقاط مسار تُظهر منعطفًا أو نقاط مرحلة تؤدي إلى وجهة
* ** المسارات **: تمثل المسارات طبقة ميزات من نوع OGR wkbMultiLineString. يتكون من مقطع واحد على الأقل يحتوي على إحداثيات في قائمة مرتبة من النقاط التي تصف المسار. يتكون من قائمة نقاط المسار التي تمثل مسارًا مستمرًا لنظام تحديد المواقع العالمي (GPS).

### ملف مثال GPX ###

يوضح ملف GPX التالي تنظيم بيانات GPS في ملف GPX ويمكن أن يعطي فكرة جيدة عن محتويات ملف GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## مراجع ##

* [تنسيق ملف GPX](http://www.topografix.com/gpx.asp)
* [GPX - بواسطة Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

