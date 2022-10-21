{
  "date" : "2019-10-11",
  "keywords" :["dhtml","dhtml文件","dhtml文件格式","dhtml文件类型","文件","类型","什么是dhtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - 动态 HTML 文件格式",
  "description":"了解 DHTML 文件格式和可以创建和打开 DHTML 文件的 API。",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .DHTML 文件？

扩展名为 .dhtml 的文件是一个动态 [HTML](/zh/web/html/) 文件，用于创建网页的动态内容。在 DHTML 中创建的 Web 元素是事件驱动的，不需要重新加载页面。在大多数情况下，DHTML 文件用于创建网页的动态内容，例如下拉菜单、浮动图层、翻转按钮和其他动态内容。当您将鼠标悬停在菜单项上并打开更多子菜单选项时，您几乎每天都会遇到动态 html 元素。 DHTML利用[HTML](/zh/web/html/)、[Javascript](/zh/web/js/)、HTML DOM、HTML Events和[CSS](/zh/web/css/)等网络技术实现动态元素的行为。

## DHTML 文件格式

DHTML 文件是纯文本文件，其中包含用于实现 Web 元素的动态行为的 DHTML 代码。


### DHTML DOM

DHTML 文档对象模型 (DOM) 基于 HTML DOM，它是具有元素、属性和文本的树结构，如下图所示。

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

`Document` 节点可用于调用多个函数来实现不同的功能。以下示例仅使用 DHTML 中 JavaScript 的 document.write() 方法。

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

此代码将文本“Hello World"写入浏览器中输出。

### DHTML 事件

|S.No.|事件|发生|
---|---|---|
|1|onabort|当用户中止页面或媒体文件加载时发生。|
|2|onblur|当用户离开一个 HTML 对象时发生。|
|3|onchange|当用户更改或更新对象的值时发生。|
|4|onclick|当任何用户点击 HTML 元素时发生或触发。|
|5|ondblclick|当用户同时点击一个 HTML 元素两次时发生。|
|6|onfocus|当用户关注一个 HTML 元素时发生。此事件处理程序的工作方式与 onblur 相反。|
|7|onkeydown|当用户按下键盘设备上的键时触发。此事件处理程序适用于所有键。|
|8|onkeypress|当用户按下键盘上的键时触发。不会为所有键触发此事件处理程序。|
|9|onkeyup|当用户在按下对象或元素后从键盘上松开一个键时发生。|
|10|onload|在对象完全加载时发生。|
|11|onmousedown|当用户在 HTML 元素上按下鼠标按钮时发生。|
|12|onmousemove|当用户在 HTML 对象上移动光标时发生。|
|13|onmouseover|当用户将光标移到 HTML 对象上时发生。|
|14|onmouseout|当鼠标指针移出 HTML 元素时发生或触发。|
|15|onmouseup|当鼠标按钮在 HTML 元素上释放时发生或触发。|
|16|onreset|用户使用它来重置表单。|
|17|onselect|在选择网页上的内容或文本后发生。|
|18|onsubmit|用户在提交表单后点击按钮触发。|
|19|onunload|当用户关闭网页时触发。|

## 参考

* [动态 HTML - 维基百科](https://en.wikipedia.org/wiki/Dynamic_HTML)

