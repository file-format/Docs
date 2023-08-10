{
  "date" : "2019-10-11",
  "keywords" :[ "fichier dae", "format de fichier dae", "qu'est-ce qu'un fichier dae", "fichier", "exemple dae", "extension de fichier dae","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier DAE et les API qui peuvent ouvrir et créer des fichiers DAE.",
  "title" :"DAE - Format de fichier d'échange d'actifs numériques",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DAE ?

Un fichier DAE est un format de fichier Digital Asset Exchange utilisé pour échanger des données entre des applications 3D interactives. Ce format de fichier est basé sur le schéma XML COLLADA (COLLAborative Design Activity) qui est un schéma XML standard ouvert pour l'échange d'actifs numériques entre les applications logicielles graphiques. Elle a été adoptée par l'ISO en tant que spécification accessible au public, ISO/pAS 17506. Les fichiers DAE peuvent être ouverts dans des applications telles qu'Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD et des API telles que [Aspose.CAD](https://products.aspose.com/cad/).

## Format de fichier DAE

Le format de fichier DAE est basé sur le [schéma XML COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf) où tous les éléments sont définis comme des balises XML. Il permet de lier divers outils de traitement DCC et 3D dans un pipeline de production pour les actifs 3D. Il dispose d'un encodage complet des scènes visuelles, y compris la géométrie, l'animation, les shaders et la physique. Le format est ouvert, de qualité archive et conserve les méta-informations.

### Balises COLLADA

La balise de schéma COLLADA est illustrée ci-dessous.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Étiquette d'inventaire

L'étiquette d'inventaire décrit l'auteur et l'environnement du fichier

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Bibliothèque de caméras

Les ressources COLLADA sont contenues dans des bibliothèques. La bibliothèque de caméras contient sans surprise des caméras. Les caméras courantes sont en perspective ou orthographiques. La balise de bibliothèque de caméra est définie comme suit.
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
### Lumières

Les lumières courantes sont ponctuelles, ponctuelles ou directionnelles
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

### Instance de matériaux

Les effets d'occurrence de matériaux sont définis comme suit.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Effets communs

Les effets communs agissent comme l'état OpenGL 1 et peuvent être définis comme suit.

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

### Attributs de géométrie

La géométrie décrit les attributs OpenGL et est définie comme suit.
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

### Scènes visuelles

Les scènes visuelles sont comme des scènes d'unité et contiennent une hiérarchie de nœuds comme suit.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Références
* [Spécifications COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

