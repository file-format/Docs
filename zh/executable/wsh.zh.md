{
  "date" : "2021-08-27",
  "keywords" :["wsh 文件","wsh 文件格式","什么是 wsh 文件","文件","wsh 示例","wsh 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 WSH 文件格式和可创建和打开 WSH 文件的 API。",
  "title" :"WSH - Windows 脚本文件",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## 什么是一 .wsh 文件？
扩展名为 .wsh 的文件包含某种编程语言脚本（如 VB 或 VBS 等）的属性和参数。WSH 的实际需要是使用它们来自定义某些脚本的执行。需要 WScript 或 CScript 才能运行，这两者都包含在 Windows 操作系统中。 WSH 文件最初是在 Windows 95 的安装光盘上提供的，作为可选的可配置和可安装的控制面板，然后是 Windows 98 的默认组件。

## WSH 文件格式
WSH（Windows 脚本宿主）可用于各种目的，包括管理,登录脚本和一般自动化。 WSH 为脚本运行建立环境。它调用合适的脚本引擎并分配一组服务和对象供脚本使用。这些脚本可以从 COM 对象或命令行模式以 GUI 模式运行，为用户提供交互式或非交互式脚本的灵活性。

＃＃＃ 例子
这是一个非常简单的示例，它显示了一些使用根 WSH COM 对象“WScript"来显示带有“确定"按钮的消息的 VBScript。当此脚本启动时，将调用 CScript 或 WScript 引擎并建立运行时环境。

```
WScript.Echo "Hello world"
WScript.Quit
```


## 参考

* [Windows 脚本宿主 - 维基百科提供](https://en.wikipedia.org/wiki/Windows_Script_Host)



