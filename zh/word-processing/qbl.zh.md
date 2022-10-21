{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks 许可文件",
  "description":"了解 QBL 文件格式和可以创建和打开 QBL 文件的 API。",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## 什么是一 .qbl 文件？

扩展名为 .qbl 的文件是 QuickBooks 许可文件，其中包含用户购买的副本的许可信息。它通常在安装 QuickBooks 后以 `license.qbl` 的名称存储在本地系统中，用户在第一次运行软件时在软件中输入许可信息。 QBL 是用于存储 QuickBooks 许可信息的早期文件格式。它现在已被 QuickBooks `qbregisteration.dat` 文件替换，并填充了来自用户确认电子邮件、购买的 DVD 或通过其他购买方式的信息。 QBL 文件可以在任何文本编辑器中打开，例如 Windows Notepad、Apple TextEdit、Notepad++、Github Atom 编辑器等等。

## QBL 文件格式 - 更多信息

QBL 文件以纯文本文件的形式创建和存储。这些文件中的信息是人类可读的，并且可以在文本编辑器中打开这些文件时进行编辑/更新。然后可以将许可和用户注册信息复制到此文件中，以便开始使用 QuickBooks 软件。 QBL 文件通常存储在 Windows 操作系统上的 Program Files\Intuit\QuickBooks\INET 目录中。

QBL 文件包含两种类型的信息。

* `QuickBooks版本信息：`指的是QuickBooks的安装版本，格式如xx.x
* `License Key:` 000-000 0000-0000-0000-000 000073adbf3f 格式的文本，其中 000-000 0000-0000-0000-000 替换为用户的 qbregisteration 密钥

## 参考

* [Intuit 的 QuickBooks](https://quickbooks.intuit.com/)
* [QuickBooks - 生成 qbregistration.dat 文件](https://quickbooks.intuit.com/learn-support/en-us/license-information/create-or-re-create-the-qbregistration-dat-file/ 00/186082)

