{
  "date" : "2021-12-09",
  "keywords" :["aro",".aro 文件","aro 文件格式","文件类型","文件","类型","什么是 .aro 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO 文件格式 - SteelArrow Web 应用程序文件",
  "description" :"了解什么是 ARO 文件以及可以创建和打开 ARO 文件的 API。",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## 什么是一 .aro 文件？

ARO 文件是使用 SteelArrow Web 应用程序生成的服务器端网页文件。它包含 [HTML](/zh/web/html/) 和 SteelArrow 标签和脚本。这些在服务器上执行以生成完整的响应页面，然后将它们发送到用户的浏览器。 ARO 文件包含几乎 95% 的 HTML 内容，而其余的则由 SteelArrow 代码组成。要使 ARO 文件为您工作，应在 Web 服务器计算机上安装并运行 SteelArrow Web 应用程序服务器。

## ARO 文件格式

ARO 文件是用嵌入了 JavaScript 代码和 Java 小程序的 HTML 标记语言文件编写的。 [SteelArrow 标签](http://www.steelarrow.com/docs/basics1.aro) 是网页开发的基本构建块。虽然这些不会改变页面的显示，但它们用于用数据填充页面。此外，它们还可用于通过条件语句控制输出。

### ARO 标记示例

这<SAOUTPUT>ARO 标记允许开发人员在脚本中的任何位置输出数据值。例如，它可用于获取 PARAM 表的输出<SAOUTPUT VALUE=PARAM[]>可以在 HTML 中显示<BODY>标签。

## 参考

* [钢箭标签](http://www.steelarrow.com/docs/basics.aro)

