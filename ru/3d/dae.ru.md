{
  "date" : "2019-10-11",
  "keywords" :[ "файл dae", "формат файла dae", "что такое файл dae", "файл", "пример dae", "расширение файла dae", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла DAE и API-интерфейсах, которые могут открывать и создавать файлы DAE.",
  "title" :"DAE — формат файла обмена цифровыми активами",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .DAE вариант №

Файл DAE — это формат файла обмена цифровыми активами, который используется для обмена данными между интерактивными 3D-приложениями. Этот формат файла основан на XML-схеме COLLADA (COLLAborative Design Activity), которая представляет собой открытую стандартную XML-схему для обмена цифровыми активами между графическими приложениями. Он был принят ISO в качестве общедоступной спецификации ISO/pAS 17506. Файлы DAE можно открывать в таких приложениях, как Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, и API-интерфейсах, таких как [Aspose.CAD](https://products .aspose.com/cad).

## Формат файла DAE

Формат файла DAE основан на [схеме XML COLLADA] (https://www.khronos.org/files/collada_spec_1_5.pdf), где все элементы определены как теги XML. Он позволяет привязывать различные инструменты DCC и 3D-обработки к производственному конвейеру для 3D-ресурсов. Он имеет комплексное кодирование визуальных сцен, включая геометрию, анимацию, шейдеры и физику. Формат является открытым, архивным и сохраняет метаинформацию.

### КОЛЛАДА Теги

Тег схемы COLLADA показан ниже.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Тег актива

Тег ресурса описывает автора и среду файла.

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Библиотека камер

Активы COLLADA содержатся внутри библиотек. Неудивительно, что библиотека камер содержит камеры. Обычные камеры являются перспективными или орфографическими. Тег библиотеки камер определяется следующим образом.
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
### Огни

Обычные источники света бывают точечными, точечными или направленными.
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

### Экземпляр материалов

Эффекты экземпляра материалов определяются следующим образом.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Общие эффекты

Общие эффекты действуют подобно состоянию OpenGL 1 и могут быть определены следующим образом.

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

### Атрибуты геометрии

Геометрия описывает атрибуты OpenGL и определяется следующим образом.
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

### Визуальные сцены

Визуальные сцены похожи на сцены единства и содержат следующую иерархию узлов.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## использованная литература
* [Технические характеристики COLLADA 1.5.0] (https://www.khronos.org/files/collada_spec_1_5.pdf)

