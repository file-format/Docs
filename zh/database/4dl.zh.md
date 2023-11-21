{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 4DL 文件格式以及可以创建和打开 4DL 文件的 API。",
  "title" :"4DL - 第四维数据库日志文件",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## 什么是4DL文件？

4DL 日志文件用于记录对 4D 数据库 (.4DD) 文件所做的修改。该文件与数据库文件一起存储，并共享相似的文件名。其目的是准确跟踪和维护数据库内实施的更新的全面记录。与 4DL 文件相比，[4DD 文件](/zh/database/4dd/) 主要与 4D Inc. 的第 4 维度相关。

## 4DL 文件格式 - 更多信息

通常，多个 4DL 文件与 4DD 文件存储在一起。因此，日志文件的第一个版本可能被命名为0001.4dl，但日志文件的横向版本将被保存为0002.4dl、0003.4dl等。现在，如果日志文件本身经历了 3 次后续保存，它将被标记为“db1[0005-0003].4dl”。

## 参考

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
