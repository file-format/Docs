{
  "date" : "2021-07-07",
  "keywords" :["INI","扩展名","文件","格式","系统","启动","目录扩展名","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - 启动文件格式",
  "description":"了解 INI 文件格式和可以创建和打开 INI 文件的 API。",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## 什么是一 .ini 文件？ ##

INI 文件是计算机程序的消息配置文档，其中包含用于在框架和语法中组织属性的特征和部分的公钥。这些系统文件格式配置文件的名称来自 MS-DOS 操作系统的目录扩展名 INI，代表启动。它普及了这种形式的软件设置。其他软件应用程序上的许多程序使用各种文件名添加，例如 CONF 和 [CFG](/zh/system/cfg)，尽管该格式已在许多配置情况下建立了非官方标准。

## INI 文件简史##

最初，Windows 的主要程序配置技术是一种文本文件格式，它由文本行组成，每行有一对关键的文本，分为多个部分。设备驱动程序、字体和启动启动器都以这种格式存储。个别设置也通常由应用程序存储在 INI 文件中。
在 Windows 3.1x 之前，该格式在 16 位 Microsoft Windows 平台上受支持。从 Windows 95 开始，微软开始鼓励开发者使用 Windows 注册表而不是 INI 文件进行配置。

## INI 文件 - 文件格式规范

### 键/属性###

键/属性是 INI 文件的最基本元素。等号 (=) 分隔每个键的名称和值。等号左侧是显示名称的位置。等号和分号在 Windows 系统中是谨慎的字母，因此不能在键中使用。值中可以使用任何字符。

```
name=value
```

### 部分###

部分注释出现在方括号 ([]) 中，单独一行。在节定义之后，所有键都链接到该节。节在下一个节指定或文档结尾处结束；没有特定的“部分结尾"分隔符。部分不能堆叠；它们只能命名一次，不需要链接。

```
[section]
a=a
b=b
```

### 改变功能###

INI 文件格式没有全球公认的定义。许多计算机应用程序包括已经提到的功能之外的功能。下面的列表包括一些可能包含或可能不包含在任何单个程序中的常见特征。

* 注释
* 转义字符
* 重复的名字


## INI 示例 ##

示例 INI 文件如下所示：

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## 参考 ＃＃

* [DMP - 微软](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

