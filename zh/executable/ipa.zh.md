{
  "date" : "2021-08-30",
  "keywords" :["ipa 文件","ipa 文件格式","什么是 ipa 文件","文件","ipa 示例","ipa 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 IPA 文件格式和可以创建和打开 IPA 文件的 API。",
  "title" :"IPA - iOS 应用程序包文件",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## 什么是一 .ipa 文件？
带有 .ipa 扩展名的文件属于 iOS，称为应用程序包文件。这是存储 iOS 应用程序的存档（使用 [ZIP](/zh/compression/zip/) 压缩压缩）文件，但该应用程序只能安装在 iOS 或基于 ARM 的 MacOS 设备上，例如 iPad、iPhone 或iPod 触摸。主要是，iTunes、Apple Configurator 2 或任何第三方软件都可以用来安装 IPA 文件。

## 国际音标文件格式
使用 Apple Xcode 开发应用程序的 IOS 开发人员非常熟悉 IPA 文件，因为他们需要将开发的应用程序打包为 IPA 文件，以便测试应用程序商店部署。虽然已知 IPA 文件作为 iOS 应用程序安装，但是，您也可以解压缩它们以查看包含的应用程序数据。由于 IPA 文件只包含一个针对手机 ARM 架构的二进制文件，而它不包含针对 x86 架构的二进制文件，因此许多 .ipa 文件无法在 iPhone 模拟器上安装。
### .ipa 文件的结构
以下示例显示了 IPA 的结构：

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
以上是 iTunes 和 App Store 识别的内置结构。按照这个结构：
- Payload 目录包含所有应用程序数据。
- iTunes Artwork 文件是一个 512×512 像素的 PNG 图像，包含用于在 iTunes 和 iPad 上的 App Store 应用程序中显示的应用程序图标。
- iTunesMetadata.plist 包含各种信息，包括开发者的姓名和 ID、版权信息、捆绑标识符、应用程序名称、流派、发布日期、购买日期等。
- META-INF 文件夹仅包含有关用于创建 IPA 的程序的元数据。


## 参考

* [.ipa - 维基百科](https://en.wikipedia.org/wiki/.ipa)


