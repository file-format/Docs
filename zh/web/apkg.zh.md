{
  "date" : "2019-10-11",
  "keywords" :["apkg","apkg 文件","apkg 文件格式","apkg 文件类型","文件","类型","什么是 APKG 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck 文件格式",
  "description" :"了解什么是 APKG 文件以及可以创建和打开它们的 API。",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## 什么是一 .APKG 文件？

带有 .apkg 扩展名的文件是一组生成的卡片，用于 [Anki](https://ankiweb.net/about) 软件应用程序，这是一个基于卡片的学习程序。它包含要在 Anki 应用程序中加载和显示的 [HTML](/zh/web/html/) 文本，并且还可以包含用于视觉和听觉学习的图像和声音。 Anki 允许用户创建自己的 Anki 抽认卡组以及导入其他用户的抽认卡组。

## APKG 文件格式

Anki 卡片组是从用 HTML 编写的模板创建的，HTML 是一种用于创建网页的著名且通用的语言。卡片的样式是使用 CSS 完成的，CSS 是用于样式化网页的语言。样式包括对以下内容的修改：

* font-family - 卡片上使用的字体名称。
* font-size - 字体大小（以像素为单位）。
* text-align - 定义文本应该居中、左对齐还是右对齐。
* 颜色 - 定义文本的颜色，可以是简单的颜色名称，例如“蓝色"、“红色"等，也可以是 HTML 颜色代码。
* background-color - 定义卡片的背景颜色

样式信息在所有卡片之间共享，在进行更改时会影响所有卡片。以下示例将在除第一张之外的所有卡片上使用黄色背景：

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Anki 卡中调整图像大小的方法如下。

```CS
img {
  max-width: none;
  max-height: none;
}
```

## 在 Anki 卡片中嵌入 Javascript

可以使用卡片模板将 [Javascript](/zh/web/js/) 嵌入到 Anki 卡片中。但是，由于 Javascript 的高级级别，不提供对它的支持。此外，渲染设备可能会以不同的方式显示 Javascript 在卡片中的实现影响，导致需要在所有设备上测试实现。某些 Javascript 功能，例如 window.alert，使调试您编写的 Javascript 代码变得困难。

## 参考 ＃＃

* [Anki 文档](https://docs.ankiweb.net/intro.html)

