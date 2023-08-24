{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz 文件", "usdz 文件格式", "文件格式", "3d","usdz 文件下载"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - 通用场景描述 ZIP 格式",
  "description":"了解 USDZ 文件格式和可以打开和创建 USDZ 文件的 API。",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## 什么是一 .USDZ 文件？

带有 .usdz 的文件是 [USD](/zh/3d/usd/)（通用场景描述）文件格式的未压缩且未加密的 ZIP 存档，其中包含嵌入其中的其他格式（例如纹理和动画）文件的代理和代理存档并直接使用 USD 运行时运行它们，无需解包。 USDZ 文件是其设计基于包的新 Ar 级抽象的包。 Usdz 已在 IANA 注册，媒体类型名称为 model，子类型名称为 vnd.usd+zip，其详细信息可在 [IANA 注册页面](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip)。

## USDZ 文件格式

USDZ 文件基于 ZIP 文件格式，可在其容器中存档单个文件。这使得接收端只需解压缩内容并使用普通的 USD 场景描述文件进行处理和检查。几乎所有操作系统都提供对 ZIP 文件格式的内置支持，并且选择这种归档格式而不是任何自定义方法使得 USDZ 文件很容易用作简单的传输协议。

### ZIP 约束

USDZ 文件格式使用没有任何“压缩"和“加密"的 ZIP 文件格式。这在设计上旨在满足两个要求：

* 对于已经加载到内存中或作为磁盘上的单个文件的包，API 以美元提供，用于访问图像中包含的数据
* 无需将文件提取到磁盘或分配更多堆存储

使用 USDZ，这两个要求都得到了满足，因为大多数图像格式本身都允许内部压缩方案，从而产生紧凑的文件大小。

### 布局要求

USDZ 包要求包内文件的布局是每个文件的数据应该从包开头的 64 字节的倍数开始。但是，包应该以原生 [USD](/zh/3d/usd/) 文件开头，以防使用简单参考来定位包。在这种情况下，第一个 USD 文件称为默认层。希望交付“可流式内容"的客户也可能希望考虑其他布局约束。

## USDZ 文件下载
由于 usdz 文件与其他高质量图像和 usd 文件打包在一起，它们可以占用更大的磁盘存储空间。在这里您可以找到一个简单且较小的 USDZ 示例文件以供下载：

- [Sample.usdz](../sample.usdz)

## 参考

* [USDZ 文件格式规范](https://openusd.org/release/spec_usdz.html)
