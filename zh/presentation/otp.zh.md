{
  "date" : "2021-01-21",
  "keywords" :["otp 文件","otp 文件格式","什么是 otp 文件","文件","otp 示例","otp 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument 演示模板",
  "description":"了解 OTP 文件格式和可以创建和打开 OTP 文件的 API。",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## 什么是一 .otp 文件？

具有 .otp 扩展名的文件表示由应用程序以 OASIS OpenDocument 标准格式创建的演示模板文件。这种文件的内容包括幻灯片形式的演示信息，包括文本、图像、形状、多媒体内容、过渡效果和其他幻灯片元素。这些模板文件用于根据存储在模板本身中的样式信息快速创建新的演示文稿。 OTP 文件可以使用几个不同的应用程序创建和保存，例如 OpenOffice 套件和 Microsoft PowerPoint 附带的 Impress。 OTP 文件格式类似于 Microsoft PowerPoint 模板文件 [.pot](/zh/presentation/pot/) 和 [.potx](/zh/presentation/potx/)。

## 一次性密码文件格式

OTP 文件格式基于 OpenDocument 标准，该标准支持将文档表示为单个 XML 文档以及以 [ZIP](/zh/compression/zip/) 格式在单个压缩包中收集多个子文档。文件内容分布在打包在一起的多个xml文件中。这些多个 [XML](/zh/web/xml/) 文件包含有关样式、内容、元信息和文档设置的信息，如下所述。

* `content.xml` - 文档内容和内容中使用的自动样式。
* `styles.xml` - 文档内容中使用的样式和样式本身中使用的自动样式。
* `meta.xml` - 文档元信息，例如作者或上次保存操作的时间。
* `settings.xml` – 特定于应用程序的设置，例如窗口大小或打印机信息。

## 参考

* [OpenDocument - 维基百科提供](https://en.wikipedia.org/wiki/OpenDocument)

