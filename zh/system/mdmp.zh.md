{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP 文件 - Windows Minidump 文件格式",
  "description":"了解 MDMP 文件格式和可以创建和打开 MDMP 文件的 API。",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## 什么是一 .MDMP 文件？

MDMP 文件是 Microsoft Windows 上应用程序异常关闭或崩溃时创建的内存转储文件。它包含可用于调试崩溃原因的信息和数据转储。 MDMP 文件适用于由 Java、C++、.NET 等任何平台创建的应用程序。除了 MDMP，

可以打开 MDMP 文件的应用程序包括 Microsoft Visual Studio 调试器。

## MDMP 文件格式

MDMP 文件以二进制文件的形式保存到光盘中，并且可以使用 Microsoft Visual Studio 调试器打开。它包含以下信息以帮助确定崩溃的原因。

* 停止消息、其参数和其他数据的详细信息
* 加载的驱动程序列表
* 停止工作的处理器的处理器上下文 (PRCB)
* 停止进程的进程信息和内核上下文（EPROCESS）
* 停止线程的进程信息和内核上下文（ETHREAD）
* 停止的线程的内核模式调用堆栈

此信息有助于找出发生了什么、解决问题并防止它再次发生。

### 分析小型转储

Windows 需要启动卷上的页面文件来创建内存转储文件。页面文件是在引导卷上创建的，大小至少应为 2 兆字节 (MB)。转储文件是在应用程序崩溃时创建的。如果出现第二个问题，则会创建第二个小内存转储文件，而保留前一个。转储文件的名称是不同的，以避免任何覆盖。

Windows 在 %SystemRoot%\Minidump 文件夹中保留所有内存转储文件的列表。您可以通过在 Visual Studio 调试器中运行 MDMP 文件来分析它们，如下面的步骤中所列。

## 如何在 Visual Studio 中打开 MDMP 文件？

以下步骤可用于在 Visual Studio 中打开 MDMP 文件。

* 在 Visual Studio 中，从文件菜单中，选择打开 |崩溃转储 。
* 导航到要打开的转储文件。
* 选择打开。

## 参考

* [发生崩溃时如何读取Windows创建的小内存转储文件](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -文件）

