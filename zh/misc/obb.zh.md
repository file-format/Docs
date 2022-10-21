{
  "date" : "2022-02-16",
  "keywords" :[ "obb 文件", "obb 文件格式", "什么是 obb 文件", "file", "obb 示例", "obb 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB 文件格式 - Android 不透明二进制 Blob 文件",
  "description":"了解 OBB 文件格式和可以创建和打开 OBB 文件的 API。",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## 什么是一 .obb 文件？

OBB 文件是一个扩展文件，其中包含除 Android [APK](/zh/compression/apk/) 文件之外的其他数据。 Google Play 商店不允许拥有大小超过 100 MB 的 Android APK 文件。但是，除了 APK 文件之外，某些应用程序可能还需要托管高清图形、媒体文件或其他大型资产。这就是 OBB 文件类型的用武之地。Google Play 允许附加这些扩展文件作为 APK 文件的补充。

## OBB 文件格式

OBB 文件与 APK 文件一起保存为二进制文件。当 APK 随附 OBB 文件时，Google Play 会在其服务器上托管扩展文件，并且不会向开发人员收取额外费用。当下载应用程序进行安装时，这些附加文件将存储在设备的共享存储中 SD 卡或 USB 可挂载分区。

OBB 文件在下载时下载并安装。但在某些情况下，这些是在第一次运行应用程序时下载的以进行安装。

### OBB 最大文件大小

Google Play 商店可让您上传最大 2 GB 的 OBB 扩展文件。建议将大尺寸文件以压缩 [ZIP](/zh/compression/zip/) 文件的形式上传，以便通过 Internet 高效上传。

这些扩展文件可以作为 **main** 主扩展文件托管，用于应用程序所需的额外资源，也可以作为可选补丁扩展文件托管，用于对主扩展文件进行小幅更新。

## 参考

* [Android 开发者 - 扩展文件](https://developer.android.com/google/play/expansion-files)

