{
  "date" : "2021-08-02",
  "keywords" :["reg 文件","reg 文件格式","什么是 reg 文件","文件","reg 示例","reg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 REG 文件格式和可以创建和打开 REG 文件的 API。",
  "title" :"REG - Windows 注册表文件",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## 什么是一 .reg 文件？
REG 文件只是一个带有 .reg 扩展名的文本文件。这些文件通常是通过从注册表中导出典型键来创建的。这些文件也可以用作注册表的备份（特别是在进行更改之前这一步很重要！）。您可以看到，有些人在向您展示如何执行注册表黑客攻击的相同站点上将它们作为可下载文件提供。 REG 文件可用于手动更改注册表并导出这些更改。只需稍微清理一下文件，然后与他人共享。

## REG文件格式
REG 文件格式设计用于使用基于 INI 的语法导出和导入部分 Windows 注册表。 Windows 注册表是一个关系或分层数据库，用于保存 Microsoft Windows 操作系统和其他使用 Windows 注册表的应用程序的低级设置。 Alternativley，我们可以说，注册表或 Windows 注册表由安装在所有版本的 Microsoft Windows 操作系统上的程序和硬件的信息、选项、设置和其他值组成。
### REG 文件的语法
以下是作为 REG 文件语法一部分的一些关键元素：
- **RegistryEditorVersion**：例如“Windows 注册表编辑器版本 5.00"，适用于 Windows 2000、Windows XP 和 Windows Server 2003。
- **空白行**：标识新注册表路径的开始。
- **RegistryPathx**：包含您要导入的第一个值的子项的路径。
- **DataItemNamex**：要导入的数据项的名称。
- **DataTypex**：注册表值的数据类型。

密钥使用以下语法存储在 .reg 文件中：
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
您可以使用“@"而不是“值名称"来编辑键的默认值：
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
＃＃＃ 例子
这是一个REG文件的例子
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## 参考

* [Windows 注册表- 维基百科提供](https://en.wikipedia.org/wiki/Windows_Registry)
* [如何使用 .reg 文件添加、修改或删除注册表子项和值](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-注册表子键和值通过使用-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23）


