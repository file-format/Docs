{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX 文件 - 组策略管理模板文件格式",
  "description":"了解 ADMX 文件格式以及如何打开 ADMX 文件。",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## 什么是 ADMX 文件？

ADMX 文件是 Microsoft Windows 组策略软件使用的策略配置文件，用于管理组中的计算机组。它是一个基于 XML 的管理模板文件，随 Windows Vista Service Pack 1 一起引入。ADMX 文件包含用户帐户、操作系统配置和应用程序的配置设置。 ADMX 文件用于存储和部署配置，以集中管理许多计算机系统。

您可以使用任何 XML 兼容的文本编辑器或 Microsoft 组策略对象编辑器创建或编辑 ADMX 文件。

## ADMX 文件格式 - 更多信息

ADMX 文件以人类可读的通用 [XML](/zh/web/xml/) 文件格式存储。它是多语言文件格式，允许不同语言的系统管理员使用相同的 ADMX 文件。 ADMX 文件取代了旧的 [ADM](/zh/system/adm/) 文件格式，这是一种 unicode 格式的文本文件格式。 ADMX 文件指定在更改特定组策略设置时更改的注册表项。

### ADMX 文件可以做什么？

ADMX 文件定义允许组中的用户计算机执行哪些操作。组策略结合 Active Directory 软件实施规则集。 ADMX 文件通过 Windows 操作系统上的中央存储进行管理，该操作系统是域中的中央位置。

部署在工作环境中的 ADMX 文件可以让管理员实施以下策略：

* 控制互联网的使用
* 下载某些类型的文件
* 在系统上使用可移动设备

## 参考

* [管理模板文件 - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - 管理管理模板文件](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

