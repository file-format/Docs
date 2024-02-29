{
  "date": "2019-10-11",
  "keywords": [
"فایل dae",
"فرمت فایل dae",
"فایل dae چیست",
"فایل",
"دای مثال",
"پسوند فایل dae",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DAE و APIهایی که می توانند فایل های DAE را باز کرده و ایجاد کنند، بیاموزید.",
  "title": "DAE - فرمت فایل تبادل دارایی دیجیتال",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-fae"
}
},
  "lastmod": "2019-09-10"
}

## فایل DAE چیست؟

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. فایل های DAE را می توان در برنامه هایی مانند Adobe Photoshop، AutoDesk Maya، AutoDesk AutoCAD و API هایی مانند [Aspose.CAD](https://products.aspose.com/cad/) باز کرد.

## فرمت فایل DAE

فرمت فایل DAE بر اساس [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf) است که در آن همه عناصر به عنوان تگ XML تعریف می شوند. این امکان اتصال ابزارهای متنوع DCC و پردازش سه بعدی را در خط لوله تولید دارایی های سه بعدی فراهم می کند. دارای رمزگذاری جامع صحنه های بصری از جمله هندسه، انیمیشن، سایه زن و فیزیک. فرمت باز، بایگانی است و اطلاعات متا را حفظ می کند.

### برچسب های COLLADA

تگ طرحواره COLLADA مطابق شکل زیر است.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### برچسب دارایی

تگ دارایی نویسنده و محیط فایل را توصیف می کند

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### کتابخانه دوربین

دارایی های COLLADA در داخل کتابخانه ها قرار دارند. کتابخانه دوربین به طور شگفت انگیزی شامل دوربین هایی است. دوربین های معمولی پرسپکتیو یا املایی هستند. تگ کتابخانه دوربین به صورت زیر تعریف می شود.
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
### چراغ ها

نورهای رایج نقطه ای، نقطه ای یا جهت دار هستند
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

### نمونه مواد

اثرات نمونه مواد به صورت زیر تعریف می شوند.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### جلوه های رایج

افکت های رایج مانند حالت OpenGL 1 عمل می کنند و می توانند به صورت زیر تعریف شوند.

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

### ویژگی های هندسه

هندسه ویژگی های OpenGL را توصیف می کند و به صورت زیر تعریف می شود.
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

### صحنه های بصری

صحنه های بصری مانند صحنه های وحدت هستند و شامل سلسله مراتبی از گره ها به شرح زیر هستند.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## منابع
 * [مشخصات COLLADA 1.5.0] (https://www.khronos.org/files/collada_spec_1_5.pdf)

