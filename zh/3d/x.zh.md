{
  "date" : "2020-01-11",
  "keywords" :[ "x 文件","x 文件格式","什么是 x 文件","文件","x 示例","x 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 文件格式",
  "description":"了解 DirectX X 文件格式和可以打开和创建 DirectX X 文件的 API。",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## 什么是 .x 文件？

带有 .x 扩展名的文件是指 Microsoft DirectX 2.0 引入的 [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D 图形旧文件格式。它用于游戏中的 3D 图形渲染，并指定网格、纹理、动画和用户定义对象的结构。自 2014 年以来，它已被弃用，因为 Autodesk FBX 文件格式更适合作为更现代的格式。 X 是模板驱动的，不需要任何使用知识。您可以使用 Microsoft DirectX 和常用文本编辑器打开 DirectX X 文件。

## X 文件格式

[X 文件参考](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) 包含 API 元素的参考信息，这些元素用于使用 DirectX .x 文件。该格式提供低级数据原语，其他应用程序使用这些原语通过数据模板定义高级原语。 DirectX 6.0 引入了能够读取和写入 .x 文件的接口和方法。 DirectX 3.0 引入了这种文件格式的二进制版本。

DirectX 9 定义的[X 文件格式参考](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) 包含.x 的参考信息二进制文件和文本编码。

### 二进制编码

[二进制格式](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) 将 DirectX X 格式定义为文本格式的标记化表示。这些标记可以是独立的以提供语法结构，也可以是提供必要数据的记录标记。

#### 标题

可以使用以下定义读取和写入二进制标头。

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### 文本编码

DirectX .x 文件不依赖于文件的使用方式，也不特定于任何应用程序。这种模板驱动的方法允许任何客户端应用程序使用 .x 文件格式。


#### 标题

可变长度标头是强制性的，并且必须位于数据流的开头。标头包含以下数据。

|类型 |子类型 |大小 |内容 |内容含义|
---|---|---|---|---|
|幻数（必填）| | 4 字节 |xof |
|版本号（必填） |主要版本 |2 字节 |03 |主要版本 3|
| |次要编号 |2 字节 |02 |次要版本 2|
|格式类型（必填）| |4 字节 |"txt" |文本文件|
| | | |“箱"|二进制文件|
| | | |"tzip"| MSZip 压缩文本文件|
| | | |"压缩包"| MSZip 压缩二进制文件|
|浮动尺寸（必填）| |4 字节| 0064| 64位浮点数|
| | | |0032 |32 位浮点数|


## 参考

* [X 文件旧版](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 文件格式参考](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

