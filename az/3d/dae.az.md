{
  "date": "2019-10-11",
  "keywords": [
"dae faylı",
"dae fayl formatı",
"dae faylı nədir",
"fayl",
"misal",
"dae fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DAE fayl formatı və DAE fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "DAE - Rəqəmsal Aktiv Mübadilə Fayl Formatı",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-aze"
}
},
  "lastmod": "2019-09-10"
}

## DAE faylı nədir?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE faylları Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD kimi proqramlarda və [Aspose.CAD](https://products.aspose.com/cad/) kimi API-lərdə açıla bilər.

## DAE fayl formatı

DAE fayl formatı bütün elementlərin XML teqləri kimi təyin olunduğu [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf)-ə əsaslanır. O, müxtəlif DCC və 3D emal alətlərini 3D aktivləri üçün istehsal boru kəmərinə birləşdirməyə imkan verir. O, həndəsə, animasiya, şeyderlər və fizika daxil olmaqla vizual səhnələrin hərtərəfli kodlaşdırılmasına malikdir. Format açıqdır, arxivdir və meta məlumatı saxlayır.

### COLLADA Teqləri

COLLADA sxem teqi aşağıda göstərildiyi kimidir.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Aktiv Etiketi

Aktiv etiketi faylın müəllifini və mühitini təsvir edir

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamera Kitabxanası

COLLADA aktivləri kitabxanaların içərisindədir. Kamera kitabxanasında təəccüblü şəkildə kameralar var. Ümumi kameralar perspektiv və ya orfoqrafikdir. Kamera kitabxanasının etiketi aşağıdakı kimi müəyyən edilir.
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
### İşıqlar

Ümumi işıqlar nöqtə, nöqtə və ya istiqamətlidir
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

### Material Nümunəsi

Materials instance effektləri aşağıdakı kimi müəyyən edilir.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Ümumi Effektlər

Ümumi effektlər OpenGL 1 vəziyyəti kimi fəaliyyət göstərir və aşağıdakı kimi müəyyən edilə bilər.

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

### Həndəsə Atributları

Həndəsə OpenGL atributlarını təsvir edir və aşağıdakı kimi müəyyən edilir.
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

### Vizual Səhnələr

Vizual səhnələr birlik səhnələri kimidir və aşağıdakı kimi qovşaqların iyerarxiyasını ehtiva edir.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## İstinadlar
 * [COLLADA 1.5.0 Spesifikasiyalar](https://www.khronos.org/files/collada_spec_1_5.pdf)

