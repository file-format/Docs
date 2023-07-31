{
  "date" : "2019-12-13",
  "keywords" :["pptx 文件","pptx 文件格式","什么是 pptx 文件","文件","pptx 示例","pptx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 PPTX 文件格式和可以创建和打开 PPTX 文件的 API。",
  "title" :"PPTX - PowerPoint 演示文件格式",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .PPTX 文件？

带有 PPTX 扩展名的文件是使用流行的 Microsoft PowerPoint 应用程序创建的演示文件。与以前版本的二进制演示文件格式 PPT 不同，PPTX 格式基于 Microsoft PowerPoint 开放 XML 演示文件格式。演示文件是幻灯片的集合，其中每张幻灯片可以包含文本,图像、格式、动画和其他媒体。这些幻灯片以带有自定义演示设置的幻灯片的形式呈现给观众。

## 历史简介

PPTX 文件格式于 2007 年推出，使用 Microsoft 早在 2000 年采用的 Open XML 标准。在 PPTX 之前，使用的常用文件格式是纯二进制文件格式的 PPT。新的文件类型增加了文件大小小、损坏变化少和格式良好的图像表示的优点。 2000 年初，Microsoft 决定进行更改以适应 **Office Open XML** 的标准。到 2007 年，这种新的文件格式成为 Office 2007 的一部分，并且在新版本的 Microsoft Office 中也得到了延续。

## PPTX 文件格式规范

使用 office Open XML 文件格式生成的文件是 XML 文件以及提供所有组成文件之间链接的其他文件的集合。这个集合实际上是一个压缩存档，可以提取它来查看它的内容。为此，只需使用 zip 重命名 PPTX 文件扩展名并将其解压缩以观察其内容（请参阅 [PPTX 文件格式规范](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) 由 Microsoft）。

以下部分对其中的每一个进行了说明。

### [Content_Types].xml

这是解压缩 zip 时在基本级别找到的唯一文件。它列出了包中部件的内容类型。此 XML 文件中引用了对包中包含的 XML 文件的所有引用。以下是幻灯片部分的内容类型：

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

如果需要将新部件添加到包中，可以通过添加新部件并更新 .rels 文件中的任何关系来完成。必须记住，对于此类更改，还必须更新 Content_Types.xml。

### \_rels（文件夹）###

包外的其他部分和资源之间的关系由关系部分维护。关系文件夹包含一个存储包级关系的 XML 文件。指向 PPTX 文件关键部分的链接作为 URI 包含在此文件中。这些 URI 标识每个关键部分与包的关系类型。这包括与位于 ppt/presentation.xml 中的主要办公文档的关系以及 docProps 中的其他部分作为核心和扩展属性。

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

作为一个或多个关系源的文档的每个部分都将具有自己的关系部分，其中每个此类关系部分都可以在该部分的 \_rels 子文件夹中找到，并通过将“.rels"附加到该部分的名称来命名部分。主要内容部分 (presentation.xml) 有自己的关系部分 (presentation.xml.rels)。它包含与内容其他部分的关系，例如 slideMaster1.xml、notesMaster1.xml、handoutMaster1.xml、slide1.xml、presProps.xml、tableStyles.xml、theme1.xml，以及外部链接的 URI。

#### 显式关系####

对于显式关系，使用资源的 Id 属性引用资源<Relationship>元素。也就是说，源中的 Id 直接映射到关系项的 Id，并具有对目标的显式引用。

例如，幻灯片可能包含如下超链接：

```
<a:hlinkClick r:id#"rId2">
```

r:id#"rId2" 引用幻灯片的关系部分 (slide1.xml.rels) 中的以下关系。

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### 隐式关系####

对于隐式关系，没有对 ` 的直接引用<Relationship>标识`。相反，引用被理解。

### ppt文件夹###

这是包含有关演示文稿内容的所有详细信息的主文件夹。默认情况下，它具有以下文件夹：

* \_rels
* 主题
*幻灯片
*幻灯片布局
*幻灯片大师

和以下 xml 文件：

* 演示文稿.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## 参考 ＃＃

* [[MS-PPTX] - PPTX 文件格式](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

