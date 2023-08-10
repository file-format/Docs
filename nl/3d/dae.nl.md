{
  "date" : "2019-10-11",
  "keywords" :[ "dae-bestand", "dae-bestandsformaat", "wat is een dae-bestand", "bestand", "dae-voorbeeld", "dae-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over DAE-bestandsindelingen en API's die DAE-bestanden kunnen openen en maken.",
  "title" :"DAE - Digital Asset Exchange-bestandsindeling",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DAE-bestand?

Een DAE-bestand is een Digital Asset Exchange-bestandsindeling die wordt gebruikt voor het uitwisselen van gegevens tussen interactieve 3D-toepassingen. Dit bestandsformaat is gebaseerd op het COLLADA (COLLAborative Design Activity) XML-schema, een open standaard XML-schema voor de uitwisseling van digitale middelen tussen grafische softwaretoepassingen. Het is door ISO aangenomen als een openbaar beschikbare specificatie, ISO/pAS 17506. DAE-bestanden kunnen worden geopend in toepassingen zoals Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD en API's zoals [Aspose.CAD](https://products.aspose.com/cad/).

## DAE-bestandsindeling

Het DAE-bestandsformaat is gebaseerd op het [COLLADA XML-schema](https://www.khronos.org/files/collada_spec_1_5.pdf) waarin alle elementen zijn gedefinieerd als XML-tags. Het maakt het mogelijk om diverse DCC- en 3D-verwerkingstools te binden aan een productiepijplijn voor 3D-assets. Het heeft uitgebreide codering van visuele scènes, waaronder geometrie, animatie, shaders en fysica. Het formaat is open, archiefwaardig en bevat meta-informatie.

### COLLADA-tags

De COLLADA-schematag is zoals hieronder weergegeven.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Activa-tag

De asset-tag beschrijft de auteur en de omgeving van het bestand

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Camerabibliotheek

COLLADA-middelen bevinden zich in bibliotheken. De camerabibliotheek bevat, niet verwonderlijk, camera's. Gemeenschappelijke camera's zijn perspectief of orthografische. De camerabibliotheektag wordt als volgt gedefinieerd.
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
### Lichten

Gemeenschappelijke lichten zijn punt, spot of directioneel
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

### Materialeninstantie

De instantie-effecten van Materialen worden als volgt gedefinieerd.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Algemene effecten

Gemeenschappelijke effecten werken als de OpenGL 1-status en kunnen als volgt worden gedefinieerd.

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

### Geometrie-attributen

Geometrie beschrijft de OpenGL-attributen en wordt als volgt gedefinieerd.
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

### Visuele Scènes

Visuele scènes zijn als eenheidsscènes en bevatten als volgt een hiërarchie van knooppunten.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referenties
* [COLLADA 1.5.0-specificaties](https://www.khronos.org/files/collada_spec_1_5.pdf)

