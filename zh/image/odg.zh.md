{
  "date" : "2019-10-11",
  "keywords" :["odg 文件","odg 文件格式","什么是 odg 文件","文件","odg 示例","odg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG 文件格式",
  "description":"了解 ODG 文件格式和可以创建和打开 ODG 文件的 API。",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .odg 文件？

Apache OpenOffice 的 Draw 应用程序使用 ODG 文件格式将绘图元素存储为矢量图像。它遵循结构信息标准推进 (OASIS) 概述的基于 XML 的文件格式规范。 ODG 将绘图表示为使用点、线和曲线的矢量图像。除了 OpenOffice，LibreOffice 和其他应用程序还提供对 ODG 文件格式的支持。例如，OpenOffice 支持的其他格式包括 [ODT](/zh/word-processing/odt/)、ODF、[ODP](/zh/presentation/odp/) 和 [ODS](/zh/spreadsheet/ods/)。


## ODG 文件格式规范

ODG 文件格式基于 OpenDocument 格式，该格式是具有良好定义架构的结构化 XML 文档格式。
OpenDocument 格式的每个结构组件都由具有关联属性的元素表示。基于 XML 的结构适用于所有文档类型，例如文本文档、电子表格或绘图文件。一个文档可以包含不同的样式。 OpenDocument 文件结构由以下元素组成。
* 文档根目录
* 文档元数据
* 正文元素和文档类型
* 应用程序设置
* 脚本
* 字体声明
* 样式
*页面样式和布局

## 文档根##

文档根元素包含整个文档，并且是 OpenDocument 格式文件的主要元素。相同类型的文档根元素适用于所有类型的文档，例如文本、文档、电子表格和绘图文档。

### 根元素###
单个 XML 文档由其自己的根元素表示。五个不同的支持根元素如下。

`<office:document>` - 单个XML 文档中的完整办公文档。
`<office:document-content>` - 文档内容和内容中使用的自动样式。
`<office:document-styles>` - 文档内容中使用的样式和样式本身中使用的自动样式。
`<office:document-meta>` - 文档元信息，例如作者或上次保存操作的时间。
`<office:document-settings>` - 特定于应用程序的设置，例如窗口大小或打印机信息。

### ODG 文档元数据###
OpenDocument 包含 中的所有元数据元素 \<office:meta>元素。有关文档的一般信息包含在文档的开头，应用程序可以更新相同元素的多个实例。

### 正文元素和文档类型###
文档正文使用文档类型元素指示文档中包含的内容类型。这些文档类型是：
* 文本文件
* 绘图文件
* 演示文件
* 电子表格文件
* 图表文件
* 图像文件

＃＃＃ 应用程序设置 ＃＃＃
办公应用程序的设置代表与文档配置或文档的视觉外观相关的不同设置。每个类别由一个`表示<config:config-item-set>`。此类设置类别的示例包括：
* 文档设置，例如默认打印机
* 查看设置，例如缩放级别

### 脚本###
一个文档通常包含多个脚本。 OpenDocument 文件中的每个脚本都由一个 `<office:script>`元素。这些脚本元素包含在单个 `<office:scripts>`元素。加载文档时脚本不会更新文档。
### 字体声明###

字体声明包含有关文档作者使用的字体的信息。此信息有助于在其他系统上找到这些字体。
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### 样式###
OpenDocument 格式支持以下样式。

`Common Styles` - 此类样式的 XML 表示称为样式
`自动样式` - 包含格式属性，在文档的用户界面视图中，这些属性被分配给诸如段落之类的对象。
`Mater Styles` - 一种通用样式，包含格式信息和应用样式时与文档内容一起显示的附加内容。母版样式的一个示例是母版页。

## 参考 ＃＃
* [OASIS 办公应用开放文档格式](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 格式 - 维基百科](https://en.wikipedia.org/wiki/OpenDocument)

