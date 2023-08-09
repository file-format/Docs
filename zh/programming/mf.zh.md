{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java 清单文件格式",
  "description":"了解 MF 文件格式和可以创建和打开 MF 文件的 API。",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .mf 文件？

扩展名为 .mf 的文件是一个 Java Manifest 文件，其中包含有关各个 [JAR](/zh/programming/jar/) 文件条目的信息。 MF 文件本身包含在 JAR 文件中，并提供所有扩展和包相关的定义。可以生成 JAR 文件以用作可执行文件。在这种情况下，mainfest 文件指定包含 **`public static void main`** 语句的应用程序的主类。清单文件被命名为 MANIFEST.MF，可以在 Windows、MacOS 和 Linux 操作系统上使用任何文本编辑器打开。

## 清单文件格式规范

Oracle 在其 JAR 文件格式指南中提供了 [清单文件格式规范](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)。 Manifest 文件由主要部分组成，其后是各个 JAR 文件条目的部分列表。每个部分都遵循一些规则和限制。

### 主要部分

主要部分：

* 包含有关 JAR 文件的安全性和配置信息
* 包含有关 JAR 文件所属的应用程序或扩展的信息
* 定义每个清单项的主要属性

**注意**：此部分中的任何属性都不能命名为“名称"。

### 个别部分

一个单独的部分定义了 JAR 文件的包或文件的各种属性。每个部分必须以一个名为“名称"的属性开头，其值必须是文件的相对路径，或者是引用存档外部数据的绝对 URL。

### 清单规格

|属性|说明|
---|---|
|manifest-file|main-section 换行 *individual-section|
|main-section|version-info 换行 *main-attribute|
|版本信息|清单版本：版本号|
|版本号|数字+{.digit+}*|
|主属性|（任何合法的主属性）换行符|
|individual-section|名称：值换行*perentry-attribute|
|perentry-attribute|（任何合法的 perentry 属性）换行符|
|换行|CR LF |低频 | CR（不跟LF）|
|数字|{0-9}|

## 参考

* [Oracle - JAR 文件格式](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR 文件格式](https://en.wikipedia.org/wiki/JAR_(file_format))

