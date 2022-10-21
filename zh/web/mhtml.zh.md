{
  "date" : "2019-10-11",
  "keywords" :["mhtml","mhtml文件","mhtml文件格式","mhtml文件类型","文件","类型","什么是mhtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML 文件",
  "description":"了解 MHTML 文件格式和可以创建和打开 MHTML 文件的 API。",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 MHTML 文件？

具有 MHTML 扩展名的文件代表一种网页存档格式，可以由许多不同的应用程序创建。该格式被称为存档格式，因为它将 web **[HTML](/zh/web/html/)** 代码和相关资源保存在单个文件中。这些资源包括链接到网页的任何内容，例如图像、小程序、动画、音频文件等。 MHTML 文件可以在各种应用程序中打开，例如 Internet Explorer 和 Microsoft Word。 Microsoft Windows 使用 MHTML 文件格式记录在 Windows 上使用任何引发问题的应用程序期间观察到的问题场景。 MHTML 文件格式对页面内容进行编码，类似于 message/rfc822 中定义的规范，这是纯文本电子邮件相关规范。格式的实际规范由 [RFC 2557](https://tools.ietf.org/html/rfc2557) 详细说明。

## MHTML 文件格式

MHTML 也被称为聚合 HTML 文档的 MIME 封装，因为它能够将 HTML 网页及其资源编码到单个 Web 存档中。根据 RFC 2557 规范，聚合文档是 MIME 编码的消息，其中包含根资源（对象）以及通过 URI 链接到它的其他资源。这样的其他资源可以是内嵌图片、样式表、小程序等的表示。此外，这些可以是其他多媒体文档的根。 MHTML 文件格式的完整文档规范在 [RFC 2557](https://tools.ietf.org/html/rfc2557) 中有详细说明，并且应参考任何类型的应用程序开发以读取/写入此文件格式。该标准规定要引用的正文部分可以由 Content-ID 或 Content-Location 标识。

### MIME 内容标题

MIME 内容标头 Content-Location 被定义为解析对其他正文部分中资源的 URI 引用。此标题可以出现在任何消息或内容标题中。

### 内容位置标题

Content-Location 是 URI 的表示，它标记了放置它的正文部分的内容。它的值可以是绝对或相对 URI。它可用于标记消息的部分或所有收件人无法检索的资源。单个消息仅允许具有单个 Content-Location 标头。包含具有 Content-Location 和 Content-ID 标签的正文部分的多部分/相关结构示例：

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML 聚合的 URI

MHTML 聚合的 URI 与其根 URI 不同。如果在多部分/相关标题的标题中使用 Content-Location 标题字段，则它应适用于整个聚合。类似地，当使用引用 MHTML 聚合的 URI 来检索此聚合时，检索到的资源集可能不同于使用其部分的 Content-Locations 检索到的资源集。例如，检索 MHTML 聚合可能会返回旧版本，而检索根 URI 及其内联链接对象可能会返回较新版本。

## 参考

* [聚合文档的 MIME 封装 - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML 文件格式 - 维基百科提供](https://en.wikipedia.org/wiki/MHTML)

