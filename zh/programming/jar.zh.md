{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","什么是 jar 文件","如何打开 jar 文件","扩展名","文件","jar 文件","jar 文件格式",".jar 扩展名" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java 存档文件格式",
  "description":"了解 JAR 文件格式和可以创建和打开 JAR 文件的 API。",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是 .jar 文件？

带有 .jar 扩展名的文件是一个 Java 存档文件，其中包含许多不同的应用程序相关文件作为单个文件。创建此文件格式是为了通过避免创建多个 HTTP 连接来降低通过 HTTP 事务在浏览器中加载下载的 Java Applet 的速度。单个 JAR 文件可以包含 Java 类文件（[.class](/zh/programming/class/)）、[images](/zh/image/) 和 [sounds](/zh/audio/)。应用程序开发人员可以对 JAR 文件中的各个项目进行数字签名以验证其来源。 JAR 文件通常用于创建包含与该 API 相关的特定功能的功能 API。

## JAR 文件格式

JAR 文件基于流行的 [ZIP 文件格式](/zh/compression/zip/)，它将其各个内容文件归档在单个文件中。 JAR 文件格式支持压缩，从而使下载的文件更小，从而进一步缩短下载时间。 Oracle 的 [JAR 文件规范](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) 文章提供了有关 JAR 文件内部规范的完整详细信息。

### 清单文件

创建 JAR 文件时，会在其中自动创建一个清单文件，其中包含有关 JAR 文件内容的元数据信息。该文件显示了打包在 JAR 文件中的内容。一个典型的清单文件如下所示，其中显示了 JAR 文件中包含的文件夹和类。

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### 清单规格

清单规范由 Oracle 定义如下。

`manifest-file`: main-section 换行符 \*individual-section

`main-section`: 版本信息换行符 \*main-attribute

`版本信息`：清单版本：版本号

`版本号` : 数字+{.digit+}*

`main-attribute`：（任何合法的主要属性）换行符

`individual-section`：名称：值换行符 \*perentry-attribute

`perentry-attribute`：（任何合法的 perentry 属性）换行符

`换行` : CR LF |低频 | CR（不跟LF）

`digit`: {0-9}

### 可执行 JAR

JAR 文件还可以包含可由 Java 虚拟机 (JVM) 执行的应用程序，类似于 Microsoft Windows 操作系统上的任何其他应用程序。在这种情况下，JVM 需要了解应用程序的入口点，即任何具有公共静态 void main 方法的类。清单文件使用以下格式的“Main-Class"标头标识此类：

```
Main-Class: com.example.MyClassName
```



## 参考

* [JAR 文件概述](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR 文件格式](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=他们%20are%20built%20on%20the,jar%20file%20extension.)

