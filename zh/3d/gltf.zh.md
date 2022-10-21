{
  "date" : "2019-12-12",
  "keywords" :["GLTF","文件","扩展名","格式","3D","Khronos Group 3D"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 GLTF 文件和可以创建和打开 GLTF 文件的 API。",
  "title" :"GLTF - GL 传输文件格式",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .GLTF 文件？

glTF（GL 传输格式）是一种 3D 文件格式，它以 JSON 格式存储 3D 模型信息。 JSON 的使用最大限度地减少了 3D 资产的大小以及解压和使用这些资产所需的运行时处理。它被应用程序用于3D场景和模型的高效传输和加载。 glTF 由 Khronos Group 3D 格式工作组开发，也被其创建者描述为 3D 的 [JPEG](/zh/image/jpeg/)。

GLTF 文件格式为 3D 内容工具和服务定义了一种可扩展的通用发布格式，可简化创作工作流程并实现跨行业内容的互操作使用。创建 glTF 文件格式的目的是为 3D 内容工具和服务定义可扩展的通用发布格式，以简化创作工作流程并实现跨行业内容的互操作使用。它最大限度地减少了使用 WebGL 和其他 API 的应用程序的运行时处理。

## 历史简介

glTF 文件格式 1.0 的第一个规范于 2015 年 10 月宣布。这是 Khronos 于 2012 年 3 月开始的一系列努力。这些努力的目的是评估围绕 WebGL 牵引力的机会。结果，基于 JSON 格式的 glTF 格式的第一个演示在 2012 年的 WebGl 聚会上展示。该格式不时被多家公司采用，包括 Cesium、3D Tiles、Oculus、Microsoft、Archilogic 等。

glTF 2.0 于 2017 年 6 月 5 日在 Web3D 2017 大会上发布。在那之后，有一长串采用 glTF 文件格式的公司。

## GLTF 文件格式

glTF 2.0 的文件格式规范可[在线](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) 供参考，在任何与读/写相关的实现中都应参考以支持glTF 文件格式。

glTF 将资产定义为带有支持外部数据的 JSON 文件。它借助以下工具表示 3D 模型：

* 包含在 JSON 格式的 .glTF 文件中的完整场景描述，其中包括有关节点层次结构、材质、相机的信息，以及网格、动画和其他构造的描述符信息
* 包含几何和动画数据以及其他基于缓冲区的数据的二进制文件 (.bin)
* 用于纹理的图像文件 ([.jpg](/zh/image/jpeg/), [.png](/zh/image/png/))

任何外部资产（例如图像）都存储在通过 URI 引用的外部文件中。这些 URI 与 GLB 容器一起存储，或者使用数据 URI 直接嵌入到 JSON 中。每个有效的 glTF 都必须指定其版本。

glTF 旨在实现小文件大小、快速加载、完整的 3D 场景表示和可扩展性。这些独特的设计目标是 glTF 文件格式在 3D 领域流行的主要原因。以下是 glTF 文件格式支持的不同文件类型的 mime 类型：

* .gltf 文件使用模型/gltf+json
* .bin 文件使用 application/octet-stream
* 贴图文件根据具体图片格式使用官方image/*类型。为了与现代 Web 浏览器兼容，支持以下图像格式：image/jpeg、image/png。

### JSON 编码

glTF 对 JSON 文件格式施加以下附加限制

为了简化客户端实现，glTF 对 JSON 格式和编码有额外的限制。

1. JSON 必须使用没有 BOM 的 UTF-8 编码。
1. 本规范中定义的所有字符串（属性名称、枚举）仅使用 ASCII 字符集，并且必须写为纯文本，例如，“缓冲区"而不是 `"\u0062\u0075\u0066\u0066\u0065\u0072"`。
1. JSON 对象中的名称（键）必须是唯一的，即不允许重复键。

### URI

缓冲区和图像资源通过 URI 引用。客户端必须支持以下两种 URI 类型。

**数据 URI：** 数据 URI 由 RFC 2397 定义，glTF 使用它在 JSON 中嵌入资源。

**相对 URI 路径：** 或 RFC 3986 [第 4.2 节](https://tools.ietf.org/html/rfc3986#section-4.2) 定义的 path-noscheme — 没有方案、权限或参数。根据 RFC 3986 [第 2.2 节](https://tools.ietf.org/html/rfc3986#section-2.2)，保留字符必须是百分比编码的。

## 参考 ＃＃

* [glTF 2.0 规范 - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF 文件格式 - 维基百科提供](https://en.wikipedia.org/wiki/GlTF)

