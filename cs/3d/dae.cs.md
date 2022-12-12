{
  "date" : "2019-10-11",
  "keywords" :[ "soubor dae", "formát souboru dae", "co je soubor dae", "soubor", "příklad dae", "přípona souboru dae", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů DAE a rozhraních API, která mohou otevírat a vytvářet soubory DAE.",
  "title" :"DAE - Digital Asset Exchange File Format",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DAE?

Soubor DAE je formát souboru Digital Asset Exchange, který se používá pro výměnu dat mezi interaktivními 3D aplikacemi. Tento formát souboru je založen na schématu XML COLLADA (COLLAborative Design Activity), což je otevřené standardní schéma XML pro výměnu digitálních aktiv mezi grafickými softwarovými aplikacemi. Byla přijata organizací ISO jako veřejně dostupná specifikace, ISO/pAS 17506. Soubory DAE lze otevřít v aplikacích, jako je Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, a v rozhraních API, jako je [Aspose.CAD](https://products .aspose.com/cad).

## Formát souboru DAE

Formát souboru DAE je založen na [schématu XML COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf), kde jsou všechny prvky definovány jako značky XML. Umožňuje spojení různých nástrojů DCC a 3D zpracování do výrobního potrubí pro 3D aktiva. Má komplexní kódování vizuálních scén včetně geometrie, animace, shaderů a fyziky. Formát je otevřený, archivní a uchovává metainformace.

### Tagy COLLADA

Značka schématu COLLADA je uvedena níže.
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

Značka aktiv popisuje autora a prostředí souboru

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Knihovna fotoaparátu

Aktiva COLLADA jsou obsažena v knihovnách. Knihovna fotoaparátů obsahuje nepřekvapivě fotoaparáty. Běžné kamery jsou perspektivní nebo ortografické. Značka knihovny fotoaparátu je definována následovně.
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
### Světla

Běžná světla jsou bodová, bodová nebo směrová
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

### Instance materiálů

Efekty instance materiálů jsou definovány následovně.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Společné účinky

Běžné efekty fungují jako stav OpenGL 1 a lze je definovat následovně.

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

### Atributy geometrie

Geometrie popisuje atributy OpenGL a je definována následovně.
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

### Vizuální scény

Vizuální scény jsou jako jednotné scény a obsahují následující hierarchii uzlů.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Reference
* [Specifikace COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

