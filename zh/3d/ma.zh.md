{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma 文件", "ma 文件格式", "文件格式", "3d","ma 文件下载", ".ma 文件", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 MA 文件格式和可以打开和创建 MA 文件的 API。",
  "title" :"MA 文件格式",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## 什么是一 .ma 文件？

扩展名为 .ma 的文件是使用 Autodesk Maya 应用程序创建的 3D 项目文件。它包含大量文本命令以指定有关文件的信息。 **.ma 文件** 可以在任何文本编辑器中打开和编辑，以修复命令的任何问题，以防文件损坏。这些文件包含用于定义 3D 场景信息的信息，例如几何、照明、动画和渲染。

## MA 文件格式

MA 文件以 ASCII 文本格式保存到磁盘，与 MB 文件以二进制文件格式保存到磁盘不同。 [Autodesk Maya 文档](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) 中提供了 MA 文件格式的详细参考，可以参考供开发者参考。

### MA 文件头

MA 文件头以一段注释开头，其中给出了文件的创建信息和修改日期。 Maya 文件阅读器会忽略此块，因为它仅用于信息目的。但是，标题必须以“//Maya"的前六个字符开头。

ASCII 文件头如下所示。

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### 文件引用

.ma 文件的文件引用部分包含有关此文件中引用的所有其他 Maya 文件的信息。可以使用包含在同一文件中的单个文件命令来读取每个引用的文件。用于引用时文件命令的语法是：

```
file -r -rpr prefixString fileName;
```
或者

```
file -r -ns nameSpace fileName
```
这是一个示例字符串。

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
这个例子表明包含在文件`solar`中的太阳对象可以在这个文件中使用名称“solar_sun"来访问。

＃＃＃ 要求

.ma 文件的需求部分由一系列必需的命令组成，并告诉 May 信息，例如读取文件所需的版本和插件信息。需求部分的示例如下。

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


下一节将详细说明要求。这由一系列需求命令组成。文件的这一部分告诉 Maya 需要什么软件才能正确加载文件。具体来说，什么版本的 Maya，什么插件。

## MA文件下载
很难找到和下载 3d 模型的 MA 文件。因此，您可以从此处下载示例 MA 文件：

- [样本.ma](../sample.ma)


## 参考

* [Maya ASCII 文件的组织 - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

