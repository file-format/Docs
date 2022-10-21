{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","什么是arsc文件","如何打开arsc文件","扩展名","文件","arsc文件","arsc文件格式","arsc文件扩展名", "arsc 文件示例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android 包资源表文件",
  "description":"了解 ARSC 文件格式和可以创建和打开 ARSC 文件的 API。",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## 什么是一 .arsc 文件？

ARSC 文件是一个 Android 资源表文件，它以表格格式包含应用程序的资源列表。这包含资源名称、属性和 ID 等信息。 ARSC 文件是用于安装这些 Android 应用程序的 APK 包的一部分。生成 APK 文件时，Android 应用程序中的所有资源（如图像、布局、样式和字符串）都会转换为二进制文件。同时还生成了 ARSC 文件，其中包含所有程序已编译资源及其 ID 的列表。

## ARSC 文件格式

.arsc 扩展文件是编译器（如 ANT (Eclipse) 或 Gradle (AS)）编译 Android 应用程序代码生成 [APK](/zh/compression/apk/) 文件后生成的二进制文件。您可以使用任何归档工具（如 WinZip）提取 APK 文件以查看其内容，即编译后的 java 类文件，即 classes.dex。除了这些之外，它还包含此 ARSC 文件，其中包含有关以下内容的元信息：

* XML 节点
* 属性
* 资源 ID

APK 文件中的资源由资源 ID 引用，而属性在运行时被解析为一个值。 Android aapt 工具在构建时收集文件中定义的所有资源，并为它们分配资源 ID。将标识符分配给已编译资源后，会从源代码以及 resources.arsc 生成一个 R.java 文件。

## 参考

* [二进制资源表结构](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

