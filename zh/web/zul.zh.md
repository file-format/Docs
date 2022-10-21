{
  "date" : "2021-05-24",
  "keywords" :["zul","文件","扩展名","文件格式","文件扩展名","打开"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK 用户界面文件",
  "description":"了解 ZUL 文件格式和可以创建和打开 ZUL 文件的 API。",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## 什么是一 .zul 文件？

扩展名为 .zul 的文件是使用用户界面标记语言 (ZUML) 创建的 Web 文件，其中包含用户界面元素的定义。 Ajax 和 Java 类支持使用基于 [XML](/zh/web/xml/) 的 ZUML 来开发服务器端文件。 ZUL 文件格式由 ZK 开发，它是一个 UI 框架，使您能够在不了解 JavaScript 或 AJAX 的情况下构建 Web 和移动应用程序。

## ZUL 文件格式

ZUL 文件是基于 XML 的，由用于构建用户界面的不同元素组成。 ZK 加载器使用每个 XML 元素来创建一个组件。页面标题、描述等页面元素的整体处理由ZUML的每条XML处理指令描述。

### ZUL 示例

在下面的 ZUML 代码示例中，第一行指定页面标题，第二行创建带有标题和边框的根组件，第三行创建带有标签和事件侦听器的按钮。

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL 模式可以从 http://www.zkoss.org/2005/zul/zul.xsd 下载。
## 参考

* [ZUL - ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL 架构](http://www.zkoss.org/2005/zul/zul.xsd)

