{
  "date": "2019-10-11",
  "keywords": [
"dae filen",
"dae filformat",
"hvad er en dae fil",
"fil",
"dae eksempel",
"dae filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DAE-filformat og API'er, der kan åbne og oprette DAE-filer.",
  "title": "DAE - Digital Asset Exchange File Format",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-dae"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DAE fil?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE-filer kan åbnes i programmer som Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD og API'er som f.eks. [Aspose.CAD](https://products.aspose.com/cad/).

## DAE filformat

DAE-filformatet er baseret på [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf), hvor alle elementer er defineret som XML-tags. Det muliggør binding af forskellige DCC- og 3D-behandlingsværktøjer til en produktionspipeline for 3D-aktiver. Den har omfattende kodning af visuelle scener, herunder geometri, animation, shaders og fysik. Formatet er åbent, arkivklassificeret og bevarer metainformation.

### COLLADA-tags

COLLADA-skematagget er som vist nedenfor.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Asset Tag

Aktiv-tagget beskriver forfatteren og miljøet af filen

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamerabibliotek

COLLADA-aktiver er indeholdt i biblioteker. Kamerabiblioteket indeholder ikke overraskende kameraer. Almindelige kameraer er perspektiv eller ortografiske. Kamerabibliotekets tag er defineret som følger.
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
### Lys

Almindelige lys er punkt, spot eller retningsbestemt
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

### Materialeforekomst

Materials-instanseffekterne er defineret som følger.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Almindelige effekter

Almindelige effekter fungerer som OpenGL 1-tilstanden og kan defineres som følger.

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

### Geometri-attributter

Geometri beskriver OpenGL-attributterne og defineret som følger.
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

### Visuelle scener

Visuelle scener er som enhedsscener og indeholder et hierarki af noder som følger.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referencer
 * [COLLADA 1.5.0-specifikationer](https://www.khronos.org/files/collada_spec_1_5.pdf)

