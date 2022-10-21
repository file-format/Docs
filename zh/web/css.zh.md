---
date: 2019-10-11
keywords: "css,.css,css文件格式,如何打开css文件,级联样式表"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "CSS 文件格式"
linktitle: "CSS"
description: "了解 CSS 文件格式和可以创建和打开 CSS 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## 什么是 CSS 文件？ ##

CSS（层叠样式表）是描述 HTML 元素如何在屏幕、纸张等上显示的文件。使用 HTML，您可以嵌入样式或可以在外部样式表中定义样式。对于嵌入样式，\ <style>\</style>使用标签。外部样式表存储在扩展名为 .css 的文件中。使用外部 CSS，您可以将其包含在多个 HTML 页面中以更新这些页面的样式。即使是一个 CSS 文件也可以用来设计一个完整的网站。

## 历史简介 ＃＃

CSS1 于 1996 年发布，Bert Bos 是合著者。 CSS 工作组开始着手解决 CSS1 中未解决的问题。这导致在 1997 年 11 月创建了 CSS2，并于 1998 年 5 月 12 日作为 W3C 推荐发布。该版本增加了对特定媒体设备的支持，如打印机、可下载字体、表格和元素定位。 1999 年 6 月，CSS3 成为 W3C 的推荐标准。这将文档划分为模块，每个模块都有 CSS2 中定义的扩展功能。

## 如何使用 CSS 文件##

要使用 CSS 文件，请将其包含在 HTML 文档的 head 部分中。您使用链接标签来包含文件，如下所示。

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

链接标签的 *href* 属性包含 CSS 文件的路径。通过这样做，包含在包含的 CSS 文件中的适用样式将应用于 HTML 文档。

## CSS 语法 ##

CSS 规则由两个组件组成，一个选择器和一个声明。选择器指向 HTML 文档中的元素。它可以是元素标签、类名、id 名称、显示层次结构的多个标签等。声明包含由属性和值组成的样式定义。属性标识要更改的元素的属性，值定义其新值。每个 CSS 规则可以有多个声明。以下是 CSS 规则的示例。

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

在上面的示例中，我们将 **h1** 作为选择器，用于选择 HTML 文档中的所有 h1 标记。该规则有两个声明，一个用于字体粗细，另一个用于颜色。 *font-weight* 和 *color* 是属性，*700* 和 *forestgreen* 分别是它们的值。

## CSS 使用示例 ##

下面显示了示例 HTML 文档和用于设置样式的样式表。还添加了比较图像以比较样式和纯 HTML 文档

### HTML 文档###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS 样式表###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### 输出比较###

图像左侧显示未应用样式的 HTML 文档，右侧显示应用了样式的 HTML 文档。

{{< figure src="../CssExample.jpg" alt="示例图片" >}}

## 参考 ＃＃

- [CSS - 维基百科](https://en.wikipedia.org/wiki/CSS)

