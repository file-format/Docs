{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE 文件 - HTML5 缓存清单文件格式",
  "description" :"了解什么是 APPCACHE 文件以及可以创建和打开 APPCACHE 文件的 API。",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## 什么是 APPCACHE 文件？

APPCACHE 文件是一个文本文件，其中包含要被浏览器缓存以供离线访问 Web 应用程序的资源列表。这在没有 Internet 连接时很有用。在这种情况下，浏览器使用离线缓存资源来提供对 Web 内容的访问。 APPCACHE文件包含图片等网络资源（例如**[PNG](/zh/image/png/)**、**[WEBP](/zh/image/webp/)**等）、样式表**([ CSS])(/zh/web/css/)** 和脚本文件（如 Javascript **[JS](/zh/web/js/)** 文件）。

可以**打开 APPCACHE 文件**的应用程序包括 Web 浏览器，例如 Google Chrome、Safari 和 Firefox。

## APPCACHE 文件格式 - 更多信息

APPCACHE 文件是简单的文本文件，提供对网页的离线访问，以便在没有互联网连接的情况下运行。 APPCACHE 的存在将页面指定为离线可用。

### 如何引用 APPCACHE 文件？

在您的 HTML 页面中，一个 APPCACHE 文件被引用如下。

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE 清单文件的结构

一个简单的 APPCACHE 清单文件如下所示。

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

这是一个最简单的例子，也可能存在更复杂的结构。

## APPCACHE 清单的优点

缓存接口的使用为 Web 应用程序提供了以下优势。

1. 离线浏览 - 缓存界面让最终用户在离线时浏览您的整个网站
1. 速度 - 缓存可以直接从光盘高速访问离线内容
1. 无时无刻的可访问性 - 如果您的网站出现故障，用户仍然可以访问网页内容并获得离线体验

## 参考

* [AppCache Manifest 初学者指南](https://web.dev/appcache-beginner/)

