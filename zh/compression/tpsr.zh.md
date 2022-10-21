{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR 文件格式 - TeamViewer Pilot 会话报告文件",
  "description":"了解 TPSR 文件格式和可以创建和打开 TPSR 文件的 API。",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## 什么是一 .TPSR 文件？

TPSR 是 TeamViewer Assist AR（以前称为 TeamViewer Pilot）使用的连接协议文件。存储在 TPSR 文件中的信息以压缩的 [ZIP](/zh/compression/zip/) 文件格式存储。 TPSR 包含专家和技术人员之间用于解决问题和审查目的的 TeamViewer 连接的详细历史记录。 TPSR 文件中包含的信息包括设备类型、名称、Assist AR ID、专家 ID、日期和时间以及连接持续时间。此数据存储在压缩的 TPSR 存档内的 [JSON](/zh/web/json/) 文件中。

## TPSR 文件格式

TPSR 文件以 ZIP 存档文件格式存储到光盘，其中内容存储在 JSON 文件中。如果在 TeamViewer 中启用了连接报告选项，它会在完成 Assist AR 连接后自动生成。

TeamViewer Assist AR 让专家连接到技术人员，通过移动摄像头获取远程端的实时信息。他们可以通过电话协助技术人员解决问题。

## 打开 TPSR 文件

您可以使用 TeamViewer 软件的桌面版本打开 TPSR 文件。如果安装在您的计算机上，双击 TPSR 文件将在 TeamViewer 软件中打开它。 TPSR 文件也可以导出为 [PDF](/zh/pdf/) 文件，也可以打印为协议文件的打印副本。

## 参考 ＃＃

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

