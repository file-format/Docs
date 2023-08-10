{
  "date" : "2019-10-11",
  "keywords" :[ "fișier dae", "format fișier dae", "ce este un fișier dae", "fișier", "exemplu dae", "extensie fișier dae", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier DAE și despre API-urile care pot deschide și crea fișiere DAE.",
  "title" :"DAE – Format de fișier pentru schimbul de active digitale",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DAE?

Un fișier DAE este un format de fișier Digital Asset Exchange care este utilizat pentru schimbul de date între aplicații 3D interactive. Acest format de fișier se bazează pe schema XML COLLADA (COLLAborative Design Activity) care este o schemă XML standard deschisă pentru schimbul de active digitale între aplicațiile software de grafică. Acesta a fost adoptat de ISO ca o specificație disponibilă public, ISO/pAS 17506. Fișierele DAE pot fi deschise în aplicații precum Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD și API-uri precum [Aspose.CAD](https://products.aspose.com/cad/).

## Format de fișier DAE

Formatul de fișier DAE se bazează pe [schema XML COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf) unde toate elementele sunt definite ca etichete XML. Permite legarea diverselor instrumente de procesare DCC și 3D într-o conductă de producție pentru active 3D. Are codificare completă a scenelor vizuale, inclusiv geometrie, animație, shadere și fizică. Formatul este deschis, arhivă și păstrează metainformații.

### Etichete COLLADA

Eticheta de schemă COLLADA este așa cum se arată mai jos.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Etichetă de bun

Eticheta de material descrie autorul și mediul fișierului

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Biblioteca camerei

Activele COLLADA sunt conținute în biblioteci. Biblioteca de camere conține, fără a fi surprinzător, camere. Camerele obișnuite sunt de perspectivă sau ortografice. Eticheta bibliotecii camerei este definită după cum urmează.
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
### Lumini

Luminile comune sunt punctuale, spot sau direcționale
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

### Materiale Instanță

Efectele instanței Materiale sunt definite după cum urmează.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Efecte comune

Efectele comune acționează ca starea OpenGL 1 și pot fi definite după cum urmează.

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

### Atribute geometrie

Geometria descrie atributele OpenGL și este definită după cum urmează.
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

### Scene vizuale

Scenele vizuale sunt ca scenele unitare și conțin o ierarhie de noduri, după cum urmează.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referințe
* [Specificații COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

