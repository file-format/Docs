{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DXL 文件格式以及可以创建和打开 DTSX 文件的 API。",
  "title" :"DXL 文件格式 - Domino XML 语言文件格式",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## 什么是一 .dxl 文件？

DXL 文件是为企业级业务协作软件 Lotus Domino 创建的基于 XML 的数据存储文件。它包含与 Lotus Domino 数据库相关的数据，例如模式、设计元素、视图、表单、文档和数据库数据本身。 [XML](/zh/web/xml/) 是一种通用文件格式，可以由任何编程语言编写的软件应用程序读取。它也是人类可读的，可以使用任何文本编辑器打开。这就是 DXL 文件提供以可互换文件格式导出数据的功能的原因。

## DXL 文件格式

DXL 文件以 XML 文件格式保存，可由任何编程语言编写的应用程序轻松读取。这些文件将数据和设置存储在 XML 标记中，这些标记对数据进行分类并按正确的顺序排列数据

### DXL 输出示例

以下是 Notes 文档的输出文本摘录输出。

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## 参考

* [DXL 格式 - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

