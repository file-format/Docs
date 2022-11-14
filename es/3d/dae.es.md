{
  "date" : "2019-10-11",
  "keywords" :[ "archivo dae", "formato de archivo dae", "qué es un archivo dae", "archivo", "ejemplo de dae", "extensión de archivo dae","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo DAE y las API que pueden abrir y crear archivos DAE",
  "title" :"DAE - Formato de archivo de intercambio de activos digitales",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DAE?

Un archivo DAE es un formato de archivo de intercambio de activos digitales que se utiliza para intercambiar datos entre aplicaciones 3D interactivas. Este formato de archivo se basa en el esquema XML COLLADA (COLLAborative Design Activity), que es un esquema XML estándar abierto para el intercambio de activos digitales entre aplicaciones de software de gráficos. Ha sido adoptado por ISO como una especificación disponible públicamente, ISO/pAS 17506. Los archivos DAE se pueden abrir en aplicaciones como Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD y API como [Aspose.CAD] (https://products aspose.com/cad).

## Formato de archivo DAE

El formato de archivo DAE se basa en el [esquema XML de COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf) donde todos los elementos se definen como etiquetas XML. Permite la vinculación de diversas herramientas de procesamiento 3D y DCC en una canalización de producción para activos 3D. Tiene una codificación integral de escenas visuales que incluye geometría, animación, sombreadores y física. El formato es abierto, de grado de archivo y retiene la metainformación.

### COLLADA Tags

La etiqueta del esquema COLLADA es como se muestra a continuación.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Etiqueta de propiedad

La etiqueta de propiedad describe el autor y el entorno del archivo.

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Biblioteca de cámaras

Los activos de COLLADA están contenidos dentro de las bibliotecas. La biblioteca de cámaras contiene, como era de esperar, cámaras. Las cámaras comunes son de perspectiva u ortográficas. La etiqueta de la biblioteca de la cámara se define de la siguiente manera.
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
### Luces

Las luces comunes son puntuales, puntuales o direccionales.
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

### Instancia de materiales

Los efectos de la instancia de Materiales se definen de la siguiente manera.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Efectos comunes

Los efectos comunes actúan como el estado de OpenGL 1 y se pueden definir de la siguiente manera.

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

### Atributos de geometría

La geometría describe los atributos de OpenGL y se define de la siguiente manera.
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

### Escenas visuales

Las escenas visuales son como escenas de unidad y contienen una jerarquía de nodos de la siguiente manera.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referencias
* [Especificaciones de COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

