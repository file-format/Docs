{
  "date" : "2019-10-11",
  "keywords" :[ "файл dae", "формат файлу dae", "що таке файл dae", "файл", "приклад dae", "розширення файлу dae", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу DAE та API, які можуть відкривати та створювати файли DAE.",
  "title" :"DAE - формат файлу обміну цифровими активами",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл DAE?

Файл DAE — це формат файлу Digital Asset Exchange, який використовується для обміну даними між інтерактивними 3D-додатками. Цей формат файлу базується на XML-схемі COLLADA (COLLAborative Design Activity), яка є відкритою стандартною XML-схемою для обміну цифровими активами між графічними програмними програмами. Його було прийнято ISO як загальнодоступну специфікацію ISO/pAS 17506. Файли DAE можна відкривати в таких програмах, як Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, і API, таких як [Aspose.CAD](https://products .aspose.com/cad).

## Формат файлу DAE

Формат файлу DAE базується на [схемі XML COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf), де всі елементи визначено як теги XML. Це дає змогу об’єднувати різноманітні інструменти DCC і 3D-обробки в конвеєр виробництва 3D-активів. Він має комплексне кодування візуальних сцен, включаючи геометрію, анімацію, шейдери та фізику. Формат відкритий, архівний і зберігає метаінформацію.

### Теги COLLADA

Тег схеми COLLADA виглядає як показано нижче.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Тег ресурсу

Тег ресурсу описує автора та середовище файлу

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Бібліотека камери

Ресурси COLLADA містяться в бібліотеках. Бібліотека камер містить камери. Поширені камери перспективні або ортографічні. Тег бібліотеки камери визначається наступним чином.
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
### Світло

Поширені вогні точкові, точкові або спрямовані
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

### Екземпляр матеріалів

Ефекти екземплярів Materials визначені наступним чином.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Загальні ефекти

Загальні ефекти діють як стан OpenGL 1 і можуть бути визначені наступним чином.

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

### Атрибути геометрії

Geometry описує атрибути OpenGL і визначається наступним чином.
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

### Візуальні сцени

Візуальні сцени схожі на сцени єдності та містять ієрархію вузлів, як показано нижче.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Список літератури
* [Специфікації COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

