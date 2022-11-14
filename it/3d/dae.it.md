{
  "date" : "2019-10-11",
  "keywords" :[ "file dae", "formato file dae", "cos'è un file dae", "file", "esempio dae", "estensione file dae", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file DAE e le API che possono aprire e creare file DAE.",
  "title" :"DAE - Formato file di scambio di risorse digitali",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DAE?

Un file DAE è un formato di file Digital Asset Exchange utilizzato per lo scambio di dati tra applicazioni 3D interattive. Questo formato di file si basa sullo schema XML COLLADA (COLLAborative Design Activity), che è uno schema XML standard aperto per lo scambio di risorse digitali tra applicazioni software di grafica. È stato adottato da ISO come specifica pubblicamente disponibile, ISO/pAS 17506. I file DAE possono essere aperti in applicazioni come Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD e API come [Aspose.CAD](https://products .aspose.com/cad).

## Formato file DAE

Il formato del file DAE è basato su [COLLADA XML Schema](https://www.khronos.org/files/collada_spec_1_5.pdf) dove tutti gli elementi sono definiti come tag XML. Consente l'associazione di diversi strumenti di elaborazione DCC e 3D in una pipeline di produzione per risorse 3D. Ha una codifica completa di scene visive tra cui geometria, animazione, shader e fisica. Il formato è aperto, di livello archivio e conserva le metainformazioni.

### COLLADA Tag

Il tag dello schema COLLADA è mostrato di seguito.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Etichetta risorsa

Il tag asset descrive l'autore e l'ambiente del file

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Libreria fotocamera

Le risorse COLLADA sono contenute all'interno delle biblioteche. La libreria delle fotocamere contiene, ovviamente, fotocamere. Le fotocamere comuni sono prospettiche o ortogonali. Il tag della libreria della fotocamera è definito come segue.
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
### Luci

Le luci comuni sono puntiformi, spot o direzionali
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

### Istanza materiali

Gli effetti dell'istanza Materiali sono definiti come segue.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Effetti comuni

Gli effetti comuni agiscono come lo stato OpenGL 1 e possono essere definiti come segue.

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

### Attributi di geometria

La geometria descrive gli attributi OpenGL e definiti come segue.
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

### Scene visive

Le scene visive sono come scene di unità e contengono una gerarchia di nodi come segue.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Riferimenti
* [Specifiche COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

