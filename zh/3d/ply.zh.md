{
  "date" : "2019-12-12",
  "keywords" :["层","文件","扩展","格式","3D文件格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解可创建和打开 PLY 文件的 PLY 文件格式和 API。",
  "title" :"PLY - 多边形 3D 文件格式",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ply 文件？

PLY，多边形文件格式，表示存储描述为多边形集合的图形对象的 3D 文件格式。这种文件格式的目的是建立一种简单易用的文件类型，该文件类型足够通用，可用于各种模型。 PLY 文件格式有 ASCII 和二进制格式，用于紧凑存储和快速保存和加载。该文件格式由支持 3D 文件读取的不同应用程序使用。

PLY 格式的对象由一组顶点、面和其他元素以及可以附加到这些元素的颜色和法线方向等属性来描述。也可以与对象一起存储的其他属性包括：

* 表面法线
* 纹理坐标
* 透明度
* 范围数据置信度
* 多边形正面和背面的属性

由 PLY 格式表示的对象可以是各种来源的结果，例如手动数字化对象、建模应用程序中的多边形对象、范围数据、行进立方体中的三角形、地形数据和辐射模型。

## 历史简介

PLY 格式是在 1990 年代由斯坦福图形实验室的 Greg Turk 和其他人开发的，这就是为什么它也被称为斯坦福三角格式。从那时起，文件格式的版本为 1.0，并且没有进行进一步的修改。

## 层文件格式

一个简单的 PLY 对象由用于表示对象的元素集合组成。它由一个顶点的 (x,y,z) 三元组列表和一个实际上是顶点列表索引的面列表组成。顶点和面是元素的两个示例，大部分 PLY 文件由这两个元素组成。也可以创建新属性并将其附加到对象的元素上，但这些属性的添加方式应使旧程序在遇到这些新属性时不会中断。这些属性也可以通过阅读应用程序丢弃。此外，可以创建新元素，也可以使用该元素定义属性。

### 文件结构

PLY 文件格式的文件结构如下：

|领域
---|
|文件头
|顶点列表
|人脸列表
|其他元素列表

#### 示例结构

我们将在后续讨论 PLY 文件格式的各个部分时使用下面的示例。

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### 文件头

PLY 文件格式标头由 ASCII 和二进制格式的 ASCII 文本组成。标题部分的开始和结束由 ply 和 end-header 关键字标识。标题的开头有魔术字ply，用于读者识别PLY文件格式。下一行显示此文件的版本号。 PLY 文件格式的注释在每条注释行的开头以注释关键字开头。

#### 元素关键字

然后 element 关键字告诉文件里面有什么。其后是该特定元素类型的属性，其中每个属性都指定了其属性类型和顺序，如下所示：

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

在这个特定的示例中，特定的顶点元素具有 3 个浮点类型的属性，并指定了它们的顺序。

#### 数据类型的类型

属性可能具有两种类型的数据类型。

`Scalar`：标量数据类型如下图：


|#Name|#Type|#字节数
|字符|字符|1
|uchar|无符号字符|1
|短|短整数|2
|ushort|无符号短整数|2
|int|整数|4
|uint|无符号整数|4
|float|单精度浮点数|4
|double|双精度浮点数|8

`List`：有一种特殊形式的属性定义使用列表数据类型。这方面的一个例子来自上面的多维数据集文件：

`属性列表 uchar int vertex_index`

这意味着属性“vertex_index"首先包含一个无符号字符，告诉该属性包含多少个索引，然后是一个包含那么多整数的列表。这个可变长度列表中的每个整数都是一个顶点的索引。

## 参考 ＃＃

* [PLY 文件格式](http://paulbourke.net/dataformats/ply/)
* [PLY - 维基百科提供](https://en.wikipedia.org/wiki/PLY_(file_format))

