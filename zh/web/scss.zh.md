---
date: 2019-10-11
keywords: "scss,.scss,scss 文件格式,如何打开 scss 文件,语法上很棒的样式表,css 预处理器,sass"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "SCSS 文件格式 - Sass 级联样式表"
linktitle: "SCSS"
description: "了解 SCSS 文件格式和可创建和打开 SCSS 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## 什么是一 .scss 文件？ ##

SCSS 是 Sass（Syntactically Awesome Stylesheet）的第二种语法，它使用括号而不是缩进。 SCSS 的设计方式是有效的 CSS3 文件也是有效的 SCSS 文件。 SCSS 文件以 .scss 扩展名存储。

## 为什么使用 SCSS ##

随着网站设计变得越来越复杂，导致大型 [CSS](/zh/web/css/) 文件。这样的文件更难维护。这就是 SCSS 的用武之地。SCSS 在 CSS 开发中引入了变量、嵌套、混合、导入和选择器继承。这些新增功能使设计工作变得更加有趣。

## 如何使用 SCSS 文件##

SCSS 文件不像 CSS 那样直接包含在 [HTML](/zh/web/html/) 文档中。相反，SCSS 文件被转换为包含在 HTML 文件中的 CSS 文件。要在您的系统上安装 SCSS，请按照 [Sass 官方网站](https://sass-lang.com/install) 上的说明进行操作。
要将 SCSS 转换为 CSS，您可以转换已保存的 SCSS 文件或观察更改并在文件保存时进行转换。下面给出了两者的命令。

### 转换一次###

第一个参数是源 SCSS 文件，第二个参数是输出 CSS 文件。

```cmd
sass main.scss main.css
```

### 关注变化###

该命令有一个额外的 *watch** 标志，可以保持命令运行，并且一旦保存 SCSS 文件，就会生成输出 CSS。

```cmd
sass --watch main.scss main.css
```

## SCSS 语法 ##

SCSS 支持变量、嵌套、混合、导入、选择器继承等。下面给出了这些特性的示例。

### 变量###

通过使用变量，您可以为保存按钮设置可重复使用的信息，例如原色或背景色。如果您需要更改该信息，这很有用，您只需在一个位置进行更改，它就会在使用时更新。

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**生成的 CSS **

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### 嵌套###

您可以嵌套类似于 HTML 层次结构的 CSS 选择器。在下面给出的示例中，跨度嵌套在 h1 块内。

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**生成的 CSS **

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### 混合###

Mixins 可用于将在多个地方一起使用的相似属性组合在一起。您还可以将参数传递给 mixins。

**SCSS**

**声明一个mixin**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**使用混合**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**生成的 CSS **

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

＃＃＃ 延长 ＃＃＃

扩展/继承在一个选择器的属性需要与另一个选择器共享的情况下很有用。在下面的示例中，*.error-notice* 选择器采用 *.error-text* 选择器的所有属性并添加边框和填充属性。

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**生成的 CSS **

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

＃＃＃ 进口 ＃＃＃

导入可用于关注点分离。您可以通过以下方式划分样式：页眉样式在一个单独的文件中，页脚样式在一个单独的文件中，样式中使用的所有颜色变量都可以在一个单独的文件中，等等。使用这种技术，风格保持井井有条。您只需导入主 SCSS 文件中的文件，如下例所示。您无需在导入指令中指定文件扩展名。 Sass 直接编译所有 SCSS 文件。为避免直接编译导入文件，您可以通过在其名称前添加下划线(_) 将其设为部分文件。您可以导入类似于普通 SCSS 文件的不带下划线的部分。

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

输出 CSS 将包含所有导入文件的样式。

## 参考 ＃＃

- [SCSS - 维基百科](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [萨斯](https://sass-lang.com/)

