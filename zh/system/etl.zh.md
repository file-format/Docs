{
  "date" : "2022-02-22",
  "keywords" :["ETL","扩展名","文件","格式","系统","驱动程序","Windows 设备驱动程序","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ETL 文件 - Microsoft 事件跟踪日志文件",
  "description":"了解 ETL 文件格式和可以创建和打开 ETL 文件的 API。",
  "linktitle" : "ETL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-02-22"
}

## 什么是一 .etl 文件？

ETL 文件是包含 Microsoft 操作系统内核生成的事件日志的日志文件。这些日志文件包括应用程序和系统级错误、警告和其他事件数据。 ETL 文件有助于分析和解决系统级问题。 ETL 文件中记录的常见问题包括由磁盘访问和页面错误产生的问题。 Microsoft 提供了两个应用程序 Tracerpt 和 Event Viewer 来读取和查看 ETL 文件的内容。 ETL 文件可以使用 Tracerpt 转换为其他文件格式，例如 [TXT](/zh/word-processing/txt/) 和 [CSV](/zh/spreadsheet/csv/)。

## ETL 文件格式

ETL 文件以压缩二进制格式保存到磁盘以减少磁盘空间。

## 使用 Windows 性能分析器打开 ETL 文件

可以使用 Microsoft Windows 性能分析器 (WPA) 应用程序以表格和图形格式读取和可视化 ETL 文件数据。 [打开和分析 ETL 文件](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/opening-and-analyzing-etl-files-in-wpa) 指南提供了有关工作的信息与 ETL 文件。

## 参考

* [Windows 性能分析器](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/getting-started--windows-performance-analyzer--wpa-)
* [WPA 快速入门指南](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/wpa-quick-start-guide)

