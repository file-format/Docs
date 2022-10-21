{
  "date" : "2020-03-16",
  "keywords" :["DWG","文件格式","CAD","打开","创建"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DWG 文件格式和可以创建和打开 DWG 文件的 API。",
  "title" :"DWG 文件格式",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .dwg 文件？

带有 DWG 扩展名的文件代表用于包含 2D 和 3D 设计数据的专有二进制文件。与作为 ASCII 文件的 DXF 一样，DWG 代表 CAD（计算机辅助设计）图纸的二进制文件格式。它包含用于表示 CAD 文件内容的矢量图像和元数据。有免费的查看器可用于在 Windows 操作系统上查看 DWG 文件，例如 Autodesk 的免费 DWG TrueView。还有其他第三方应用程序支持访问 DWG 文件。 DWG 文件包含用户创建的信息，包括：

* 设计
* 几何数据
* 地图和照片

这种格式被建筑师、工程师和设计师广泛用于各种设计目的。

## 历史简介 ＃＃

DWG 文件格式自 1982 年正式引入以来随着时间的推移而发展。从历史角度简要概述过去的事件如下。

**1982：** Autodesk 授权使用 Mike Riddle 于 1970 年开发的 DWG 文件格式作为 AutoCAD 的基础。

**1998：** 随着 AutoCAD R14.01 的发布，Autodesk 通过名为 DWGCHECK 的功能添加了文件验证功能，该功能将加密的校验和和产品代码（Autodesk 称为 WaterMark）嵌入到程序创建的 DWG 文件中。

**2006：** Autodesk 修改了 AutoCAD 2007，包括“TrustedDWG 技术"以将文本字符串“Autodesk DWG。此文件是 Autodesk 应用程序或 Autodesk 许可应用程序最后保存的受信任的 DWG"到 DWG 文件中。这样做的目的是帮助 Autodesk 软件用户确保这些文件是由 Autodesk 或 RealDWG 应用程序创建的，这绝对有助于降低不兼容的风险。

## 文件结构##

DWG 已成为一系列应用程序广泛使用的文件格式之一，并且具有强大的文件结构。由于 DWG 是一种二进制文件格式，因此它不像纯 ASCII [DXF](/zh/cad/dxf/) 文件格式那样可读。 DWG 文件通常包含有关图像坐标的信息以及与之关联的任何元数据。 DWG 文件格式的完整 [规格](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) 可供 OpenDesign 下载。 DWG 文件格式的文件结构总结如下。

**标头**：文件标头由 DWG 标头变量和有关用于错误检测的循环冗余校验 (CRC) 的信息组成。每个小节都是一个专门的向量，其中不同长度的位用于表示不同的标签。例如，DWG Header 变量的前 6 位代表版本字符串。

**类定义：** DWG 文件可能包含许多类，具体取决于特定的 .dwg 文件用途。类数据区的类元数据大小、类号和校验和等信息。

**模板**：这是可选的，对于 R15 和 R15 版本，此部分位于对象可用空间部分下方。

**填充**：元数据带有特定字节数的后缀和后缀，这使得旧 AutoCAD 软件版本能够向前兼容新的 DWG 文件格式。

**图像数据**：此部分的元数据取决于特定的 .dwg 类型。对于 R14 和 R15 用户，此部分是可选的。

**对象数据**：对象数据由对应于现有对象列表的表实体、字典条目等的完整列表组成。

**对象映射**：文件中每个对象的位置在此文件部分中指定。本节中的大多数元数据是文件句柄，它们在对象的识别和重新渲染中发挥作用。

**对象可用空间**：此部分对所有用户都是可选的

**第二个标题**：DWG 文件末尾的文件标题部分的副本

## 参考 ＃＃

* [DWG 文件格式规范](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [DWG 文件规范](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - 维基百科](https://en.wikipedia.org/wiki/.dwg)

