{
  "date" : "2019-12-09",
  "keywords" :["3mf 文件","3mf 文件格式","什么是 3mf 文件","文件","3mf 示例","3mf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"了解 3MF 文件格式和可以打开和创建 3MF 文件的 API。",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## 什么是 3MF 文件？

3MF（3D 制造格式）被应用程序用于将 3D 对象模型渲染到各种其他应用程序、平台、服务和打印机。它旨在避免其他 3D 文件格式的限制和问题，例如 [STL](/zh/cad/stl/)，用于使用最新版本的 3D 打印机。 3MF 是一种相对较新的文件格式，由 3MF 联盟开发和发布。它足够丰富，可以完全描述模型，保留内部信息、颜色和其他特征，使其可扩展以支持 3D 打印的新创新。该格式是可扩展的，能够被广泛采用并且没有困扰其他广泛使用的文件格式的问题。

## 历史简介 ＃＃

可用模型描述文件格式（如 STL 等）的现有限制导致领先品牌齐心协力，为 3D 打印制定更具扩展性的文件格式。一个重要的考虑因素是应用程序应如何将模型数据传递给 3D 打印机。因此，3MF 联盟应运而生，以支持一种名为 3MF 的新 3D 文件格式，旨在使其具有足够的可扩展性以满足 3D 打印的需求。包括微软、欧特克、达索系统、Netfabb、SLM、惠普等在内的几家公司都是该联盟的成员。 Microsoft 捐赠了其正在进行的 3D 文件格式工作，作为 3MF 联盟协作进一步开发该规范的起点。

## 3MF 文件格式 - 更多信息

3MF 是一种基于 XML 的数据格式——人类可读的压缩 XML——包括与 3D 制造相关的数据的定义，包括自定义数据的第三方可扩展性。 3MF 文件格式的设计考虑到其他 3D 文件格式面临的限制和问题。这导致了 3MF 文件格式的制定，即：

* **完整：** 在一个档案中包含所有必要的模型、材料和属性信息
* **人类可读：** 使用 OPC、[ZIP](/zh/compression/zip/) 和 XML 等通用结构来简化开发
* **简单：** 一个简短、清晰的规范，使开发变得容易和快速验证
* **可扩展：** 利用 XML 命名空间允许公共和私有扩展，同时保持兼容性
* **明确：**清晰的语言和一致性测试确保文件从数字到物理始终保持一致
* **免费：** 3MF 规范的访问和实施将永远免版税、专利和许可

3MF 文件格式的规范托管在 [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) 上，以供公众访问和持续更新。当前发布的版本是 1.2.3，它描述了使用 XML 和其他广泛可用的技术来描述一个或多个 3D 模型的内容和外观的一组约定。想要构建处理 3MF 文件格式的系统的开发人员可以参考这些规范来实现。

## 文件格式规范##

3MF 文件格式使用 ZIP 存档形式的开放打包规范作为其物理模型。它包括一组定义明确的部分和关系，这些部分和关系可以满足文档中的特定目的。这也使格式遵循包括数字签名和缩略图在内的包功能。

### 3MF 文件###

典型的 3MF 文档如下所示：

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

有效载荷包括处理 3D 模型部件所需的全套部件。用于制造 3D 有效负载中描述的对象的所有内容必须包含在 3MF 文档中。下表给出了每个文档部分的描述及其状态作为必需或选项。


|**名称**|**描述**|**关系来源**|**必填/可选**
--- | --- | --- | ---
|3D 模型|包含一个或多个用于制造的 3D 对象的描述。|包|必填
|核心属性|包含各种文档属性的 OPC 部分。|包|可选
|数字签名来源|作为包中数字签名根的 OPC 部分。|包|可选
|数字签名|每个都包含一个数字签名的 OPC 部分。|数字签名来源|可选
|数字签名证书|包含数字签名证书的 OPC 部分。|数字签名|可选
|PrintTicket|提供在 3D 模型部件中输出 3D 对象时使用的设置。|3D 模型|可选
|缩略图|包含一个小的 JPEG 或 PNG 图像，代表包中的 3D 对象或整个包。|包|可选
|3D 纹理|包含用于将颜色应用于 3D 模型部分中的 3D 对象的纹理（可用于扩展）|3D 模型|可选
|自定义部件|与元数据关联的 OPC 部件|包|可选

[部件和关系](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships)、[3D 模型](https:// /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models)，[对象资源](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [材料资源](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) 和 [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) 部分的规范文档提供有关 3MF 文档的详细信息。

## 参考 ＃＃

* [3MF 文件格式规范](https://github.com/3MFConsortium/spec_core)
* [3MF - 维基百科提供](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

