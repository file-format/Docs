{
  "date" : "2019-10-11",
  "keywords" :[ "dae fil", "dae filformat", "vad är en dae fil", "fil", "dae exempel", "dae filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om DAE-filformat och API:er som kan öppna och skapa DAE-filer.",
  "title" :"DAE - Digital Asset Exchange File Format",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är DAE fil?

En DAE-fil är ett Digital Asset Exchange-filformat som används för att utbyta data mellan interaktiva 3D-applikationer. Det här filformatet är baserat på COLLADA (COLLAborative Design Activity) XML-schema som är ett öppet standard-XML-schema för utbyte av digitala tillgångar mellan grafikprogram. Det har antagits av ISO som en allmänt tillgänglig specifikation, ISO/pAS 17506. DAE-filer kan öppnas i applikationer som Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD och API:er som [Aspose.CAD](https://products .aspose.com/cad).

## DAE-filformat

DAE-filformatet är baserat på [COLLADA XML-schemat](https://www.khronos.org/files/collada_spec_1_5.pdf) där alla element definieras som XML-taggar. Det möjliggör bindning av olika DCC- och 3D-bearbetningsverktyg till en produktionspipeline för 3D-tillgångar. Den har omfattande kodning av visuella scener inklusive geometri, animation, shaders och fysik. Formatet är öppet, arkivklassat och behåller metainformation.

### COLLADA-taggar

COLLADA-schemataggen är som visas nedan.
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

Asset-taggen beskriver författaren och miljön för filen

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamerabibliotek

COLLADA-tillgångar finns i bibliotek. Kamerabiblioteket innehåller föga överraskande kameror. Vanliga kameror är perspektiv eller ortografiska. Kamerabibliotekstaggen definieras enligt följande.
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
### Ljus

Vanliga ljus är punkt, punkt eller riktad
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

### Materialinstans

Materials-instanseffekterna definieras enligt följande.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Vanliga effekter

Vanliga effekter fungerar som OpenGL 1-tillståndet och kan definieras enligt följande.

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

### Geometriattribut

Geometri beskriver OpenGL-attributen och definieras enligt följande.
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

### Visuella scener

Visuella scener är som enhetsscener och innehåller en hierarki av noder enligt följande.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referenser
* [COLLADA 1.5.0-specifikationer](https://www.khronos.org/files/collada_spec_1_5.pdf)

