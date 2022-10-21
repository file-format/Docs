{
  "date" : "2019-10-11",
  "keywords" :["dae 文件","dae 文件格式","什么是 dae 文件","文件","dae 示例","dae 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解可以打开和创建 DAE 文件的 DAE 文件格式和 API。",
  "title" :"DAE - 数字资产交换文件格式",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .dae 文件？

DAE 文件是一种数字资产交换文件格式，用于在交互式 3D 应用程序之间交换数据。此文件格式基于 COLLADA（COLLAborative Design Activity）XML 模式，它是一种开放标准 XML 模式，用于在图形软件应用程序之间交换数字资产。它已被 ISO 采用为公开可用的规范 ISO/pAS 17506。DAE 文件可以在 Adobe Photoshop、AutoDesk Maya、AutoDesk AutoCAD 等应用程序以及 [Aspose.CAD](https://products) 等 API 中打开.aspose.com/cad）。

## DAE 文件格式

DAE 文件格式基于 [COLLADA XML 模式](https://www.khronos.org/files/collada_spec_1_5.pdf)，其中所有元素都定义为 XML 标记。它可以将各种 DCC 和 3D 处理工具绑定到 3D 资产的生产管道中。它具有对视觉场景的全面编码，包括几何、动画、着色器和物理。该格式是开放的、存档级的并保留元信息。

### COLLADA标签

COLLADA 模式标记如下所示。
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
＃＃＃ 资产标签

资产标签描述了文件的作者和环境

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### 相机库

COLLADA 资产包含在库中。毫不奇怪，相机库包含相机。常见的相机是透视或正交的。相机库标签定义如下。
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
＃＃＃ 灯

常见的光源有点光源、聚光源或定向光源
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

### 材质实例

材质实例效果定义如下。
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### 常见效果

常见效果类似于 OpenGL 1 状态，可以定义如下。

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

### 几何属性

Geometry 描述了 OpenGL 属性并定义如下。
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

### 视觉场景

视觉场景就像统一场景，包含如下的节点层次结构。
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## 参考
* [COLLADA 1.5.0 规格](https://www.khronos.org/files/collada_spec_1_5.pdf)

