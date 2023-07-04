{
  "date" : "2021-02-01",
  "keywords" :["usd","usd 文件","usd 文件格式","文件格式","文件","扩展名","3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"美元 - 通用场景描述格式",
  "description":"了解美元文件格式和可以打开和创建美元文件的 API。",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## 什么是一美元文件？

具有 .usd 扩展名的文件是一种通用场景描述文件格式，它对数据进行编码，以便在数字内容创建应用程序之间进行数据交换和扩充。由 Pixar 开发的 [USD](https://openusd.org/release/intro.html) 提供了交换元素资产（例如模型）或动画的能力。

## 美元文件格式

USD 文件可以具有二进制格式（也称为 Crate 文件）或 ASCII 支持的文件。这两种文件格式都是可以互换的，其中引用可以链接到 .usd 资产而无需更改源。 USD 文件格式由一组带有 Python 脚本绑定的 C++ 库组成。它可以组装和组织任意数量的 3D 场景元素，例如虚拟场景、场景和镜头，以便在应用程序之间传输它们。

### 美元数据类型

USD 文件格式支持的基本数据类型如下表所示。

|值类型标记 |C++ 类型 |描述|
---|---|---|
|布尔|布尔||
|uchar|uint8_t|8 位无符号整数|
|int|int32_t|32 位有符号整数|
|uint|uint32_t|32 位无符号整数|
|int64|int64_t|64 位有符号整数|
|uint64|uint64_t|64 位无符号整数|
|half|GfHalf|16 位浮点|
|float|float|32 位浮点|
|双|双|64位浮点|
|timecode|SdfTimeCode|表示可解析时间的双精度|
|string|std::string|stl 字符串|
|token|TfToken|具有快速比较和散列的内部字符串|
|asset|SdfAssetPath|表示另一个资产的可解析路径|
|matrix2d|GfMatrix2d|2x2 双精度矩阵|
|matrix3d|GfMatrix3d|3x3 双精度矩阵|
|matrix4d|GfMatrix4d|4x4 双精度矩阵|
|quatd|GfQuatd|双精度四元数|
|quatf|GfQuatf|单精度四元数|
|quath|GfQuath|半精度四元数|
|double2|GfVec2d|2 个双精度的向量|
|float2|GfVec2f|2 个浮点数的向量|
|half2|GfVec2h|2 个半的向量|
|int2|GfVec2i|2 个整数的向量|
|double3|GfVec3d|3 个双精度的向量|
|float3|GfVec3f|3 个浮点数的向量|
|half3|GfVec3h|3 个半的向量|
|int3|GfVec3i|3 个整数的向量|
|double4|GfVec4d|4 个双精度的向量|
|float4|GfVec4f|4 个浮点数的向量|
|half4|GfVec4h|4 个半的向量|
|int4|GfVec4i|4 个整数的向量|

## 美元示例

纯 ASCII 文件格式的 USD 文件示例如下。

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## 参考 ＃＃

* [美元介绍](https://openusd.org/release/intro.html)
* [USD API 参考](https://openusd.org/release/apiDocs.html)

