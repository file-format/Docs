
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS 文件 - APK 集存档",
  "description":"了解什么是 APKS 文件？",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## 什么是一 .apks 文件？

带有 .apks 扩展名的文件是一个存档文件，它是 Android 软件包 **APK** 文件的集合。 APKS 文件中的每个单独的 APK 文件都是根据设备的各个方面生成的。这些包括架构、语言、屏幕密度和其他设备功能。 AKS 文件由 **bundletool** 生成。它用于构建 Android App Bundle 并将应用程序包转换为不同的 APK 以部署在设备上。

## AKS 文件格式 - 更多信息

AKS 文件使用 [ZIP](/zh/compression/zip/) 文件格式保存为压缩文件。

## 如何生成APKS文件？

当 Android App Bundle (AAB) 准备就绪时，可以测试其在 Google Play 商店中的行为以部署到设备。为此，可以从 AAB 文件生成 APKS 文件，并使用 Google 的 Android [bundletool](https://developer.android.com/tools/bundletool) 将其安装在测试设备上。它提供了命令行工具来使用以下命令从 APK 创建 APKS 存档文件。

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

为了将 APK 部署到设备，可以使用设备签名信息对 APKS 文件进行签名，如下所示。

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## 参考

* [bundletool - 命令行](https://developer.android.com/tools/bundletool)

