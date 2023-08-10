{
  "date" : "2019-10-11",
  "keywords" :[ "file dae", "format file dae", "apa itu file dae", "file", "contoh dae", "ekstensi file dae", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file DAE dan API yang dapat membuka dan membuat file DAE.",
  "title" :"DAE - Format File Pertukaran Aset Digital",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DAE?

File DAE adalah format file Pertukaran Aset Digital yang digunakan untuk bertukar data antara aplikasi 3D interaktif. Format file ini didasarkan pada skema XML COLLADA (COLLAborative Design Activity) yang merupakan skema XML standar terbuka untuk pertukaran aset digital di antara aplikasi perangkat lunak grafis. Ini telah diadopsi oleh ISO sebagai spesifikasi yang tersedia untuk umum, ISO/pAS 17506. File DAE dapat dibuka di aplikasi seperti Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, dan API seperti [Aspose.CAD](https://products.aspose.com/cad/).

## Format File DAE

Format file DAE didasarkan pada [skema COLLADA XML](https://www.khronos.org/files/collada_spec_1_5.pdf) yang semua elemennya didefinisikan sebagai tag XML. Ini memungkinkan pengikatan alat pemrosesan DCC dan 3D yang beragam ke dalam pipa produksi untuk aset 3D. Ini memiliki pengkodean adegan visual yang komprehensif termasuk geometri, animasi, shader dan fisika. Formatnya terbuka, tingkat arsip, dan menyimpan informasi meta.

### COLLADA Tag

Tag skema COLLADA adalah seperti yang ditunjukkan di bawah ini.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Label Aset

Tag aset menjelaskan pembuat dan lingkungan file

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Pustaka Kamera

Aset COLLADA terdapat di dalam perpustakaan. Pustaka kamera berisi kamera yang tidak mengejutkan. Kamera umum adalah perspektif atau ortografi. Tag perpustakaan kamera didefinisikan sebagai berikut.
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
### Lampu

Lampu umum adalah titik, titik atau arah
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

### Instance Material

Efek instance Material didefinisikan sebagai berikut.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Efek Umum

Efek umum bertindak seperti keadaan OpenGL 1 dan dapat didefinisikan sebagai berikut.

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

### Atribut Geometri

Geometri menggambarkan atribut OpenGL dan didefinisikan sebagai berikut.
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

### Pemandangan Visual

Adegan visual seperti adegan kesatuan dan berisi hierarki node sebagai berikut.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referensi
* [Spesifikasi COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

