{
  "date" : "2019-10-11",
  "keywords" :["ملف dae" , "تنسيق ملف dae" , "ما هو ملف dae" , "ملف" , "dae example" , "امتداد ملف dae" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف DAE وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات DAE." ,
  "title" :"DAE - تنسيق ملف تبادل الأصول الرقمية" ,
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف DAE؟

ملف DAE هو تنسيق ملف تبادل الأصول الرقمية يُستخدم لتبادل البيانات بين التطبيقات ثلاثية الأبعاد التفاعلية. يعتمد تنسيق الملف هذا على مخطط XML COLLADA (نشاط تصميم COLLAborative) وهو مخطط XML قياسي مفتوح لتبادل الأصول الرقمية بين تطبيقات برامج الرسوم. تم اعتماده من قبل ISO كمواصفات متاحة للجمهور ، ISO / pAS 17506. يمكن فتح ملفات DAE في تطبيقات مثل Adobe Photoshop و AutoDesk Maya و AutoDesk AutoCAD و APIs مثل [Aspose.CAD] (https: // products .aspose.com / cad).

## تنسيق ملف DAE

يعتمد تنسيق ملف DAE على [مخطط COLLADA XML] (https://www.khronos.org/files/collada_spec_1_5.pdf) حيث يتم تعريف جميع العناصر على أنها علامات XML. إنه يتيح ربط أدوات معالجة DCC و 3D المتنوعة في خط أنابيب إنتاج للأصول ثلاثية الأبعاد. يحتوي على ترميز شامل للمشاهد المرئية بما في ذلك الهندسة والرسوم المتحركة والتظليل والفيزياء. التنسيق مفتوح ويصنف في الأرشيف ويحتفظ بالمعلومات الوصفية.

### علامات كولادا

علامة مخطط COLLADA كما هو موضح أدناه.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### علامة الأصول

تصف علامة الأصل مؤلف وبيئة الملف

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### مكتبة الكاميرا

توجد أصول COLLADA داخل المكتبات. مكتبة الكاميرا تحتوي على كاميرات بشكل غير مفاجئ. الكاميرات الشائعة هي منظور أو إملائي. يتم تعريف علامة مكتبة الكاميرا على النحو التالي.
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### أضواء

المصابيح الشائعة هي نقطة أو موضعية أو اتجاهية
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### نموذج المواد

يتم تعريف تأثيرات مثيل المواد على النحو التالي.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### التأثيرات المشتركة

تعمل التأثيرات الشائعة مثل حالة OpenGL 1 ويمكن تعريفها على النحو التالي.

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### سمات الهندسة

يصف Geometry سمات OpenGL ويتم تعريفه على النحو التالي.
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### مشاهد بصرية

المشاهد المرئية تشبه مشاهد الوحدة وتحتوي على تسلسل هرمي للعقد على النحو التالي.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## مراجع
* [مواصفات COLLADA 1.5.0] (https://www.khronos.org/files/collada_spec_1_5.pdf)

