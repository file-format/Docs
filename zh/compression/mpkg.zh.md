{
  "date" : "2019-10-11",
  "keywords" :["mpkg 文件","mpkg 文件格式","什么是 mpkg 文件","文件","mpkg 示例","mpkg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG 文件格式 - 元包文件",
  "description":"了解 MPKG 文件格式和可以创建和打开 MPKG 文件的 API。",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## 什么是一 .mpkg 文件？

带有 .mpkg 扩展名的文件是一个存档安装程序文件，主要在 MacOS 操作系统上找到。它包含应用程序所需的所有安装文件，无需单独保存相关文件。除了其他文件之外，单个 MPKG 文件还可以包含包文件 [PKG](/zh/compression/pkg/) 作为安装文件之一。 MPKG 文件不能用任何通用软件打开，在 MacOS 上使用 Apple Installer 自动执行。

## MPKG 文件格式

MPKG 文件包含安装它所包含的多个软件包所需的不同类型的文件。从下图中可以看出这是一个示例 MPKG 文件的树结构。在 MacOS 终端上使用 `tree` 命令导出此树结构。

{{< figure src="../mpkg.png" alt="MPKG 文件格式" >}}

图像中不同元素的描述如下。

`Packages Directory` - 存放pkg文件的列表，即子Packages的列表
`Resources Directory` - 存放 pkg 使用的资源，如本地化资源和图片、Rtf 文档、pdf 文档等。
`Distribution.dist file` - 一个 xml 文档，包含要安装的子包和运行时脚本等信息

MPKG 文件的示例 XML 文件可能如下所示，具体取决于关联的子包。

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/zh/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - 是要安装的子包。它是 Bundle 结构的 pkg 格式的目录。它包含一个 Contents 子目录。

## 参考

* [OSX 平面包](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG 包管理器](https://github.com/puellavulnerata/mpkg)

