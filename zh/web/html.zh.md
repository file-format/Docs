{
  "date" : "2019-10-11",
  "keywords" :["html","html文件","html文件格式","html文件类型","文件","类型","什么是html文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTML 文件格式",
  "description":"了解 HTML 文件格式和可以创建和打开 HTML 文件的 API。",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 HTML 文件？

HTML（超文本标记语言）是为在浏览器中显示而创建的网页的扩展。 HTML 被称为网络语言，随着新信息要求的要求而发展，要求将其显示为网页的一部分。最新的变体被称为 HTML 5，它为使用该语言提供了很大的灵活性。 HTML 页面要么从托管这些页面的服务器接收，要么也可以从本地系统加载。每个 HTML 页面都由 HTML 元素组成，例如表单、文本、图像、动画、链接等。这些元素由标签和其他几个元素表示，每个标签都有开始和结束。它还可以嵌入以 JavaScript 和样式表 (CSS) 等脚本语言编写的应用程序，以实现整体布局表示。

## 历史简介 ＃＃

HTML 规范自 1996 年以来一直由万维网联盟 (W3C) 维护。2000 年，它也成为国际标准 (ISO/IEC 15445:2000)。 1999 年，HTML 4.01 发布。 2004 年，Web 超文本应用技术工作组 (WHATWG) 开始研究 HTML5 版本，该版本于 2008 年与 W3C 共同交付。它于 2014 年 10 月 28 日完成并标准化。

## HTML 文件格式结构 ##

HTML 4 文档由三部分组成：

1.一行包含HTML版本信息
1. 声明性标题部分
1. 正文，包含文档的实际内容。主体可以由 BODY 元素或 FRAMESET 元素实现，以将主体包含在框架中

每个部分可以前导或后跟空格、换行符、制表符和注释。一个简单的 HTML 文档示例如下所示：

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

＃＃＃ 版本信息 ＃＃＃

第一行代码，\<!DOCTYPE html> , 称为 doctype 声明，它告诉浏览器页面是用哪个版本的 HTML 编写的。根据 HTML 的版本，有许多不同的 doctype 声明来命名文档使用的文档类型定义 (DTD)。每个 DTD 在其支持的元素上都与其他 DTD 不同，不同之处如下：

* HTML 4.01 Strict - 包括所有尚未 [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) 或未出现在框架集文档中的元素和属性
* HTML 4.01 过渡 - 包括严格 DTD 中的所有内容以及不推荐使用的元素和属性（其中大部分涉及视觉呈现
* HTML 4.01 框架集 - 包括过渡 DTD 中的所有内容以及框架

对于**HTML5**，版本信息简单如下。

```
<!DOCTYPE html>
```

### HTML 标头信息###

HTML 文档的标题可以包含许多浏览器未呈现的 HTML 元素。这些元素要么是描述页面信息的元数据，要么是用于从外部资源（如 CSS 样式表或 JavaScript 文件）获取信息的部分。页面的标题由 head 标签表示。

对于设置页面标题，**title** 元素是唯一需要的元素<head>标签。搜索引擎也使用相同的方法来识别页面的标题。

### HTML 正文信息 ###

这是文件中的主要部分，包含由浏览器呈现的文件的所有内容。 Html 正文可以包含标记，这些标记可以引用标记形式的各种构建块。它可以包含多种不同类型的信息，如文本、图像、颜色、图形等。此外，音频和视频元素也可以嵌入到 html body 中以供浏览器呈现。在存在用于视觉表示的现代样式表应用程序的情况下，BODY 的表示属性（例如背景颜色、链接颜色、文本颜色等）已被弃用。因此，使用样式表可以实现相同的效果，如下所示：

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

内联样式表易于嵌入并且为了快速应用于视觉效果，外部样式表使其更方便一次部署并在多个地方访问。

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML 元素 ###

如前所述，HTML Body 中的内容由标签表示，也称为 Html 元素。每个标签都可以具有属性形式的附加信息，这些信息写为<tag attribute1#"value1" attribute2#"value2">，尽管没有必要为每个标签都提供属性。如果未提及属性，则在每种情况下都使用默认值。以下是一些元素示例：

#### 标题####

```
<head>
  <title>The Title</title>
</head>
```

#### 标题####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### 段落####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## 参考 ＃＃

* [HTML文档的全局结构](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

