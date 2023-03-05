{
  "date" : "2019-10-11",
  "keywords" :[ "plik dae", "format pliku dae", "co to jest plik dae", "plik", "przykład dae", "rozszerzenie pliku dae", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku DAE i interfejsach API, które mogą otwierać i tworzyć pliki DAE.",
  "title" :"DAE — format pliku wymiany zasobów cyfrowych",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DEA?

Plik DAE to format pliku Digital Asset Exchange, który służy do wymiany danych między interaktywnymi aplikacjami 3D. Ten format pliku jest oparty na schemacie XML COLLADA (COLLAborative Design Activity), który jest otwartym standardowym schematem XML do wymiany zasobów cyfrowych między aplikacjami graficznymi. Został przyjęty przez ISO jako publicznie dostępna specyfikacja, ISO/pAS 17506. Pliki DAE można otwierać w aplikacjach, takich jak Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD i interfejsach API, takich jak [Aspose.CAD](https://products .aspose.com/cad).

## Format pliku DAE

Format pliku DAE jest oparty na [schemacie XML COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf), w którym wszystkie elementy są zdefiniowane jako znaczniki XML. Umożliwia łączenie różnych narzędzi do przetwarzania DCC i 3D w potok produkcyjny zasobów 3D. Posiada kompleksowe kodowanie scen wizualnych, w tym geometrię, animację, shadery i fizykę. Format jest otwarty, archiwalny i zachowuje metainformacje.

### Tagi COLLADA

Znacznik schematu COLLADA jest pokazany poniżej.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Etykieta zasobu

Etykieta zasobu opisuje autora i środowisko pliku

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Biblioteka aparatu

Zasoby COLLADA są zawarte w bibliotekach. Biblioteka aparatów zawiera, co nie jest zaskoczeniem, aparaty. Typowe kamery są perspektywiczne lub prostopadłe. Znacznik biblioteki kamery jest zdefiniowany w następujący sposób.
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
### Światła

Typowe światła to punktowe, punktowe lub kierunkowe
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

### Instancja materiałów

Efekty wystąpienia materiałów są zdefiniowane w następujący sposób.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Typowe efekty

Typowe efekty działają jak stan OpenGL 1 i można je zdefiniować w następujący sposób.

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

### Atrybuty geometrii

Geometria opisuje atrybuty OpenGL i jest zdefiniowana w następujący sposób.
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

### Sceny wizualne

Sceny wizualne są podobne do scen jedności i zawierają następującą hierarchię węzłów.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Bibliografia
* [Specyfikacje COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

