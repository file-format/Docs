{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM 文件 - Adobe Edge Animate Widget 文件格式",
  "description" :"了解什么是 OAM 文件以及可以创建和打开 OAM 文件的 API。",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## 什么是一 .oam 文件？

.oam 文件是从 Adobe Edge Animate Widget 导出的动画小部件文件。导出为 OAM 小部件文件格式的动画可以插入到其他 Adobe 应用程序中，例如 InDesign Documents（[INDD 文件](/zh/page-description-language/indd/)、Dreamweaver 和 Muse。OAM 文件就像可以轻松部署的部署包）插入到其他 Adobe 项目中以使用它们。OAM 文件包含有关动画资源、行为和动作脚本代码的信息。您可以通过发布 Adobe Animate 项目 [.AN 文件](/zh/web/an/) 来创建 OAM 文件。
用户可以通过从 Edge Animate 项目（.AN 文件）发布来创建 OAM 文件。

## OAM 文件格式

OAM 文件作为压缩 [ZIP](/zh/compression/zip/) 存档保存到光盘。这意味着您可以将文件扩展名重命名为 .zip 并使用任何压缩实用程序（例如 WinZIP 或 WinRAR）进行解压。文件大小的减小使得通过互联网与其他用户传输和共享动画变得更加容易。

### OAM 文件结构

.oam 文件的内部文件结构是专有的，Adobe 未公开记录。然而，众所周知，.oam 文件包含打包到单个文件中的文件和资源（例如图形、音频和 ActionScript 代码）的集合。 .oam 文件的内容可能包括 [XML](/zh/web/xml/) 文件、SWF 文件和其他资源文件。 .oam 文件的确切结构取决于用于创建它的 Adobe Animate 的特定版本，以及文件中包含的动画和资源的类型。

OAM 文件包含以下信息。

`资产：` 有关动画中使用的图形、音频和视频资产的信息。

`行为：` 动画中发生的动作和交互的描述。

`ActionScript 代码：` 用于控制动画的行为和交互性的代码。

`发布设置：` 有关发布动画的平台和格式的信息，例如 HTML5 或 AIR。

`元数据：` 附加信息，例如动画的作者、创建日期和版本号。

## 如何打开 OAM 文件？

您可以使用以下应用程序打开 OAM 文件。

* Adobe Edge Animate CC（已停产）
* Adobe 动画 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## 参考

* [OAM 发布](https://helpx.adobe.com/animate/using/OAM-publishing.html)

