---
date: 2019-10-11
keywords: "js, .js, js文件格式, 如何打开js文件, javascript文件"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JS 文件格式"
linktitle: "JS"
description: "了解 JS 文件格式和可以创建和打开 JS 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## 什么是一 .js 文件？ ##

JS (JavaScript) 是包含用于在网页上执行的 JavaScript 代码的文件。 JavaScript 文件以 .js 扩展名存储。在 [HTML](/zh/web/html/) 文档中，您可以使用 \ 嵌入 JavaScript 代码<script>\</script>标签或包含一个 JS 文件。与 [CSS](/zh/web/css/) 文件类似，JS 文件可以包含在多个 HTML 文档中，以实现代码的可重用性。 JavaScript 可用于操作 HTML DOM。

## 历史简介 ＃＃

JavaScript 于 1995 年 9 月首次作为 Navigator 浏览器的一部分发布，Netscape 将其命名为 LiveScript。三个月后它更名为 JavaScript。 1996 年，微软对 Navigator 的解释器进行了逆向工程以创建 JScript。 JScript 与 Internet Explorer 一起发布，与 JavaScript 非常不同。

Netscape 将 JavaScript 提交给 ECMA 国际，导致第一个 ECMAScript 规范于 1997 年正式发布。ECMAScript 2 于 1998 年发布，ECMAScript 3 于 1999 年发布，ECMAScript 4 的工作始于 2000 年，但从未实现。

Jesse James Garrett 在 2005 年发布了一份白皮书，他在其中创造了 *Ajax* 一词。这使用 JavaScript 作为主干来创建在后台加载数据并避免整个页面重新加载的 Web 应用程序。这导致了 JQuery、Prototype、Dojo 等库的创建。

Google 于 2008 年发布了带有 V8 JavaScript 引擎的 Chrome 浏览器。2009 年初，双方达成了一项协议，将所有相关工作结合起来，推动 JavaScript 向前发展。这导致了 2009 年 12 月 ECMAScript 5 标准的发布。

## 如何使用JS文件##

要使用 JS 文件，请将其包含在 HTML 文档中。您使用链接标签来包含文件，如下所示。

```html
<script src="site.js"></script>
```

*script* 标签的 *src* 属性包含 JS 文件的路径。通过这样做，JS 功能被添加到 HTML 文档中。

## JS 语法 ##

JavaScript 文件可以包含变量、运算符、函数、条件、循环、数组、对象等。下面是 JavaScript 语法的简要概述。

- 每个命令都以分号 (;) 结尾。
- 使用 *var* 关键字声明变量。
- 支持算术运算符 ( + - * / ) 来计算值。
- 单行注释用 // 添加，多行注释用 /* 和 */ 包围。
- 所有标识符都区分大小写，即*modelNo* 和*modelno* 是两个不同的变量。
- 函数是使用 *function* 关键字定义的。
- 可以使用方括号 [] 定义数组。
- JS 支持比较运算符，如 ==、!=、>=、!== 等。
- 可以使用 *class* 关键字定义类。

## JS 使用示例 ##

下面显示了一个简单的使用示例 JavaScript 文件。

### HTML 文档###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS代码###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## 参考 ＃＃

- [JS - 维基百科](https://en.wikipedia.org/wiki/JavaScript)

