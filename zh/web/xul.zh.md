{
  "date" : "2021-05-24",
  "keywords" :["xul","文件","扩展名","文件格式","文件扩展名","XML 用户界面语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML 用户界面语言文件",
  "description":"了解 XUL 文件格式和可以创建和打开 XUL 文件的 API。",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## 什么是一 .xul 文件？

具有 .xul 扩展名的文件（[XUL](https://wiki.mozilla.org/XUL:Home_Page) 代表 XML 用户界面语言）是一个基于 [XML](/zh/web/xml/) 的标记语言文件，用于创建用户界面。它由 Mozilla 开发，供开发人员创建类似于用于创建网页的其他标记语言的图形用户界面元素。 XUL 已被 Mozilla 在其使用 Mozilla 代码库的 Firefox 浏览器中广泛使用。 XUL 渲染是使用
[壁虎引擎](https://en.wikipedia.org/wiki/Gecko_(software))。 Pale Moon、Basilisk 和 Waterfox 等 Firefox 分支保留了对 XUL 附加组件的支持。 XUL 文件使用 MIME 类型标识：application/vnd.mozilla.xul+xml。

## XUL 文件格式

XUL 文件以基于 XML 文件格式的纯文本编写，并使用 Gecko 引擎呈现。 XUL 结构的三个主要部分是：

* `Content` - 这包括窗口的声明和其中包含的用户界面元素。
* `皮肤` - 它包括任何样式表、图像和其他主题相关文件。窗口的外观在样式表中描述。
* `Locale` - 窗口内显示的文本单独存储，用户可以使用多组语言文件。

### XUL 示例

下面的示例创建三个在垂直方向上相互堆叠的按钮。

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## 参考

* [XUL - 维基百科](https://en.wikipedia.org/wiki/XUL)
* [XUL 存档文档 - Mozilla 提供](https://wiki.mozilla.org/XUL:Home_Page)

