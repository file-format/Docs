{
  "date" : "2019-10-11",
  "keywords" :["adr",".adr 文件","文件格式","文件类型","什么是 adr 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADR - Opera 书签文件格式",
  "description" :"了解什么是 ADR 文件以及可以创建和打开 ADR 文件的 API。",
  "linktitle" : "ADR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-06"
}

## 什么是一 .adr 文件？

ADR 文件（以 .adr 扩展名保存）是由 Opera Web 浏览器创建的书签列表。当用户不断为 Web URL 添加书签时，此列表会被填充。这些书签存储在 ADR 文件中，需要时可以备份和恢复。由于大多数浏览器（例如 Chrome 和 Firefox）以 [HTML](/zh/web/html/) 格式保存书签，因此可以将其转换为 ADR 文件格式以便在 Opera 浏览器中导入。 ADR 文件可以在 Opera 浏览器中打开。

## ADR 文件格式 - 更多信息

ADR 文件的内部文件格式详细信息未知。但是，使用不同版本的 Opera 导出的 ADR 文件格式存在差异。这使得 [合并 ADR 文件](https://superuser.com/questions/471959/how-do-i-merge-several-opera-adr-bookmark-files-to-one-single-file) 生成变得困难与不同版本的 Opera。不过，可以使用一些外部工具来合并这些。

## 参考

* [合并 ADR 文件](https://superuser.com/questions/471959/how-do-i-merge-several-opera-adr-bookmark-files-to-one-single-file)

