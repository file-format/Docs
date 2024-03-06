{
  "date": "2019-10-11",
  "keywords": [
"dae fails",
"dae faila formāts",
"kas ir dae fails",
"failu",
"dae piemērs",
"dae faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DAE faila formātu un API, kas var atvērt un izveidot DAE failus.",
  "title": "DAE — digitālo aktīvu apmaiņas faila formāts",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-lve"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DAE fails?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE failus var atvērt tādās lietojumprogrammās kā Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD un API, piemēram, [Aspose.CAD](https://products.aspose.com/cad/).

## DAE faila formāts

DAE faila formāts ir balstīts uz [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf), kur visi elementi ir definēti kā XML tagi. Tas ļauj saistīt dažādus DCC un 3D apstrādes rīkus 3D līdzekļu ražošanas konveijerā. Tam ir visaptverošs vizuālo ainu kodējums, tostarp ģeometrija, animācija, ēnotāji un fizika. Formāts ir atvērts, arhīva līmeņa un saglabā metainformāciju.

### COLLADA tagi

COLLADA shēmas tags ir tāds, kā parādīts tālāk.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Līdzekļu tags

Līdzekļa tags apraksta faila autoru un vidi

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kameras bibliotēka

COLLADA līdzekļi atrodas bibliotēkās. Kameras bibliotēkā nepārsteidzoši ir kameras. Parastās kameras ir perspektīvas vai ortogrāfiskas. Kameras bibliotēkas tags ir definēts šādi.
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
### Gaismas

Parastie gaismas ir punktveida, punktveida vai virziena gaismas
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

### Materiālu instance

Materiālu gadījumu efekti ir definēti šādi.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Izplatītas sekas

Parastie efekti darbojas kā OpenGL 1 stāvoklis, un tos var definēt šādi.

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

### Ģeometrijas atribūti

Ģeometrija apraksta OpenGL atribūtus un definē šādi.
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

### Vizuālās ainas

Vizuālās ainas ir kā vienotības ainas un satur šādu mezglu hierarhiju.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Atsauces
 * [COLLADA 1.5.0 specifikācijas](https://www.khronos.org/files/collada_spec_1_5.pdf)

