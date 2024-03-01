{
  "date": "2019-10-11",
  "keywords": [
"dae tiedosto",
"dae tiedostomuoto",
"mikä on dae-tiedosto",
"tiedosto",
"dae esimerkki",
"dae tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DAE-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda DAE-tiedostoja.",
  "title": "DAE - Digital Asset Exchange -tiedostomuoto",
  "linktitle": "DAE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-da-fie"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DAE-tiedosto?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE-tiedostoja voidaan avata sovelluksissa, kuten Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD ja API, kuten [Aspose.CAD](https://products.aspose.com/cad/).

## DAE tiedostomuoto

DAE-tiedostomuoto perustuu {{HYPERLINKKI}}, jossa kaikki elementit on määritelty XML-tunnisteiksi. Se mahdollistaa erilaisten DCC- ja 3D-käsittelytyökalujen sitomisen 3D-resurssien tuotantoputkeen. Siinä on kattava visuaalisten kohtausten koodaus, mukaan lukien geometria, animaatio, varjostimet ja fysiikka. Muoto on avoin, arkistolaatuinen ja säilyttää metatiedot.

### COLLADA-tunnisteet

COLLADA-skeeman tunniste on seuraavanlainen.
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

Omaisuustunniste kuvaa tiedoston tekijän ja ympäristön

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamerakirjasto

COLLADA-varat ovat kirjastojen sisällä. Kamerakirjasto sisältää yllättäen kameroita. Yleisimmät kamerat ovat perspektiivi- tai ortografisia. Kamerakirjaston tunniste määritellään seuraavasti.
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
### Valot

Yleiset valot ovat piste-, piste- tai suuntavalot
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

### Materiaaliinstanssi

Materiaalien ilmentymän vaikutukset määritellään seuraavasti.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Yleisiä vaikutuksia

Yleiset tehosteet toimivat kuten OpenGL 1 -tila, ja ne voidaan määritellä seuraavasti.

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

### Geometrian attribuutit

Geometria kuvaa OpenGL-attribuutit ja määritellään seuraavasti.
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

### Visuaaliset kohtaukset

Visuaaliset kohtaukset ovat kuin yhtenäiskohtauksia ja sisältävät seuraavan solmuhierarkian.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Viitteet
 * [COLLADA 1.5.0:n tekniset tiedot](https://www.khronos.org/files/collada_spec_1_5.pdf)

