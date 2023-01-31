{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM 文件 - 手持设备标记语言文件",
  "description":"了解可以创建和打开 HDM 文件的 HDM 文件格式和 API。",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## 什么是一 .hdm 文件？

HDM 文件是以手持设备标记语言 (HDML) 创建的标记语言网页文件。它包含类似于[HTML](/zh/web/html/)语言的标记标签，但专为智能手机和PDA等手持电子设备而设计。 [HDML 文件格式规范](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) 已提交给 W3C 进行标准化，但未能成为标准。 HDM 基于 W3 网站上提供的 [HDML](/zh/web/hdml/) 文件格式规范。

## HDM 文件格式 - 更多信息

HDM 文件由标记标记组成，这些标记标记呈现给手持设备上视觉设计的网站。 HDM 文件使用 HDTP（手持设备传输协议）协议而不是用于 HTML 页面的 HTTP 协议复制到设备。

## HDML 文件元素

以下是一些为 HDML 提供运行时环境的元素，称为用户代理。

|元素|描述|
---|---|
|卡片|这是 HDML 的基本构建块，显示信息卡片并允许用户与信息卡片交互。 |
|Decks|HDML 卡被分组到 decks 中。 HDML 卡片组类似于 HTML 页面，因为它由 URL [RFC1738] 标识，并且是从服务器请求并由用户代理缓存的内容单元。|
|Actions|Actions 可以是 PREV、SOFT1-SOFT8 和 HELP 类型。这些是抽象的，并以用户代理特定的方式在用户界面中得到支持。|
|活动|活动就像一组执行一个逻辑功能的相关卡片。这些可能跨越一个或多个甲板。 HDML 导航和状态模型是围绕活动构建的。|
|基于历史的导航|用户代理维护显示给用户的卡片的历史。每张被访问的卡片都会添加到卡片历史记录中。用户代理允许用户轻松导航回历史记录中的上一张卡片。|

## 参考

* [HDML - 维基百科](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML 规范 - W3 学校](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

