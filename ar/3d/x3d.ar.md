{
  "date" : "2019-10-11",
  "keywords" :["ملف x3d" , "تنسيق ملف x3d" , "ما هو ملف x3d" , "ملف" , "مثال x3d" , "امتداد ملف x3d" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - ملف صورة ثلاثية الأبعاد" ,
  "description":"تعرف على تنسيق ملف X3D وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات X3D." ,
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف X3D؟
X3D هو تنسيق ملف رسومات ثلاثية الأبعاد يستند إلى [XML](/ar/ web / xml /) لعرض المعلومات ثلاثية الأبعاد. إنه معيار معياري ويتم تحديده من خلال العديد من مواصفات ISO. يدعم التنسيق الرسومات المتجهة والنقطية والشفافية وتأثيرات الإضاءة وإعدادات الرسوم المتحركة بما في ذلك التدوير والتلاشي والتأرجح. أصبح لاحقًا لتنسيق الملف [VRML](/ar/ 3d / vrml /) في عام 2001. يتمتع X3D بميزة ترميز معلومات اللون (على عكس [STL](/ar/ cad / stl /)) التي يتم استخدامها أثناء طباعة النموذج على لون طابعة 3D. يتميز التنسيق بامتدادات لـ VRML ، مما يوفر القدرة على ترميز المشهد باستخدام بناء جملة XML وكذلك بناء جملة Open Inventor مثل VRML97 أو تنسيق ثنائي.

تمت الموافقة على المواصفات المجردة لـ X3D (ISO / IEC 19775) لأول مرة من قبل ISO في عام 2004. تمت الموافقة على ترميزات XML و ClassicVRML لـ X3D (ISO / IEC 19776) لأول مرة في عام 2005.

## تنسيق ملف X3D

تحتوي ملفات مشهد X3D على بنية ملف مشتركة:

* عنوان الملف (إما XML أو ClassicVRML أو ثنائي مضغوط)
* بداية عقدة الجذر X3D بما في ذلك سمات الإصدار والملف الشخصي
* قسم رئيسي يحتوي على عبارات مكون وبيانات وصفية (كلاهما اختياري)
* الرسم البياني X3D Scene وعقده الفرعية
* نهاية عقدة جذر X3D

## مثال تنسيق ملف X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## مراجع ##

* [X3D - بواسطة Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [الموقع الرسمي لاتحاد Web3D](http://www.web3d.org/)
* [موقع X3D الرسمي](http://www.web3d.org/x3d/what-x3d)

