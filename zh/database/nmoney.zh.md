{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 NMONEY 文件格式以及可以创建和打开 NMONEY 文件的 API。",
  "title" :"NMONEY 文件 - Denaro 账户文件格式",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## 什么是 NMONEY 文件？

NMONEY 文件是一个金融数据存储数据库文件，其中包含金融交易的跟踪记录。它由 Nickvision 开发，并用于 Nickvision Denaro 软件，这是一款个人财务软件应用程序。 NOMONEY 文件中存储的数据包括帐户的贷记和借记交易信息。

NOMONEY 文件可以使用 [Github](https://github.com/NickvisionApps/Denaro) 应用程序打开。

## 关于 Denaro 软件

Denaro 最初由 [Nickvision](https://nickvision.org/) 开发作为产品，后来转换为托管在 [Github](https://github.com/NickvisionApps/Denaro) 上的开源软件应用程序。从那时起，应用程序仅在 Github 上进行了修改和更新。该应用程序是使用 Windows App SDK（目前为 WinUI 3）在 Windows UI 中用 C# 开发的。

### Denaro 提供的功能

* 通过其最受欢迎和熟悉的选项卡界面同时管理多个帐户
* 按类型、组或日期过滤交易
* 重复交易，例如每月发生的账单
* 将钱从一个帐户转移到另一个帐户
* 将账户数据导出为 CSV 文件，并导入 CSV、OFX 或 QIF 文件以将交易添加到账户

## Denaro 文件格式 - 更多信息

Denaro 文件以二进制文件格式保存到光盘上。财务数据以 **.SQLITE3** 文件格式存储为数据库文件。 SQLITE 是使用 SQLite 软件创建的轻量级 SQL 数据库文件。它提供独立的数据库引擎，能够提供功能齐全且高度可靠的数据库。 SQLite 数据库文件可用于在系统之间共享丰富的内容，只需通过网络交换这些文件即可。 SQLite 绑定适用于 C、[C#](/zh/programming/cs/)、[C++](/zh/programming/cpp/)、[Java](/zh/programming/java/)、[PHP](/zh/programming/php/) 等。

## 参考

* [尼克视觉](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

