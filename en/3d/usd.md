{
  "date" : "2021-02-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "USD - Universal Scene Description Format",
  "description":"Learn about USD file format and APIs that can open and create USD files.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2021-02-01"
}

## What is a USD file?

A file with .usd extension is a Universal Scene Description file format that encodes data for the purpose of data interchanging and augmenting between digital content creation applications. Developed by Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) provides the ability to interchange elemental assets (such as models) or animation. USD enables assembly and organization of any number of 3D scene elements such as virtual sets, scenes, and shots to transmit them from application to application. Some of the applciations that can be open USD files include [Pixar Animation Studios USD](https://github.com/PixarAnimationStudios/USD) and NVIDIA Omniverse.

## USD File Format

USD files can have binary format (also known as Crate files) or ASCII-backed files. Both these file formats are interchangeable where the references can be linked to .usd assets without changing the sources. USD consists of a set of C++ libraries with Python bindings for scripting.

### USD Data Types

The fundamental data types supported by the USD file format are listed in the following table.

|Value type token	|C++ type	|Description|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit unsigned integer|
|int|int32_t|32 bit signed integer|
|uint|uint32_t|32 bit unsigned integer|
|int64|int64_t|64 bit signed integer|
|uint64|uint64_t|64 bit unsigned integer|
|half|GfHalf|16 bit floating point|
|float|float|32 bit floating point|
|double|double|64 bit floating point|
|timecode|SdfTimeCode|double representing a resolvable time|
|string|std::string|stl string|
|token|TfToken|interned string with fast comparison and hashing|
|asset|SdfAssetPath|represents a resolvable path to another asset|
|matrix2d|GfMatrix2d|2x2 matrix of doubles|
|matrix3d|GfMatrix3d|3x3 matrix of doubles|
|matrix4d|GfMatrix4d|4x4 matrix of doubles|
|quatd|GfQuatd|double-precision quaternion|
|quatf|GfQuatf|single-precision quaternion|
|quath|GfQuath|half-precision quaternion|
|double2|GfVec2d|vector of 2 doubles|
|float2|GfVec2f|vector of 2 floats|
|half2|GfVec2h|vector of 2 half's|
|int2|GfVec2i|vector of 2 ints|
|double3|GfVec3d|vector of 3 doubles|
|float3|GfVec3f|vector of 3 floats|
|half3|GfVec3h|vector of 3 half's|
|int3|GfVec3i|vector of 3 ints|
|double4|GfVec4d|vector of 4 doubles|
|float4|GfVec4f|vector of 4 floats|
|half4|GfVec4h|vector of 4 half's|
|int4|GfVec4i|vector of 4 ints|

## USD Example

An example of a USD file in plain ASCII file format is as following.

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
## References ##

* [Introduction to USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD API Reference](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)
