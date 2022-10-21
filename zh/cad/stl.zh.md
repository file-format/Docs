{
  "date" : "2020-03-16",
  "keywords" :["STL 文件","格式","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 STL 文件格式和可以创建和打开 STL 文件的 API。",
  "title" :"STL 文件格式",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .stl 文件？

STL，stereolithrography 的缩写，是一种可互换的文件格式，表示 3 维表面几何形状。该文件格式可用于多个领域，例如快速原型制作、3D 打印和计算机辅助制造。它将一个表面表示为一系列小三角形，称为小平面，其中每个小平面由一个垂直方向描述，三个点表示三角形的顶点。应用程序使用结果数据来确定制造商要构建的 3D 形状的横截面。 STL 文件格式中没有可用于表示颜色、纹理或其他常见 [CAD](/zh/cad/) 模型属性的信息。

## 历史简介 ＃＃

STL 文件格式的开发可以追溯到 1987 年。它是由 3D Systems 开发的，用于商业 3D 打印机。 STL 文件格式的修订版，称为 STL 2.0，于 2009 年提出，并对文件格式进行了更新。

## 文件格式规范##

STL 文件使用小平面表示表面几何。刻面定义了 3D 对象的表面，并由单位法线（垂直于长度为 1.0 的三角形的线）和三个顶点唯一标识。每个面总共存储了 12 个数字作为法线，每个顶点由三个坐标指定。 StL 文件不包含任何比例信息；坐标是任意单位。

STL文件格式的规范可以从以下两个方面来考察。

### 刻面方向###

小平面的方向由单位法线的方向和列出顶点的顺序决定。刻面的方向通过以下两种方式指定：

* 法线的方向是向外的
* 顶点从外部按逆时针顺序列出，遵守右手规则。

###顶点到顶点规则###

根据这个规则，每个三角形与其相邻的三角形共享两个顶点。因此，一个三角形的顶点不能位于另一个三角形的边上。

## 文件格式##

STL 可用于 ASCII 以及紧凑文件格式的二进制表示。

### STL ASCII 格式 ###

STL 文件格式的 ASCII 版本是用纯 ASCII 编写的。但是，由于文件格式较大，因此没有选择该文件格式作为使用的首选格式。 ASCII STL 文件的语法如下：
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
粗体字表示应始终为小写的关键字。斜体符号是要替换为用户指定值的变量。 **facet normal** 和 **vertex** 行中的数值数据是单精度浮点数，例如 1.23456E+789。 **facet normal** 坐标可能有一个前导减号； **顶点**坐标可能不会。

### STL 二进制格式 ###

二进制格式使用 IEEE 整数和浮点数值表示。文件格式表示如下：

|字段|信息|
---|---|
|标题|80 个字符|
|三角形数|4字节小端无符号整数|
|每个三角形的数据|12 个 32 位浮点数|

文件格式的更详细视图如下所示。

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## 参考 ＃＃

* [STL 格式](http://www.fabbers.com/tech/STL_Format)
* [STL - 维基百科](https://en.wikipedia.org/wiki/STL_(file_format))

