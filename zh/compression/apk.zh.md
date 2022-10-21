{
  "date" : "2019-10-11",
  "keywords" :[ "apk 文件", "apk 文件格式", "什么是 apk 文件", "文件", "apk 示例", "apk 文件扩展名", "扩展名", "格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - 什么是 APK 文件？",
  "description":"了解什么是 APK 文件以及可以创建和打开 APK 文件的 API。",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## 什么是 APK 文件？

带有 .apk 扩展名的文件是一个 Google Android 应用程序文件，用于在 Android 设备上安装应用程序（应用程序）。它使用官方 IDE Google Android Studio 创建为可执行文件，并上传到 Google Play 商店以供最终用户下载和安装。在发布到 Google Play 商店之前，可以生成 APK 文件并使其可用于手动安装。这有助于测试生成的 APK 包文件的功能和行为。因此，需要确保 APK 文件来自受信任的来源并且不包含任何恶意软件。

## APK 文件格式

APK 文件以 [ZIP](/zh/compression/zip/) 文件格式压缩打包，可以使用任何 ZIP 文件打开软件打开。此类文件的 .apk 扩展名可以重命名为 .zip 并在任何 ZIP 应用程序中打开该文件或提取其内容。

## APK 包内容

单个 APK 文件包含安装和执行所需的所有必要文件。使用 ZIP 应用程序提取的 APK 文件包含以下文件和文件夹。

* `META-INF/`：包含清单文件、签名和存档中资源列表的目录
* `lib/`：包含与特定平台相关的编译代码的目录，例如 armeabi-v7a、x86、arm64-v8a 等。
* `res/`: 包含图片等非编译资源的目录
* `assets/`：包含应用程序资产的目录，可由 AssetManager 检索。
* `androidManifest.xml`：包含APK文件的名称、版本信息和内容
* `classes.dex`：这些是编译后的 Java 类，可以在 Dalvik 虚拟机和 Android 运行时运行
* `resources.arsc`：编译后的资源文件，如字符串

## 如何在 Android 设备上安装 APK 文件？

为了在您的 Android 设备上安装 APK 文件，可以使用以下步骤。

1.使用网络浏览器下载APK
2. 点击它——然后您应该能够在设备的顶部栏中看到它正在下载
3. 下载后，打开下载，点击 APK 文件，并在出现提示时点击是。

按照这些步骤将开始在您的设备上安装应用程序。

## 参考

* [APK 文件格式](https://en.wikipedia.org/wiki/Android_application_package)

