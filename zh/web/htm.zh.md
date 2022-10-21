{
  "date" : "2019-10-11",
  "keywords" :["htm","htm 文件","htm 文件格式","htm 文件类型","文件","类型","什么是 htm 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTM 文件格式",
  "description" :"您的文件格式指南,了解什么是 HTM 文件以及可以创建和打开它们的 API。",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .htm 文件？

带有 **.htm** 扩展名的文件代表超文本标记语言，用于创建网页以在 Google Chrome、Internet Explorer、Firefox 等网络浏览器中显示。它定义了用于创建要在万维网 (WWW) 上发布以供其他人访问的静态页面的标记。这些标记告诉浏览器如何显示网页的内容。此类页面可以包含纯文本、图像、指向其他页面的超链接、视频和其他媒体信息。当一个网页发布后，您可以通过查看其页面源代码来了解其背后的标记代码。现代浏览器允许检查网页的每个部分，其中详细说明了 HTM 源中的每个细分或标记元素。

## HTM 简史

HTML 规范自 1996 年以来一直由万维网联盟 (W3C) 维护。2000 年，它也成为国际标准 (ISO/IEC 15445:2000)。 1999 年，HTML 4.01 发布。 2004 年，Web 超文本应用技术工作组 (WHATWG) 开始研究 HTML5 版本，该版本于 2008 年与 W3C 共同交付。它于 2014 年 10 月 28 日完成并标准化。

## HTML 文件格式

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

＃＃＃ 版本信息

第一行代码，<!DOCTYPE html> , 称为 doctype 声明，它告诉浏览器页面是用哪个版本的 HTML 编写的。根据 HTML 的版本，有许多不同的 doctype 声明来命名文档使用的文档类型定义 (DTD)。每个 DTD 在其支持的元素上都与其他 DTD 不同，不同之处如下：

* HTML 4.01 Strict - 包括所有尚未 [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) 或未出现在框架集文档中的元素和属性
* HTML 4.01 过渡 - 包括严格 DTD 中的所有内容以及不推荐使用的元素和属性（其中大部分涉及视觉呈现
* HTML 4.01 框架集 - 包括过渡 DTD 中的所有内容以及框架

对于**HTML5**，版本信息简单如下。

```
<!DOCTYPE html>
```

### 标头信息

HTML 文档的标题可以包含许多浏览器未呈现的 HTML 元素。这些元素要么是描述页面信息的元数据，要么是用于从外部资源（如 CSS 样式表或 JavaScript 文件）获取信息的部分。页面的页眉由 \ 表示<head>标记并以 \ 结尾</head>标签。

<html>对于设置页面标题，\<title> element 是 \<head> 标签中唯一需要的元素。搜索引擎也使用相同的方法来识别页面的标题。 </html>

### 身体信息

这是文件中的主要部分，包含由浏览器呈现的文件的所有内容。 Html 正文可以包含标记，这些标记可以引用标记形式的各种构建块。它可以包含多种不同类型的信息，如文本、图像、颜色、图形等。此外，还可以将音频和视频元素嵌入到 html 正文中以供浏览器呈现。在存在用于视觉表示的现代样式表应用程序的情况下，BODY 的表示属性（例如背景颜色、链接颜色、文本颜色等）已被弃用。因此，使用样式表可以实现相同的效果，如下所示：

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

### HTML 元素

如前所述，HTML Body 中的内容由标签表示，也称为 Html 元素。每个标签都可以具有属性形式的附加信息，这些信息写为
```
<tag attribute1#"value1" attribute2#"value2">
```
尽管没有必要对每个标签都有属性。如果未提及属性，则在每种情况下都使用默认值。以下是一些元素示例：

#### 标题

```
<head>
  <title>The Title</title>
</head>
```

#### 标题

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### 段落

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## 参考

* [HTML文档的全局结构](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

