{
  "date" : "2019-12-12",
  "keywords" :["FBX","文件","扩展名","格式","3D 文件格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"您的文件格式指南，了解什么是 FBX 文件以及可以创建和打开它们的 API。",
  "title" :"FBX - FilmBox 3D 文件格式",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .FBX 文件？

FBX，FilmBox，是一种流行的 3D 文件格式，最初由 Kaydara 为 MotionBuilder 开发。它于 2006 年被 Autodesk Inc 收购，现在是许多 3D 工具使用的主要 3D 交换格式之一。 FBX 提供二进制和 ASCII 文件格式。建立该格式是为了提供数字内容创建应用程序之间的互操作性。有许多工具可用于从/到 FBX 文件格式的转换。

## FBX 文件格式 - 更多信息

FBX 是一种专有格式，官方没有关于其二进制文件格式的规范。 Autodesk 提供了一个 C++ FBX SDK，用于从 FBX 文件读取、写入和转换。 FBX 的 Python 导入和导出脚本也可用于不使用 FBX SDK 的 Blender 软件。

### 基于文本的文件结构###

基于文本的文件结构是具有明确命名标识符的树状文档。它由按层次结构排列的节点的嵌套列表组成，其中每个节点具有：

* 一个 NodeType 标识符（类名）
* 与其关联的属性元组，元组元素是通常的原始数据类型：##float、integer、string## 等。
* 包含相同格式（递归）节点的列表。

这些可以在逻辑上表示如下：

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

一些标准节点被定义为隐式列表，其中每个项目都由一个嵌套列表组成。任何打算访问 FBX 几何图形的应用程序都必须解析这些内容并赋予其有用的意义。基于文本的 FBX 文件的示例如下所示：

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## 二进制文件结构##

如前所述，FBX 文件格式规范未公开用于 FBX。由于 Blender 基金会在没有使用公司提供的 SDK 的情况下实现了 FBX 文件格式，所以关于二进制文件格式的一些细节是 [available](https://code.blender.org/2013/08/fbx-binary-file-format -specification/) 作为它实现的一部分。

二进制文件结构遵循以下顺序：

* 标题
* 对象记录
* 页脚

### 标题###

文件头信息由 27 个字节组成。

* 字节 0 - 20：Kaydara FBX 二进制 \x00（文件魔术，末尾有 2 个空格，然后是 NULL 终止符）。
* 字节 21 - 22：[0x1A, 0x00]##（未知，但所有观察到的文件都显示这些字节）。
* 字节 23 - 26：无符号整数，版本号。例如 7.3 版的 7300。

### 对象记录###

Header 后面是一个对象记录，它是一个完整的节点记录，具有空名称和空属性列表。它递归地包含整个文件结构。

###页脚###

FBX 页脚部分位于内容未知的文件末尾。

## 记录格式##

FBX 文件中的记录分为以下几类：

* 节点记录
* 财产记录

### 节点记录格式###

每个节点记录格式都被命名并具有以下内存布局。


|大小（字节）|日期类型|名称
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|名称长度|字符|名称
|?|?|Property[n]，其中 n = 0:PropertyListLen
|可选| |
|?|?|嵌套列表
|13|uint8[]|空记录

在哪里：

* `EndOffset` 是从文件开头到节点记录结尾的距离（即接下来的第一个字节）。这可用于轻松跳过未知或不需要的记录。
* `NumProperties` 是与节点关联的值元组中的属性数。作为最后一个元素的嵌套列表不计为属性。
* `PropertyListLen` 是属性列表的长度。这是存储##NumProperties## 属性所需的大小，这取决于属性的数据类型。
* `NameLen` 是对象名称的长度，以字符为单位。 this 为 0 的唯一情况似乎是顶级列表。
* `Name` 是对象的名称。没有零终止。
* `Property[n]` 是第 n 个属性。有关格式，请参阅属性记录格式部分。属性是按顺序写入的，没有填充。
* `NestedList` 是嵌套列表，它的存在由最后的 NULL 记录指示。

可以通过检查在到达 EndOffset 之前是否还有剩余字节来确定嵌套列表条目的存在。如果是这样，则应在最后一个属性之后直接读取下一个对象记录。然后对象记录跟随 13 个零字节，然后与 EndOffset 组合。 NULL 条目的用途或要求未知，可能指向某些格式特征。

### 属性记录格式###

属性记录包含有关属于节点的属性的详细信息。属性记录具有以下内存布局：


|大小（字节）|数据类型|名称
--- | --- | ---
|1|char|类型代码
|?|?|数据

TypeCode 表示按需要类似处理的组排序的字符代码。 TypeCode 可以分为以下类型，TypeCode 可以是这些类型中的一种字符代码。

#### 原始类型####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

原始标量类型记录中的数据正是该值的二进制表示，采用 little-endian 字节顺序。

#### 数组类型####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

数组类型的数据更复杂，结构如下。


|大小（字节）|数据类型|名称
--- | --- | ---
|4|Uint32|数组长度
|4|Uint32|编码
|4|Uint32|压缩长度
|?|?|目录

### 特殊类型###

以下是特殊类型类型代码。

```
S: String
R: raw binary data
```

这两个 TypeCode 都表示如下：


|大小（字节）|数据类型|名称
--- | --- | ---
|4|Uin32|长度
|长度| |

该字符串不是以零结尾的，并且很可能包含 \0 字符（这实际上在某些 FBX 属性中使用）。

## 参考 ＃＃

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [FBX 二进制文件格式规范](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - 维基百科](https://en.wikipedia.org/wiki/FBX#File_format)

