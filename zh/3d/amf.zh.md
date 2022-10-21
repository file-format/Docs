{
  "date" : "2019-10-11",
  "keywords" :["amf","amf 文件","amf 文件格式","文件格式","3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 AMF 文件格式和可以打开和创建 AMF 文件的 API。",
  "title" :"AMF - 增材制造文件",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .amf 文件？
AMF 文件包含对象描述指南，以供增材制造过程使用。它包含一个开口<amf>XML 标记并以</amf>元素。这前面是一个 XML 声明行，指定文件的 XML 版本和编码。声明可以包含测量单位信息，如果没有此类信息，则使用毫米作为默认单位。


## AMF 文件格式
增材制造文件格式 (**AMF**) 定义了对象描述的开放标准，以便供 3D 打印等增材制造工艺使用。 CAD 程序通过利用对象的几何形状、颜色和材料等信息来使用 AMF 文件格式。 AMF 与 STL 格式不同，因为横向不支持颜色、材料、格子和星座。



### AMF 文件的元素

定义的五个顶级元素<AMF>标签如下所述。功能齐全的 AMF 文件必须存在单个对象元素。

`<object> ` - 对象元素定义了一个或多个材料体积，每个材料都与一个用于打印的材料 ID 相关联。文件中必须至少存在一个对象元素。附加对象是可选的。

`<material> ` - 可选材料元素定义一种或多种用于打印的材料以及相关的材料 ID。如果不包含任何材料元素，则假定为单一默认材料。

`<texture> ` - 可选的纹理元素为颜色或纹理映射定义一个或多个图像或纹理，每个图像或纹理都有一个关联的纹理 ID。

`<constellation> ` - 可选的星座元素分层地将对象和其他星座组合成一个用于打印的相对模式。

`<metadata> ` - 可选的元数据元素指定有关文件中包含的对象和元素的附加信息。

## AMF 示例

以下是 AMF 文件的示例，可以将其复制到 [text](/zh/word-processing/txt/) 文件并保存为压缩的 [zip](/zh/compression/zip/) 文件以供打开。
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## 参考

* [AMF - 维基百科](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [ISO 上的 AMF 规范](https://www.iso.org/standard/67472.html)

