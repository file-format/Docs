{
  "date" : "2019-10-11",
  "keywords" :[ "dae-Datei", "dae-Dateiformat", "was ist eine dae-Datei", "Datei", "dae-Beispiel", "dae-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das DAE-Dateiformat und APIs, die DAE-Dateien öffnen und erstellen können.",
  "title" :"DAE - Digital Asset Exchange-Dateiformat",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DAE-Datei?

Eine DAE-Datei ist ein Digital Asset Exchange-Dateiformat, das zum Austauschen von Daten zwischen interaktiven 3D-Anwendungen verwendet wird. Dieses Dateiformat basiert auf dem XML-Schema COLLADA (COLLAborative Design Activity), einem offenen Standard-XML-Schema für den Austausch digitaler Assets zwischen Grafiksoftwareanwendungen. Es wurde von ISO als öffentlich verfügbare Spezifikation ISO/pAS 17506 angenommen. DAE-Dateien können in Anwendungen wie Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD und APIs wie [Aspose.CAD](https://products.aspose.com/cad/).

## DAE-Dateiformat

Das DAE-Dateiformat basiert auf dem [COLLADA-XML-Schema](https://www.khronos.org/files/collada_spec_1_5.pdf), in dem alle Elemente als XML-Tags definiert sind. Es ermöglicht die Einbindung verschiedener DCC- und 3D-Verarbeitungswerkzeuge in eine Produktionspipeline für 3D-Assets. Es verfügt über eine umfassende Codierung visueller Szenen, einschließlich Geometrie, Animation, Shader und Physik. Das Format ist offen, archivtauglich und behält Metainformationen bei.

### COLLADA-Tags

Das COLLADA-Schema-Tag sieht wie unten gezeigt aus.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Asset-Tag

Das Asset-Tag beschreibt den Autor und die Umgebung der Datei

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamerabibliothek

COLLADA-Assets sind in Bibliotheken enthalten. Die Kamerabibliothek enthält wenig überraschend Kameras. Übliche Kameras sind perspektivisch oder orthografisch. Das Tag der Kamerabibliothek ist wie folgt definiert.
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
### Beleuchtung

Gängige Lichter sind Punkt-, Spot- oder gerichtete Lichter
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

### Materialinstanz

Die Materialinstanzeffekte sind wie folgt definiert.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Gemeinsame Effekte

Allgemeine Effekte verhalten sich wie der OpenGL 1-Zustand und können wie folgt definiert werden.

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

### Geometrieattribute

Geometrie beschreibt die OpenGL-Attribute und ist wie folgt definiert.
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

### Visuelle Szenen

Visuelle Szenen sind wie Einheitsszenen und enthalten eine Hierarchie von Knoten wie folgt.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Verweise
* [COLLADA 1.5.0 Spezifikationen](https://www.khronos.org/files/collada_spec_1_5.pdf)

