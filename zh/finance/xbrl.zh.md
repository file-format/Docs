{
  "date" : "2019-10-11",
  "keywords" :["xbrl","xbrl 文件","xbrl 文件格式","fxbrl 文件类型","文件","类型","什么是 xbrl 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - 商业和财务报告文件格式",
  "description":"了解 XBRL 文件格式和可以创建和打开 XBRL 文件的 API。",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## 什么是一 .xbrl 文件？

扩展名为 .xbrl（可扩展业务报告语言）的文件是用于交换业务信息的免费全球框架。它现在被广泛用作标准格式之一，用更有用和更准确的数字记录取代了旧的纸质报告。使用 XBRL 文件交换的数据包括分类账、财务细节和资产负债表。它支持数据标签，允许对各种业务信息从准备到分析阶段进行数据处理。 XBRL 文件可以使用 Rivet Software Dragon View XBRL Viewer 等软件和 [Aspose.Finance](https://products.aspose.com/finance/) 等 API 打开。

## XBRL 文件格式

XBRL 是一种在全球范围内广泛使用的数字业务报告的开放国际标准。它是一种基于 [XML](/zh/web/xml/) 的语言，它使用称为标签的 XBRL 元素来描述每一项业务数据，以形成用于报表排序和分析的数据。 XBRL 文件格式规范由 XBRL International, Inc 开发和发布，目前 [XBRL 版本 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html)可供用户使用。

### XBRL 文档结构

关于 [XBRL 2.1 标签]的完整信息(https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html）可以被程序员引用来编写应用程序来处理这种文件格式。 XBRL 由一个 XBRL 实例和一组分类法组成。

**`XBRL 实例`** - XBRL 实例以<xbrl>根元素。一个大型 XML 文档可以包含多个嵌入其中的 XBRL 实例。

**`XBRL 分类法`** - [XBRL 分类法](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) 被定义为一个 XML 模式结构和一组直接引用的外部链接元素。显示链接库引用的可扩展分类模式如下。

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## 参考 ＃＃

* [XBRL - 维基百科提供](https://en.wikipedia.org/wiki/XBRL)
* [可扩展业务报告语言 (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-勘误表-2013-02-20.html)

