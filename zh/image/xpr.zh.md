{
  "date" : "2022-03-21",
  "keywords" :["xpr 文件","xpr 文件格式","什么是 xpr 文件","文件","xpr 示例","xpr 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR 文件格式 - Microsoft 表达式设计图形文件",
  "description":"了解 XPR 文件格式和可创建和打开 XPR 文件的 API。",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## 什么是一 .xpr 文件？

XPR 文件是使用现已停产的 Microsoft Expression Graphics (EGD) 软件创建的矢量图像文件。它包含可用作用户界面模型的图形信息。 XPR 文件后来被 Microsoft Expression Design 中的 .design 文件取代。 XPR 文件可以使用已停产一段时间的 Microsoft Expression Studio 打开。

## XPR 文件格式漏洞

XPR 文件被确定为利用 Microsoft Expression Design 中的一个漏洞，从而允许执行远程代码。在报告的问题中，如果用户打开网络目录中的合法 .xpr 文件以及动态链接库 (DLL) 文件，Microsoft Expression Design 可能会尝试加载 DLL 文件并执行其中包含的代码。微软后来在安全更新中修复了这个问题。

## 参考

* [表达式设计中的漏洞可能允许远程执行代码 (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

