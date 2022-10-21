{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC 文件 - Google 文档快捷方式",
  "description":"了解什么是 GDOC 文件以及可以创建和打开 GDOC 文件的 API。",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## 什么是一 .gdoc 文件？

GDOC 文件是指向位于 Google Drive（一种基于云的文档存储服务）上的文件的快捷方式文件。当计算机上安装了Google Drive客户端并在其中创建了一个文档时，驱动器会在在线云存储中创建一个文档，并将该文档的[URL](/zh/web/url/)写入本地Google的GDOC文件中驱动器文件夹。双击此快捷方式文件时，默认 Web 浏览器会从 [URL](/zh/web/url/) 位置打开文档。如果将此快捷方式文件移出此文件夹，则联机文档的链接将断开。

## GDOC 文件格式 - 更多信息

GDOC 文件包含以 [JSON](/zh/web/json/) 文件格式编写的在线文档的快捷方式。打开 GDOC 文件的浏览器会读取 URL 信息并打开链接的文档以供显示，前提是用户登录到存储文档的 Google 帐户。 GDOC 文件不包含文档的内容。

### GDOC 文件示例

GDOC 文件可以在文本编辑器中打开，其内容如下所示。

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

可以看出，内容采用 JSON 格式，具有文档的 URL 和相关的文档 ID。

## 参考

* [Google Docs 无法打开 gdoc 或 docx 文件](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

