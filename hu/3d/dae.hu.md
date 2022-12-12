{
  "date" : "2019-10-11",
  "keywords" :[ "dae fájl", "dae fájl formátum", "mi az a dae fájl", "fájl", "dae példa", "dae fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a DAE fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak DAE fájlokat.",
  "title" :"DAE - Digital Asset Exchange File Format",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DAE fájl?

A DAE fájl egy Digital Asset Exchange fájlformátum, amelyet interaktív 3D alkalmazások közötti adatcserére használnak. Ez a fájlformátum a COLLADA (COLLAborative Design Activity) XML sémán alapul, amely egy nyílt szabványú XML séma a digitális eszközök grafikus szoftveralkalmazások közötti cseréjére. Az ISO nyilvánosan elérhető specifikációként fogadta el, az ISO/pAS 17506. A DAE fájlok megnyithatók olyan alkalmazásokban, mint az Adobe Photoshop, az AutoDesk Maya, az AutoDesk AutoCAD és az API-k, mint például az [Aspose.CAD](https://products .aspose.com/cad).

## DAE fájlformátum

A DAE fájlformátum a [COLLADA XML-sémán] (https://www.khronos.org/files/collada_spec_1_5.pdf) alapul, ahol az összes elem XML-címkeként van definiálva. Lehetővé teszi a különféle DCC és 3D feldolgozó eszközök gyártási folyamatba kötését a 3D eszközök számára. A vizuális jelenetek átfogó kódolásával rendelkezik, beleértve a geometriát, az animációt, a shadereket és a fizikát. A formátum nyitott, archív minőségű, és megőrzi a metainformációkat.

### COLLADA Címkék

A COLLADA sémacímke az alábbiak szerint látható.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Eszközcímke

Az eszközcímke leírja a fájl szerzőjét és környezetét

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamerakönyvtár

A COLLADA-eszközök a könyvtárakban találhatók. A kamerakönyvtár nem meglepő módon kamerákat tartalmaz. A gyakori kamerák perspektivikus vagy ortográfiaiak. A kamerakönyvtár címke meghatározása a következő.
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
### Lámpák

A gyakori lámpák pontszerűek, pontszerűek vagy irányítottak
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

### Anyagpéldány

A Materials példányhatások meghatározása az alábbiak szerint történik.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Gyakori hatások

A gyakori hatások az OpenGL 1 állapothoz hasonlóan működnek, és az alábbiak szerint határozhatók meg.

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

### Geometriai attribútumok

A geometria leírja az OpenGL attribútumokat, és a következőképpen definiálja.
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

### Vizuális jelenetek

A vizuális jelenetek olyanok, mint az egységjelenetek, és a következő csomópontok hierarchiáját tartalmazzák.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Hivatkozások
* [COLLADA 1.5.0 specifikáció](https://www.khronos.org/files/collada_spec_1_5.pdf)

