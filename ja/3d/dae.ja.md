{
  "date" : "2019-10-11",
  "keywords" :[ "dae ファイル", "dae ファイル形式", "dae ファイルとは", "ファイル", "dae の例", "dae ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"DAEファイルを開いて作成できるDAEファイル形式とAPIについて学びます。",
  "title" :"DAE - デジタル資産交換ファイル形式",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .DAE オプション番号

DAE ファイルは、インタラクティブな 3D アプリケーション間でデータを交換するために使用される Digital Asset Exchange ファイル形式です。このファイル形式は、グラフィック ソフトウェア アプリケーション間でデジタル アセットを交換するためのオープン スタンダード XML スキーマである COLLADA (COLLAborative Design Activity) XML スキーマに基づいています。これは、公開されている仕様 ISO/pAS 17506 として ISO によって採用されています。DAE ファイルは、Adobe Photoshop、AutoDesk Maya、AutoDesk AutoCAD などのアプリケーション、および [Aspose.CAD](https://products .aspose.com/cad)。

## DAE ファイル形式

DAE ファイル形式は、すべての要素が XML タグとして定義されている [COLLADA XML スキーマ](https://www.khronos.org/files/collada_spec_1_5.pdf) に基づいています。これにより、さまざまな DCC および 3D 処理ツールを 3D アセットの制作パイプラインにバインドできます。ジオメトリ、アニメーション、シェーダー、物理などのビジュアル シーンを包括的にエンコードします。形式はオープンで、アーカイブ グレードであり、メタ情報を保持します。

### コラーダタグ

COLLADA スキーマ タグは次のとおりです。
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
＃＃＃ アセットタグ

資産タグは、ファイルの作成者と環境を記述します

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### カメラ ライブラリ

COLLADA アセットはライブラリ内に含まれています。カメラ ライブラリには、当然のことながら、カメラが含まれています。一般的なカメラは、遠近法または正投影です。カメラ ライブラリ タグは次のように定義されます。
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
＃＃＃ ライト

一般的なライトは、ポイント、スポット、またはディレクショナルです
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

### マテリアル インスタンス

マテリアル インスタンスの効果は次のように定義されます。
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### 一般的な効果

一般的な効果は、OpenGL 1 の状態のように機能し、次のように定義できます。

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

### ジオメトリ属性

Geometry は OpenGL の属性を記述し、次のように定義されます。
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

### ビジュアルシーン

ビジュアル シーンはユニティ シーンのようなもので、次のようなノードの階層が含まれています。
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## 参考文献
* [COLLADA 1.5.0 仕様](https://www.khronos.org/files/collada_spec_1_5.pdf)

