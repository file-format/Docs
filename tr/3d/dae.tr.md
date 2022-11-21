{
  "date" : "2019-10-11",
  "keywords" :[ "dae dosyası", "dae dosya biçimi", "dae dosyası nedir", "dosya", "dae örneği", "dae dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"DAE dosya formatı ve DAE dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"DAE - Dijital Varlık Değişim Dosyası Formatı",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## DAE dosyası nedir?

DAE dosyası, etkileşimli 3B uygulamalar arasında veri alışverişi için kullanılan bir Dijital Varlık Değişimi dosya biçimidir. Bu dosya formatı, grafik yazılım uygulamaları arasında dijital varlıkların değiş tokuşu için açık standart bir XML şeması olan COLLADA (COLLAborative Design Activity) XML şemasına dayanmaktadır. ISO tarafından halka açık bir spesifikasyon olan ISO/pAS 17506 olarak benimsenmiştir. DAE dosyaları Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD gibi uygulamalarda ve [Aspose.CAD](https://products) gibi API'lerde açılabilir. .aspose.com/cad).

## DAE Dosya Biçimi

DAE dosya biçimi, tüm öğelerin XML etiketleri olarak tanımlandığı [COLLADA XML şemasına](https://www.khronos.org/files/collada_spec_1_5.pdf) dayalıdır. Çeşitli DCC ve 3B işleme araçlarının 3B varlıklar için bir üretim boru hattına bağlanmasını sağlar. Geometri, animasyon, gölgelendiriciler ve fizik dahil olmak üzere kapsamlı görsel sahne kodlamasına sahiptir. Biçim açıktır, arşiv düzeyindedir ve meta bilgileri tutar.

### COLLADA Etiketleri

COLLADA şema etiketi aşağıda gösterildiği gibidir.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Varlık Etiketi

Varlık etiketi, dosyanın yazarını ve ortamını tanımlar

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Kamera Kitaplığı

COLLADA varlıkları kitaplıkların içinde bulunur. Kamera kitaplığı şaşırtıcı olmayan bir şekilde kameralar içerir. Yaygın kameralar perspektif veya ortografiktir. Kamera kitaplığı etiketi aşağıdaki gibi tanımlanır.
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
### Işıklar

Ortak ışıklar nokta, spot veya yönlüdür
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

### Malzeme Örneği

Materials örnek efektleri aşağıdaki gibi tanımlanır.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Ortak Etkiler

Ortak efektler, OpenGL 1 durumu gibi davranır ve aşağıdaki gibi tanımlanabilir.

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

### Geometri Nitelikleri

Geometri, OpenGL özniteliklerini açıklar ve aşağıdaki gibi tanımlanır.
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

### Görsel Sahneler

Görsel sahneler, birlik sahneleri gibidir ve aşağıdaki gibi bir düğüm hiyerarşisi içerir.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referanslar
* [COLLADA 1.5.0 Spesifikasyonları](https://www.khronos.org/files/collada_spec_1_5.pdf)

