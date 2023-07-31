{
  "date" : "2019-10-11",
  "keywords" :["ixbrl","ixbrl 文件","ixbrl 文件格式","ixbrl 文件类型","文件","类型","什么是 ixbrl 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - 商业和财务报告文件格式",
  "description":"了解 IXBRL 文件格式和可以创建和打开 IXBRL 文件的 API。",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## 什么是一 .iXBRL 文件？

iXBRL (ilnine XBRL) 文件格式允许将 [XBRL](/zh/finance/xbrl/) 数据嵌入到 HTML 文件中，使其既机器可读又人类可读。它实际上是一个使用 XBRL 标签的 [xHTML](/zh/web/xhtml/) 文件，由 XBRL International 开发，以满足英国 HMRC 的要求。使用 iXBRL，可以在保持原始文档布局不变的情况下创建财务报表。 iXBRL 文件可以在任何文本编辑器中打开，例如 Windows 操作系统上的记事本和 MacOS 上的 TextEdit。

## iXBRL 文件格式

在 iXBRL 内部，XBRL 的内容以使用 XML 标记的 xHTML 文件格式包装。与 XBRL 一样，<xbrl>是 iXBRL 文件的根元素。 XHTML 格式将其内容表示为不同文档类型和模块的集合。 XHTML 中的所有文件均基于 XML 文件格式并符合 XML 文档标准。 XHTML 是依赖 [HTML](/zh/web/html/) 文档对象模型 (DOM) 或 [XML](/zh/web/xml/) 文档对象模型的操作使用的基本用法格式。对于外部世界，iXBRL 遵循 [xHTML](/zh/web/xhtml/) 文件格式规范。

### iXBRL 与 XBRL

XBRL 可以根据以下因素与 iXBRL 进行比较：

* 复杂性
* 格式化选项
* 文件类型/扩展名
* 渲染选项
* 备案流程

下表说明了这些差异。

|参数|XBRL|iXBRL|
---|---|---|
|复杂性|比 iXBRL 更复杂|由于现有的 XHTML 组织方案，复杂性更小|
|格式化选项|有限的灵活性|内容格式化的高度灵活性|
|文件类型/扩展名|以 .xml 扩展名正式保存|通常保存为 .html 或 .xhtml 扩展名|
|渲染选项|查看这些所需的 XBRL 查看器|可以在浏览器中查看的人类可读内容|
|备案流程| XBRL（机器可读）和 HTML（人类可读）实例文档分别归档。|人类可读和机器可读格式都可在单个实例文档中使用|

## 参考

* [XBRL - 维基百科提供](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

