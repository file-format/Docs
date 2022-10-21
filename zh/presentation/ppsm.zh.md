{
  "date" : "2019-10-11",
  "keywords" :["ppsm 文件","ppsm 文件格式","什么是 ppsm 文件","文件","ppsm 示例","ppsm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - 启用宏的 PowerPoint 演示文件",
  "description":"了解 PPSM 文件格式和可以创建和打开 PPSM 文件的 API。",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ppsm 文件？

带有 PPSM 扩展名的文件表示使用 Microsoft PowerPoint 2007 或更高版本创建的启用宏的幻灯片文件格式。另一种类似的文件格式是 [PPTM](/zh/presentation/pptm/)，它与 Microsoft PowerPoint 以可编辑格式打开而不是作为幻灯片放映运行不同。当以幻灯片形式运行时，PPSM 文件会显示演示幻灯片，幻灯片中的内容保持不变，默认情况下处于只读模式。通过在 PowerPoint 中打开 PPSM 文件，仍然可以在 Microsoft PowerPoint 中对其进行编辑。

## 文件格式 ＃＃

PPSM 文件格式是在 PowerPoint 2007 中引入的，它基于 OpenXML 文件格式，它使用 XML 和 [ZIP](/zh/compression/zip/) 的组合来存储其内容。使用 office Open XML 文件格式生成的文件是 XML 文件以及提供所有组成文件之间链接的其他文件的集合。这个集合实际上是一个压缩存档，可以提取它来查看它的内容。为此，只需将 PPSM 文件扩展名重命名为 zip 并将其解压缩以观察其内容。

以下部分对其中的每一个进行了说明。

### [Content_Types].xml ###

这是解压缩 zip 时在基本级别找到的唯一文件。它列出了包中部件的内容类型。此 XML 文件中引用了对包中包含的 XML 文件的所有引用。以下是幻灯片部分的内容类型：
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
如果需要将新部件添加到包中，可以通过添加新部件并更新 .rels 文件中的任何关系来完成。必须记住，对于此类更改，还必须更新 Content_Types.xml。

### \_rels（文件夹）###

包外的其他部分和资源之间的关系由关系部分维护。关系文件夹包含一个存储包级关系的 XML 文件。演示文件关键部分的链接作为 URI 包含在此文件中。这些 URI 标识每个关键部分与包的关系类型。这包括与位于 ppt/presentation.xml 中的主要办公文档的关系以及 docProps 中的其他部分作为核心和扩展属性。
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
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

* [OpenXML 演示文件格式](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [打开 Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

