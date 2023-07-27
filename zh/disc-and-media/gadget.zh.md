{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 GADGET 文件格式和可以创建和打开 GADGET 文件的 API。",
  "title" :"小工具 - 虚拟 CD 文件",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## 什么是小工具文件？

GADGET 文件由在 Windows Vista 或 Windows 7 侧边栏中执行的小型软件程序组成。它压缩了几个基于 Web 的文件，这些文件可能包含 [.html](/zh/web/html/)、[.css](/zh/web/css) 或 [.js](/zh/web/js/) 文件，以及其他网页文件。 GADGET 文件用于小型组件，例如搜索工具、新闻提要、系统实用程序和小型游戏。尽管小工具由侧边栏托管，但并不特定于侧边栏区域；这些可以根据需要取消停靠并移动到桌面上。

## 小工具文件格式

GADGET 文件是一个重命名的 [ZIP](/zh/compression/zip/) 存档，其中包含 HTML、XML、JScript 和 CSS（层叠样式表）文件的集合。安装包括下载 .gadget 文件并启用下载过程以安装组件或将 .gadget 文件保存到本地系统并双击以开始安装过程。

基本上，GADGET 包含两个文件：

1. **Gadget.xml**：清单，一个 XML 文件，包含小工具的一般表示和配置信息。
2. **name.html**：一个 HTML 文件，其中的名称在<name>关联小工具清单的标记，它提供小工具 UI 的包装器并包含小工具的核心功能。

GADGET 文件的多个实例可以同时运行。例如，如果有人想知道不同时区的时间，他们可以通过将每个时钟设置为特定时区来运行时钟小工具的多个实例。

### GADGET 停产

由于 Windows 7 中的 Windows Sidebar 平台存在严重漏洞，微软官方网站上不再提供 Gadgets。后来，Microsoft 在较新版本的 Windows 中停用了此功能。 GADGET 可以随时被利用来访问计算机的文件、损害计算机、泄露令人反感的内容或改变他们的行为。

## 参考

* [Windows 边栏 - Microsoft 提供](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [为 Windows 边栏开发小工具第 1 部分](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

