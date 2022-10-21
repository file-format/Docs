{
  "date" : "2021-07-08",
  "keywords" :["HAR","文件","扩展名","文件格式","文件扩展名","JSON","存档文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP 存档文件格式",
  "description" :"您的文件格式指南,了解什么是 HAR 文件以及可以创建和打开 HAR 文件的 API。",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## 什么是一 .har 文件？

带有 .har ([HTTP](/zh/web/http/) Archive) 文件的文件是一个 HTTP 存档文件，它以 [JSON] 格式存储在许多浏览器（例如 Chrome、Safari、IE、Firefox 等）上传输的会话数据(/zh/web/json/) 文件格式。服务器和客户端（在本例中为用户的浏览器）之间通过 Internet 传输的数据包含存储在 HAR 文件中的 HTTP 请求和响应标头。它还包含有关浏览器中加载的网页的性能数据的详细信息。 HAR 文件可以在任何文本编辑器中打开，例如 Microsoft Windows 操作系统上的记事本和 Apple MacOS 上的 TextEdit。

## HAR 文件格式 - 更多信息

HAR 文件使用流行的 JSON 格式将会话信息存储在纯文本文件中。 HAR 文件格式规范由万维网联盟 (W3C) 的 Web 性能组制定，但无法发布。但是，它成功地定义了 HTTP 事务的归档格式。

除了监控请求和响应信息的传输之外，开发人员还使用 HAR 文件来记录 Web 浏览器在页面加载速度、内容加载持续时间、内容加载、执行查询以从浏览器获取响应等方面的性能.

## 为什么要使用 HAR 文件？

通过评估较长的加载时间、页面呈现时间和响应时间，HAR 文件有助于提高网站的性能。可以分析 HAR 文件以发现任何此类问题并解决网站的任何问题以提高性能。

## 如何生成 HAR 文件？

那么，如何生成 HAR 文件呢？嗯，这取决于您用来生成 HAR 文件的浏览器类型。在本指南中，我们列出了 Google Chrome 浏览器的步骤。使用 Safari、Firefox 等生成 HAR 文件的方法可以很容易地在互联网上搜索并遵循。

### 使用 Google Chrome 生成 HAR 文件的步骤

可以在面临问题的网页上执行以下步骤。

1.在谷歌浏览器中打开出现问题的网页。
1. 打开开发者工具（检查元素）。
1. 转到面板左侧开始文件录制。这部分有一个小的圆形红色按钮。
1. 单击“清除图标"以删除浏览器中保存的所有日志记录。
1.如上图保存你想要的内容，右键点击“Save as HAR File"

## 参考

* [HAR 文件格式 - 维基百科](https://en.wikipedia.org/wiki/HAR_(file_format))

