{
  "date" : "2022-06-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ECS 文件格式 - 索尼爱立信手机备份文件",
  "description":"了解 ECS 文件格式和可以创建和打开 ECS 文件的 API。",
  "linktitle" : "ECS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-30"
}

## 什么是一 .ecs 文件？

ECS 文件是索尼爱立信手机创建的数据备份文件。它存储用户数据的副本作为备份，以防需要恢复以恢复存储的数据。 ECS 文件保存为压缩的 [ZIP](/zh/compression/zip/) 档案，以减少磁盘空间的使用。这也使得通过低速互联网连接传输数据变得容易。

## ECS 文件格式 - 更多信息

ECS 文件保存为压缩的 ZIP 档案。它可以使用任何标准解压缩程序（如 WinZip 和 WinRAR）打开。为此，将文件扩展名从 .ecs 重命名为 .zip 并使用 WinZip 提取内容。

## 参考

* [Dzip](https://speeddemosarchive.com/dzip/)

