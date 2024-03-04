{
  "date": "2019-10-11",
  "keywords": [
"dae failą",
"dae failo formatas",
"kas yra dae failas",
"failą",
"dae pavyzdys",
"dae failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DAE failo formatą ir API, kurios gali atidaryti ir kurti DAE failus.",
  "title": "DAE – skaitmeninio turto mainų failo formatas",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-lte"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DAE failas?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE failus galima atidaryti tokiose programose kaip Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD ir API, pvz., [Aspose.CAD](https://products.aspose.com/cad/).

## DAE failo formatas

DAE failo formatas pagrįstas [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf), kur visi elementai yra apibrėžti kaip XML žymos. Tai leidžia susieti įvairius DCC ir 3D apdorojimo įrankius į 3D išteklių gamybos dujotiekį. Jame yra visapusiškas vaizdinių scenų, įskaitant geometriją, animaciją, atspalvius ir fiziką, kodavimas. Formatas yra atviras, archyvo lygio ir išlaiko meta informaciją.

### COLLADA Žymos

COLLADA schemos žyma yra tokia, kaip parodyta toliau.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Turto žyma

Turto žyma apibūdina failo autorių ir aplinką

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Fotoaparatų biblioteka

COLLADA turtas yra bibliotekose. Nenuostabu, kad fotoaparatų bibliotekoje yra fotoaparatų. Įprasti fotoaparatai yra perspektyviniai arba ortografiniai. Kameros bibliotekos žyma apibrėžiama taip.
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
### Šviesos

Įprasti žibintai yra taškiniai, taškiniai arba kryptiniai
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

### Medžiagų pavyzdys

Medžiagų egzempliorių efektai apibrėžiami taip.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Bendras poveikis

Įprasti efektai veikia kaip OpenGL 1 būsena ir gali būti apibrėžti taip.

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

### Geometrijos atributai

Geometrija aprašo OpenGL atributus ir apibrėžia taip.
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

### Vaizdinės scenos

Vaizdinės scenos yra kaip vienybės scenos ir turi mazgų hierarchiją, kaip nurodyta toliau.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Nuorodos
 * [COLLADA 1.5.0 specifikacijos](https://www.khronos.org/files/collada_spec_1_5.pdf)

