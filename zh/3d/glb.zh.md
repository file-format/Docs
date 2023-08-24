{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","文件","格式","文件类型","扩展名","什么是 GLB 文件？" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"了解 GLB 文件格式和可以打开和创建 GLB 文件的 API。",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## 什么是一 .glb 文件？

GLB 是以 GL 传输格式 ([glTF](/zh/3d/gltf/)) 保存的 3D 模型的二进制文件格式表示。有关 3D 模型的信息，例如二进制格式的节点层次结构、相机、材质、动画和网格。这种二进制格式将 glTF 资产（JSON、.bin 和图像）存储在二进制 blob 中。它还避免了在 glTF 的情况下发生的文件大小增加的问题。 GLB 文件格式导致文件大小紧凑、加载速度快、完整的 3D 场景表示以及进一步开发的可扩展性。该格式使用 model/gltf-binary 作为 MIME 类型。

## GLB 文件格式 - 更多信息

glTF 使用的内容交付方法导致对 base-64 编码的二进制数据进行解码的额外处理，并且还将文件大小增加了 33%。这些交付方式促成了 GLB 文件格式的形成，包括：

* glTF JSON 指向外部二进制数据（几何、关键帧、皮肤）和图像。
* glTF JSON 嵌入 base64 编码的二进制数据，并使用数据 URI 内联图像。

GLB 作为一种容器格式被引入为二进制文件格式，用于在二进制 blob 中表示 glTF 资产，以避免由 glTF 引起的问题。 GLB 文件格式 [规范](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) 应参考用于应用程序开发的任何读取器/写入器实现.

## GLB 文件结构

GLB文件格式是基于little endian的，其结构表明它包含：

* 一个 12 字节的前导码，标题为标题。
* 一个或多个包含 JSON 内容和二进制数据的块。

#### 标题

GLB 文件格式标头由三个 4 字节条目组成：

* uint32 魔法 - 魔法等于 0x46546C67。它是 ASCII 字符串 glTF，可用于将数据识别为二进制 glTF
* uint32 version - 表示 Binary glTF 容器格式的版本
* uin32 length - Binary glTF 的总长度，包括 Header 和所有块（以字节为单位）

#### 块

GLB 文件中的每个块都具有以下结构：

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - chunkData 的字节长度
* `chunkType` - 表示块的类型
* `chunkData` - 块的二进制有效载荷

块类型是：

|# |块类型|ASCII|描述|出现次数
---|---|---|---|---|
|1.|0x4E4F534A|JSON|结构化 JSON 内容|1
|2.|0x004E4942|BIN|二进制缓冲区|0 或 1

每个块的开始和结束必须与 4 字节边界对齐，为此应使用填充。

##### 结构化 JSON 内容

这应该是二进制 glTF 资产的第一个块，并使实现能够从后续块中逐步检索资源。这还提供了从二进制 glTF 资产（例如网格的最粗略 LOD）中仅读取选定资源子集的能力。为了满足对齐要求，这个块必须用尾随空格字符（0x20）填充。

##### 二进制缓冲区#####

该块包含几何、动画关键帧、皮肤和图像的二进制有效负载。它应该是二进制 glTF 资产的第二个块，并且必须用尾随零 (0x00) 填充以满足对齐要求。

## 参考 ＃＃

* [GLB 文件格式规范 - Khronos](/zh/3d/gltf/)

