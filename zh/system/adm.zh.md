{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM 文件 - 管理模板文件格式",
  "description":"了解 ADM 文件格式以及如何打开 ADM 文件。",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## 什么是一 .adm 文件？

ADM 文件是 Microsoft 组策略软件使用的模板文件，用于指定注册表文件中基于注册表的策略设置的位置。系统管理员使用它来定义管理属于该组的计算机组的策略。此信息成为为管理组而创建的组策略对象 (GPO) 的一部分。

您可以使用 Microsoft 组策略对象编辑器打开 ADM 文件。

## ADM 文件格式 - 更多信息

ADM 文件存储为 unicode 格式的文本文件。这些主要用于描述 Windows Vista 和 Windows 7 注册表中基于注册表的策略设置的位置。

ADM 文件不再受支持，并已被 [ADMX](/zh/system/admx/) 文件取代。 GPA 会忽略运行 Microsoft Windows Vista Service Pack 1 或更高版本的计算机上的以下默认 ADM 文件。

* 系统.adm
* inetres.adm
*conf.adm
* wmplayer.adm
* wuau.adm

## 参考

* [管理模板文件 - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 管理管理模板文件](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

