{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS 文件格式 - 连接管理器服务配置文件",
  "description":"了解 CMS 文件和可以创建和打开 CMS 文件的 API。",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
    "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## 什么是 .cms 文件？

CMS 文件是包含 Microsoft Windows 连接管理器使用的配置文件信息的数据文件。它允许远程用户使用此配置文件信息连接到网络。存储在 CMS 文件中的信息包括有关用户操作系统的数据和用于在远程用户和网络之间建立连接的权限。 CMS 管理员使用连接管理器管理员工具包 (CMAK) 来生成 CMS 文件。

## CMS 文件格式 - 更多信息

CMS 文件通常不会在用户计算机上找到。由于这些专门用于允许远程用户访问网络，因此您会在用于连接到公司网络或某些特定用途的办公室的计算机上找到它们。在大多数情况下，它用于连接到组织网络，例如专用于公司的虚拟专用网络 (VPN)。作为网络管理员，您将使用 Connection Manager 设置对此类网络的访问，以允许他从远程位置访问公司网络。

### 什么是独立 CMS？

CMS 配置文件是使用连接管理器创建的，并在提供给远程用户之前与其他配置文件打包在一起。这些附加文件可能包括一个 CMP 和一个 INF 文件，它们与 [EXE](/zh/executable/exe/) 文件一起打包。这个完整的包被提供给远程用户用于连接到网络。

## 参考

* [了解和配置 Windows 连接管理器](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

