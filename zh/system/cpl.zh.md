{
  "date" : "2021-06-29",
  "keywords" :["CPL","扩展名","文件","格式","系统","控制面板文件","Windows","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - 控制面板文件",
  "description":"了解 CPL 文件格式和可以创建和打开 CPL 文件的 API。",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是一 .cpl 文件？ ##

CPL 文件是一种“系统"文件。它由 Windows 操作系统使用。 CPL 文件是控制面板文件的缩写。这些文件是在 Microsoft Windows 操作系统中通过控制面板打开的二进制文件，用于表示和打开控制面板中可用的工具，例如鼠标、显示器、网络等。 CPL 文件通常存储在设备上的系统文件夹中。不应手动打开这些文件。


## CPL 文件格式 ##

Windows 操作系统中的不同 CPL 文件连接起来代表不同的控制面板项目。所有控制面板项目都链接到 CPL 文件，并在其项目上附加了后缀“.cpl"。

一些常见的 CPL 文件类型及其格式包括：

* Inetcpl.cpl – 用于您设备上的 Internet 属性
* Appwiz.cpl – 在您的设备上添加或删除程序属性
* Desk.cpl – 用于显示属性
* Main.cpl – 用于与鼠标、字体、键盘和打印机相关的属性。
* Netcpl.cpl – 用于网络相关属性
* System.cpl – 用于系统相关属性和添加新硬件向导
* TimeDate.cpl – 用于日期或时间属性
* Mlcfg32.cpl – 用于 Microsoft Exchange 或 Windows 消息属性
* Intl.cpl – 这与区域设置属性有关
* Modem.cpl – 调制解调器相关属性
* Themes.cpl – 存储桌面主题和属性。
* Password.cpl – 用于密码属性
* Mmsys.cpl – 用于多媒体属性
* Wgpocpl.cpl – 与 Microsoft Mail 邮局相关

## 历史简介 ＃＃

CPL 文件类型由 Microsoft Windows 开发，是自 Windows 1.0 以来 Windows 操作系统的一个组成部分。它仍在所有 Windows 版本中使用，并且所有控制面板项属性都使用此文件类型存储。

## CPL 示例 ##

示例 CPL 文件如下所示：

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
