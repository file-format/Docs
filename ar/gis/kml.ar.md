{
  "date" : "2019-10-11",
  "keywords" :["ملف kml" , "ما هو ملف kml" , "ملف" , "مثال kml" , "امتداد ملف kml" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"KML - لغة ترميز Keyhole" ,
  "description":"تعرف على تنسيق ملف KML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات KML وفتحها." ,
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف KML؟

KML ، لغة ترميز Keyhole) يحتوي على معلومات جغرافية مكانية في تدوين XML. يمكن فتح الملفات المحفوظة بتنسيق KML في تطبيقات نظام المعلومات الجغرافية (GIS) بشرط أن تدعمها. بدأت العديد من التطبيقات في تقديم الدعم لتنسيق ملف KML بعد اعتماده كمعيار دولي. يستخدم ملف KML بنية قائمة على العلامات مع عناصر وسمات متداخلة. جميع العلامات حساسة لحالة الأحرف وترتيب هذه العلامات ، وفقًا لـ [KML] (https://developers.google.com/kml/documentation/kmlreference) المرجع ، مهم لمتابعة.

## نبذة تاريخية ##

تم تطوير KML في الأصل للاستخدام مع برنامج Google Earth والذي كان يُعرف في الأصل باسم Keyhole Earth Viewer. تم اعتماد KLM كمعيار دولي في عام 2008 من قبل Open Geospatial Consortium في عام 2008. نظرًا لأن التنسيق تم تطويره للاستخدام مع Google Earth ، فقد تميز بأنه أول من يقوم بعرض ملفات KML وتحريرها. مع مرور الوقت ، يوجد الآن المزيد والمزيد من المشاريع التي توفر الدعم لتنسيقات ملفات KML بما في ذلك العديد من واجهات برمجة التطبيقات بلغات مختلفة.

## مواصفات تنسيق ملف KML ##

مرجع KML هو دليل كامل للإشارة من أجل الحصول على مواصفات تنسيق الملف الكامل. يتكون ملف KML القياسي من:

* العلامات الموضعية
* العلامات الموضعية HTMLin الوصفية
* تراكبات أرضية
* مسارات
* المضلعات

بالإضافة إلى ذلك ، يمكن أن يحتوي الإصدار المتقدم من ملف KML على:

* أنماط الهندسة
* أنماط الأيقونات المميزة
* تراكبات الشاشة
* روابط الشبكة

يحتوي كل عنصر من عناصر KML على معلومات طويلة تحدد الموقع الجغرافي للمعلومات الموجودة في الملف. ومع ذلك ، يمكن أن تكون هناك معلمات إضافية مثل العنوان والارتفاع والميل.

### علامات المكان ###

يتم استخدامه لتمثيل موقع على سطح الأرض ويتم تحديده بواسطة<Point> عنصر. فيما يلي مثال على كيفية تمثيل العلامة الموضعية في ملف KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML وصفي في العلامات الموضعية ###

يمكن إقران معلومات إضافية بعلامة موضعية تزيد من تحسين تمثيل العلامة الموضعية. تتضمن هذه المعلومات الروابط وأحجام الخطوط والأنماط والألوان. بالإضافة إلى ذلك ، يتضمن أيضًا محاذاة النص والجداول لتكون جزءًا من العلامة الموضعية.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### تراكبات أرضية ###

تمثل طبقات الصورة على سطح الأرض. ال<icon> يحتوي elment على رابط ملف صورة التراكب.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### مسارات ###

يتم تمثيل المسارات بواسطة<LineString> عنصر عبارة عن مجموعة من أزواج خطوط الطول. باستخدام هذه ، يمكن إنشاء العديد من أنواع المسارات المختلفة في Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## الإسناد المكاني في ملف KML ##

يمكن أن يكون للمعلومات الواردة في أي ملف جغرافي مكاني حول المواقع الجغرافية معاني مختلفة بدون معلومات الإسناد المكاني. بشكل افتراضي ، يتم تحديد الإسناد المكاني لملف KML بواسطة النظام الجيوديسي العالمي لعام 1984 ، WGS84.

## مراجع ##

* [مرجع KML] (https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial for KML] (https://developers.google.com/kml/documentation/kml_tut)
* [تنسيق ملف KML] (https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

