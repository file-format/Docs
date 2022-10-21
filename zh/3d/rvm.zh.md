{
  "date" : "2019-10-11",
  "keywords" :["rvm 文件","rvm 文件格式","什么是 rvm 文件","文件","rvm 示例","rvm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RVM - AVEVA PDMS 项目文件",
  "description":"了解 RVM 文件格式和可打开和创建 RVM 文件的 API。",
  "linktitle" : "RVM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## 什么是 .rvm 文件？

**RVM** 数据文件与 AVEVA PDMS 相关。 **RVM** 文件是 AVEVA 工厂设计管理系统模型项目文件。 AVEVA 的工厂设计管理系统 (PDMS) 是最流行的 3D 设计系统，它使用以数据为中心的技术来管理项目。许多应用程序可用于打开 RVM 文件并将其转换为其他格式，例如 [3DS](/zh/3d/3ds/)。

## RVM 文件格式

除了可以以二进制和 ASCII 格式保存之外，没有太多关于 RVM 文件格式的详细信息。 RVM 文件支持以下实体：

*所有几何
* 存储在组上的属性
* 纹理（通过 RVS 文件）
* 摄像机和摄像机轨道（通过 RVS 文件）
* 裁剪平面（通过 RVS 文件）
* 标志（通过 RVS 文件）
* 标签（通过 RVS 文件）
* 标签（通过 RVS 文件）
* 半透明（通过 RVS 文件）
* PDMS 原点

## 参考

* [RVM 解析器](https://github.com/cdyk/rvmparser)

