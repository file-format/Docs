{
  "date" : "2019-12-03",
  "keywords" :["DOCX","文件","格式","文件类型","扩展名","什么是 DOCX 文件？" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"了解 DOCX 文件格式和可以创建和打开 DOCX 文件的 API。",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## 什么是一 .docx 文件？ ##

DOCX 是一种众所周知的 Microsoft Word 文档格式。从 2007 年随着 Microsoft Office 2007 的发布引入，这种新文档格式的结构从纯二进制更改为 XML 和二进制文件的组合。 Docx 文件可以用 Word 2007 和横向版本打开，但不能用支持 DOC 文件扩展名的早期版本的 MS Word 打开。

## 历史简介 ＃＃

微软开放 DOC 文件格式规范后，竞争对手很容易对格式进行逆向工程，并在自己的应用程序中提供相同的支持。此外，来自 Open Office 的开放文档格式的竞争，迫使微软采用更开放和更广泛的标准。 2000 年初，Microsoft 决定进行更改以适应 **Office Open XML** 的标准。此新标准下的文档被赋予 [.docx 扩展名](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)，“X"用于 XML。到 2007 年，这种新的文件格式成为 Office 2007 的一部分，并且在新版本的 Microsoft Office 中也得到了延续。新的文件类型增加了文件大小小、损坏更改少和格式良好的图像表示的优点。

## DOCX 文件格式规范 - 更多信息

Docx 文件由包含在 ZIP 存档中的 XML 文件的集合组成。可以通过解压缩其内容来查看新 Word 文档的内容。该集合包含一个 XML 文件列表，这些文件被分类为：

* 元数据文件 - 包含有关存档中其他可用文件的信息
* Document - 包含文档的实际内容

### 元数据文件###

Microsoft Word 使用这些文件来查找文件之间的关系并定位文档内容。提取 Word 文档存档时，它包含许多此类文件，如下所述。

#### 关系 - \_rels/.rels ####

该文件包含告诉 MS Word 在哪里查找文档内容和其他参考的信息。每个关系都由唯一的关系 ID 标识，并将引用的 XML 文件指定为目标。示例关系文件如下所示：

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### 内容类型####

一个文档可以包含多种媒体类型，如图像、主题、艺术文字等。[Content_Types].xml 包含有关文档中存在的此类媒体类型的信息。这样一个 XML 文件的内容如下所示：

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### 对资源的引用 - \_rels/document.xml.rels ####

此 XML 文件中引用了有关资源的信息，例如文档中嵌入的图像。

#### 主要文档内容####

这是指包含文档文本内容的存档的主要 XML 文件。根据 OpenOffice XML 规范，此内容由各种节点表示。该文件的内容主要由段落和表格组成，尽管它们也可以是其他节点。

### 文件格式节点###

主 document.xml 文件是用于表示文件整体内容的节点集合。每个节点都有一个开始和结束，它封装了更多的节点或内容。此类 xml 文件的简化示例如下：

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

以下是有关 DOCX 文件中包含的一些节点的信息，用于表示内容。

`<w:document> ` - 表示文件主要内容的根元素。

`<w:body> ` - 表示文档的主体，它可以包含许多其他元素节点，例如段落、表格和部分。

#### 段落####

段落是文档中的主要内容持有者。它由**表示<w:p>** 文档中的元素。一个段落进一步包含一个或多个运行**<w:r> ** 包含段落的实际文本。除了运行，段落还可能包含其他文档元素，例如超链接、注释等。示例段落结构如下所示：

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## 参考 ＃＃

* [MS - DOCX 文件格式](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

