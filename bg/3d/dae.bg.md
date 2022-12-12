{
  "date" : "2019-10-11",
  "keywords" :[ "dae файл", "dae файлов формат", "какво е dae файл", "файл", "dae пример", "dae файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за DAE файловия формат и API, които могат да отварят и създават DAE файлове.",
  "title" :"DAE – Файлов формат за обмен на цифрови активи",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е DAE файл?

DAE файлът е файлов формат за обмен на цифрови активи, който се използва за обмен на данни между интерактивни 3D приложения. Този файлов формат се основава на XML схемата COLLADA (COLLAborative Design Activity), която е отворена стандартна XML схема за обмен на цифрови активи между приложения за графичен софтуер. Той е приет от ISO като публично достъпна спецификация, ISO/pAS 17506. DAE файловете могат да се отварят в приложения като Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD и API като [Aspose.CAD](https://products .aspose.com/cad).

## DAE файлов формат

Файловият формат DAE се основава на [XML схемата на COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf), където всички елементи са дефинирани като XML тагове. Той позволява обвързване на различни DCC и инструменти за 3D обработка в производствена линия за 3D активи. Има цялостно кодиране на визуални сцени, включително геометрия, анимация, шейдъри и физика. Форматът е отворен, архивен и запазва мета информация.

### Етикети COLLADA

Тагът на схемата COLLADA е както е показано по-долу.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Етикет на актива

Тагът на актива описва автора и средата на файла

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Библиотека на камерата

Активите на COLLADA се съдържат в библиотеки. Не е изненадващо библиотеката с камери съдържа камери. Често срещаните камери са перспективни или ортографски. Етикетът на библиотеката на камерата се дефинира, както следва.
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
### Светлини

Общите светлини са точкови, точкови или насочени
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

### Екземпляр на материали

Ефектите на екземпляра на Materials се дефинират както следва.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Общи ефекти

Общите ефекти действат като състоянието на OpenGL 1 и могат да бъдат дефинирани както следва.

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

### Геометрични атрибути

Геометрията описва атрибутите на OpenGL и се дефинира както следва.
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

### Визуални сцени

Визуалните сцени са като единни сцени и съдържат йерархия от възли, както следва.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Препратки
* [Спецификации на COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

