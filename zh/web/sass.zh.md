---
date: 2019-10-11
keywords: "sass,.sass,sass 文件格式,如何打开 sass 文件,语法上很棒的样式表,css 预处理器,sass"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "萨斯文件格式"
linktitle: "SASS"
description: "了解 Sass 文件格式和可以创建和打开 Sass 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## 什么是一 .sass 文件？ ##

Sass（语法上很棒的样式表）是一种预处理器脚本语言。它被编译成 [CSS](/zh/web/css/) 并以 .sass 扩展名存储。 Sass 由两种语法组成，原始的基于使用 .sass 扩展名的缩进，而新的 SCSS 具有块格式，如使用 .scss 扩展名的 CSS。

## 为什么使用 Sass ##

Sass 在维护样式方面非常有帮助，因为它提供了许多功能，例如引入变量、嵌套、混合、导入和选择器继承，使使用样式变得有趣。

## 如何使用 SASS 文件##

SASS 文件不直接包含在 [HTML](/zh/web/html/) 文档中，而是转换为包含在 HTML 文件中的 CSS 文件。您可以按照 [Sass 官方网站](https://sass-lang.com/install) 上的说明安装系统的 Sass。

Sass 可以通过转换已保存的 SASS 文件或通过观察更改并在文件保存时转换来转换为 CSS。下面给出了两者的命令。

### 转换一次###

该命令的第一个参数是源 SASS 文件，第二个参数是输出 CSS 文件。

```cmd
sass main.sass main.css
```

### 关注变化###

上面的命令可以使用额外的 *watch* 标志运行，该标志保持命令运行，并且一旦保存 Sass 文件，就会生成输出 CSS。

```cmd
sass --watch main.sass main.css
```

## Sass 语法 ##

Sass 支持变量、嵌套、混合、导入、选择器继承等。下面给出了这些特性的示例。

### 变量###

变量可用于设置可重用信息，例如按钮的原色或填充。如果将来您需要更改该信息，这将证明是有用的，您只需在一个位置更改它并且它会随处更新。

**萨斯**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

CSS 选择器可以嵌套，类似于 HTML 的层次结构。在以下示例中，跨度嵌套在 h1 块内。

**萨斯**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Mixin 用于将在多个地方使用的相似属性组合在一起。 Mixins 也支持参数。

**萨斯**

**声明一个mixin**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**使用混合**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

在一个选择器的属性需要与另一个选择器共享的情况下，扩展/继承可以证明是有用的。在下面的示例中，*.error-notice* 选择器采用 *.error-text* 选择器的所有属性并添加边框和填充属性。

**萨斯**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

如果您根据功能或您遵循的任何其他结构将样式构建到不同的文件中，则导入会很有用。您可以将所有这些文件导入到一个主要的 SASS 文件中，该文件稍后会转换为 CSS。导入时，无需在导入指令中指定文件扩展名。 Sass 直接编译所有 SASS 文件。为避免直接编译导入文件，您可以通过在其名称的开头添加下划线(_) 来使它们成为部分文件。部分导入类似于普通的 Sass 文件。

**萨斯**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

输出 CSS 将包含所有导入文件的样式。

## 参考 ＃＃

- [Sass - 维基百科](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [萨斯](https://sass-lang.com/)

