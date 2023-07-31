{
  "date" : "2021-06-29",
  "keywords" :["DLL","扩展","文件","格式","系统","动态链接库","设置","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - 动态链接库",
  "description":"了解 DLL 文件格式和可以创建和打开 DLL 文件的 API。",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是 DLL 文件？ ##

DLL 文件或动态链接库是一种可执行文件。它是您设备上最常见的扩展文件之一，通常存储在 Windows 上的 System32 文件夹中。 DLL 扩展文件由 Microsoft 开发，并被他们广泛使用。它具有很高的人气用户评级。 DLL 作为一个架子工作，其中包含为 Windows 服务器设计和应用的程序/应用程序的*驱动程序/过程/功能/属性*。单个 DLL 文件也可以在各种 Windows 程序之间共享。这些扩展文件对于在您的设备上顺利运行 Windows 程序至关重要，因为它们负责在程序上启用和运行各种功能，例如写入和读取文件，与您的设置外部的其他设备连接。
然而，这些文件只能在支持任何版本的 Windows（windows 7/windows 10/等）的设备上打开，因此不能直接在支持 Mac OS 的设备上打开。 （如果您想在 Mac OS 上打开 DLL 文件，各种外部应用程序可以帮助打开它们。）


## DLL文件格式##

DLL 文件由 Microsoft 开发，具有代表类型的扩展名“.dll"。它已成为 Windows 1.0 服务器及更高版本不可分割的一部分。它是一种二进制文件类型，所有版本的 Microsoft Windows 都支持。创建此文件类型是为了在 Windows 程序中创建共享库系统，以允许在程序库中进行单独和独立的编辑或更改，而无需重新链接程序。


## DLL 示例 ##

可以在下面找到 DLL 入口点的示例代码：

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## 参考 ＃＃

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
