{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","file", "format", "file type", "extension","什么是 ASE 文件？" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 ASE 文件格式和可以打开和创建 ASE 文件的 API。",
  "title" :"ASE - Autodesk ASCII 场景导出文件",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## 什么是一 .ASE 文件？

具有 .ase 扩展名的文件是 Autodesk ASCII 场景导出文件格式，它是场景的 ASCII 表示，在使用 Autodesk 导出场景数据时包含 2D 或 3D 信息。 Autodesk 提供了在导出场景数据时包含场景组件的选项。您可以包括网格定义以及顶点和面信息、材质描述、对象的变换动画数据、每 n 帧的完整网格定义、相机和灯光的动画数据以及 IK 关节设置。

## ASE 文件格式 - 更多信息

ASE 文件是以 ASCII 格式存储的文本文件，可以在任何文本编辑器中打开。 ASE 文件可以包含 Autodesk 提供的以下类型的信息。

### 输出选项

* `Mesh Definition` - 导出每个网格的定义，包括几何对象的顶点和面信息。此外，打开此选项可启用“网格选项"组框中的项目，如下所述。
* `材料` - 包括材料描述。如果未将材质指定给对象，则会导出其线框颜色。包含材质树的所有级别，因此可以生成大量文本。
* `Transform Animation Keys` - 包括对象的变换动画数据。如果对象是目标相机或聚光灯，这将包括目标动画数据。
* `Animated Mesh` - 导出每 n 帧的完整网格定义。频率由控制器输出微调器指定，如下所述。每个块都包含在 Mesh Options 组框中指定的相同信息，如下所述。启用此功能可能会导致文件很大，即使对于小场景也是如此。
* `动画摄影机/灯光设置` - 导出摄影机和灯光的动画数据，例如颜色、强度、衰减、贴图偏差等。每 n 帧输出一个块，由控制器输出微调器指定。
* `Inverse Kinematic Joints` - 导出层次分支中的 IK 关节设置。

### 对象类型

此处的项目可让您指定要包含在输出中的对象类别。您可以包括几何对象、形状、相机、灯光和辅助对象。

* 几何的
* 形状
* 相机
* 灯
* 帮手

### 网格选项

* `Mesh Normals` - 导出面和顶点法线。首先列出面的法线，然后是支撑面的三个顶点的法线。打开它会产生一个更大的文件。
* `Mapping Coordinates` - 根据 3ds Max 软件开发工具包中描述的 TVert 和 TVFace 结构，导出映射顶点和面的列表。如果对象使用面贴图，则会导出一个面贴图列表，其中包含每个面的 UVW 坐标。
* `Vertex Colors` - 导出顶点颜色。

### 控制器输出

* `Use Keys` - 导出键值。如果控制器不使用键，则使用强制采样方法。对于变换控制器，仅当所有变换控制器都是线性/TCB 或 Bezier 时，“使用键"选项才有效。如果其中一个变换轨道使用不同类型的控制器，则强制采样方法用于所有变换轨道。
* `Force Samples` - 根据 Frames per Sample Controller 中指定的频率对控制器值进行采样。

## 参考

* [Autodesk - 导出为 ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

