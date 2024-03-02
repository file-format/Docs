{
  "date": "2019-10-11",
  "keywords": [
"dae file",
"formáid comhaid dae",
"cad is comhad dae ann",
"comhad",
"dae shampla",
"síneadh comhad dae",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DAE agus APIanna ar féidir comhaid DAE a oscailt agus a chruthú.",
  "title": "DAE - Formáid Comhaid um Mhalartú Sócmhainní Digiteach",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-gae"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DAE ann?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. Is féidir comhaid DAE a oscailt in feidhmchláir mar Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, agus APInna ar nós [Aspose.CAD](https://products.aspose.com/cad/).

## Formáid Chomhaid DAE

Tá formáid comhaid DAE bunaithe ar an [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf) ina sainmhínítear na heilimintí go léir mar chlibeanna XML. Cuireann sé ar chumas uirlisí próiseála éagsúla DCC agus 3D a cheangal isteach i bpíblíne táirgthe do shócmhainní 3D. Tá ionchódú cuimsitheach radhairc aige lena n-áirítear céimseata, beochan, scáthaitheoirí agus fisic. Tá an fhormáid oscailte, de ghrád cartlainne agus coimeádann sí meiteaisnéis.

### Clibeanna COLLADA

Tá an chlib scéimre COLLADA mar a thaispeántar thíos.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Clib Sócmhainn

Déanann an chlib sócmhainn cur síos ar údar agus ar thimpeallacht an chomhaid

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Leabharlann Ceamara

Tá sócmhainní COLLADA laistigh de leabharlanna. Ní nach ionadh go bhfuil ceamaraí sa leabharlann ceamaraí. Tá ceamaraí coitianta peirspictíochta nó ortagrafach. Sainmhínítear an chlib leabharlainne ceamara mar seo a leanas.
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
### Soilse

Tá soilse coitianta pointe, spot nó treo
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

### Ábhair Ábhair

Sainmhínítear éifeachtaí shampla na nÁbhar mar seo a leanas.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Éifeachtaí Coitianta

Feidhmíonn éifeachtaí coitianta cosúil le staid OpenGL 1 agus is féidir iad a shainmhíniú mar seo a leanas.

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

### Tréithe Céimseata

Déanann Céimseata cur síos ar na tréithe OpenGL agus sainmhínithe mar seo a leanas.
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

### Radhairc Amharc

Tá radhairc amhairc cosúil le radhairc aontacht agus tá ordlathas nóid iontu mar a leanas.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Tagairtí
 * [Sonraíochtaí COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

