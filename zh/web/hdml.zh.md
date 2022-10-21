{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"手持设备标记语言文件",
  "description":"了解 HDML 文件格式和可以创建和打开 HDML 文件的 API。",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## 什么是 HDML 文件？

具有 .hdml（手持设备标记语言）扩展名的文件是一种标记语言，用于为便携式电子设备（如手持计算机、智能手机和信息显示设备）创建网页。 HDML 据说是 [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) 语言的扩展。 HDML 类似于 HTML，但适用于具有小型显示器的无线和手持设备，例如 PDA、移动电话等。它被 WML 取代，WML 对其产生了重要影响。

## HDML 文件格式 - 更多信息

HDML 是一种用于手持设备的标记语言，它基于类似于 HTML 的标记标签。 HDML 已提交给 W3C 进行标准化，但它从未成为标准。但是，其文件格式规范可在 [W3 网站](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) 上获取以供参考。 [HDML 语言语法](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) 可供开发者参考，可用于示例应用程序开发。

## HDML 元素

以下是为 HDML 提供运行时环境的一些元素，被称为用户代理。

|元素|描述|
---|---|
|卡片|这是 HDML 的基本构建块，显示并允许用户与信息卡片进行交互。 |
|卡组|HDML 卡组合成卡组。 HDML 卡片组类似于 HTML 页面，因为它由 URL [RFC1738] 标识，并且是从服务器请求并由用户代理缓存的内容单元。
|操作|操作可以是 PREV、SOFT1-SOFT8 和 HELP 类型。这些是抽象的，并以用户代理特定的方式在用户界面中得到支持。|
|活动|活动就像一组执行一个逻辑功能的相关卡片。这些可能跨越一个或多个甲板。 HDML 导航和状态模型是围绕活动构建的。|
|基于历史的导航|用户代理维护向用户显示的卡片的历史。每张被访问的卡片都会添加到卡片历史记录中。用户代理允许用户轻松导航回历史记录中的上一张卡片。

## 参考

* [HDML - 维基百科](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML 规范 - W3 学校](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

