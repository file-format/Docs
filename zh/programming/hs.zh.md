{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell 脚本文件格式",
  "description":"了解什么是 HS 文件格式以及可以创建和打开 HS 文件的 API。",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java 帮助集文件格式

## 什么是 Java HS 文件？

Java 编程语言中扩展名为 .hs 的文件是一个帮助文档文件，当 JavaHelp 系统被应用程序激活时，它会使用该文件。它为安装的特定应用程序定义了帮助集，并由多个子集组成，作为应用程序系统帮助的一部分。 Java 程序必须能够找到名称以 .hs 扩展名结尾的帮助集文件。

## Java 帮助集信息

.hs 文件可能包含以下信息。

|信息|说明|
---|---|
|映射文件|映射文件用于将主题ID与超文本标记语言主题文件的统一资源定位符或路径名相关联。|
|查看信息|描述帮助集中使用的导航器的信息。质量导航器是：目录、索引和全文搜索。其他导航器包括光泽和收藏夹导航器。此处进一步包含有关自定义导航器的数据。|
<html>|帮助标题|\<title>在帮助集 (.hs) 文件中进行了概述。此标题似乎位于帮助集文件中列出的最多窗口和任何辅助窗口的最高处。| </html>
|Home ID|调用协助观察者时显示的（默认）ID 的标题，但未指明 ID。|
|Presentation|显示帮助主题的窗口。这可以是 JavaHelp 2 计算机程序的现代包含，在 \ 下面有更详细的描述<presentation>.|
|子帮助集|这个任意区域通过使用标签静态合并其他帮助集。此标记显示的帮助集自然地组合到包含该标记的帮助集中。更多关于混合的兴趣点可以在混合帮助集中找到。|
|实现|此任意段创建一个注册表，该注册表提供关键信息映射以表征在 HelpSet.createHelpBroker 方法中使用的 HelpBroker 类。此外，注册表还为给定的 Emulate 排序决定了客户端的物质查看器。

## Java HS 文件格式

Java HS 文件为 XML 文件格式，并基于万维网联盟 (W3C) 扩展标记语言提出的建议 [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208）。这意味着 Java HS 文件是人类可读的 XML 文件格式，可以在任何 XML 阅读器应用程序中打开。

### Java HS 文件格式示例

以下是来自 [Oracle Helpset 文档](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html) 的帮助集文件示例。

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## 参考
* [Oracle Java 帮助集文件](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell 脚本文件格式

## 什么是一 .hs 文件？

带有 .hs 扩展名的文件是用 [Haskell](https://wiki.haskell.org/Haskell) 编写的 Haskell 脚本文件，这是一种高级纯功能开源编程语言。用 HS 文件编写的代码完全基于函数，不像 [C](/zh/programming/c/)、[C++](/zh/programming/cpp/) 等，它们遵循快速开发健壮和简洁软件的原则。 Haskell 提供内置的并发性和并行性以及丰富的 API、分析器和调试器，以生成灵活和高质量的应用程序。

## HS 文件格式

与任何编程语言一样，HS 文件以人类可读的纯文本格式编写。可以使用任何可用的文本工具创建、编辑和查看这些内容。 .hs 源代码文件使用 Haskell 编译器编译，生成可执行的二进制文件。

### HS 文件格式示例

代码可以写在 .hs 文件中，并使用 Haskell 编译器进行编译，例如 [GHC](https://haskell.org/ghc)。以下代码行保存为 `HelloWorld.hs`，如以下示例所示。

```
main = putStrLn "Hello, World!"
```

这是使用以下命令编译的：

```
$ ghc -o hello hello.hs
```
并且生成的可执行文件可以运行为：

```
$ ./hello
```
这将打印“Hello, World!"对输出的声明。

## 参考

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell 5 个简单步骤](https://wiki.haskell.org/Haskell_in_5_steps)

