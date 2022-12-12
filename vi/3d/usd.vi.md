{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd file", "usd file format", "file format", "file","extension", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Định dạng mô tả cảnh phổ quát",
  "description":"Tìm hiểu về định dạng tệp USD và các API có thể mở và tạo tệp USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Tệp USD là gì?

Một tệp có phần mở rộng .usd là một định dạng tệp Mô tả cảnh phổ biến mã hóa dữ liệu nhằm mục đích trao đổi và bổ sung dữ liệu giữa các ứng dụng tạo nội dung kỹ thuật số. Được phát triển bởi Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) cung cấp khả năng trao đổi các nội dung cơ bản (chẳng hạn như mô hình) hoặc hoạt ảnh.

## Định dạng tệp USD

Các tệp USD có thể có định dạng nhị phân (còn được gọi là tệp Crate) hoặc tệp được hỗ trợ bởi ASCII. Cả hai định dạng tệp này đều có thể hoán đổi cho nhau khi các tham chiếu có thể được liên kết với nội dung .usd mà không cần thay đổi nguồn. Định dạng tệp USD bao gồm một tập hợp các thư viện C++ với các liên kết Python để tạo tập lệnh. Nó cho phép lắp ráp và tổ chức bất kỳ số lượng thành phần cảnh 3D nào, chẳng hạn như bộ ảo, cảnh và ảnh để truyền chúng từ ứng dụng này sang ứng dụng khác.

### Loại dữ liệu USD

Các loại dữ liệu cơ bản được định dạng tệp USD hỗ trợ được liệt kê trong bảng sau.

|Mã thông báo loại giá trị |Loại C++ |Mô tả|
---|---|---|
|bool|bool||
|uchar|uint8_t|số nguyên không dấu 8 bit|
|int|int32_t|Số nguyên có dấu 32 bit|
|uint|uint32_t|Số nguyên không dấu 32 bit|
|int64|int64_t|Số nguyên có dấu 64 bit|
|uint64|uint64_t|số nguyên không dấu 64 bit|
|half|GfHalf|Dấu chấm động 16 bit|
|float|float|dấu phẩy động 32 bit|
|kép|kép|dấu phẩy động 64 bit|
|timecode|SdfTimeCode|double thể hiện thời gian có thể phân giải|
|chuỗi|std::chuỗi|chuỗi stl|
|token|TfToken|chuỗi nội bộ với so sánh và băm nhanh|
|nội dung|SdfAssetPath|biểu thị đường dẫn có thể phân giải đến nội dung khác|
|matrix2d|GfMatrix2d|ma trận đôi 2x2|
|matrix3d|GfMatrix3d|ma trận đôi 3x3|
|matrix4d|GfMatrix4d|ma trận đôi 4x4|
|quatd|GfQuatd|quaternion độ chính xác kép|
|quatf|GfQuatf|quaternion độ chính xác đơn|
|quath|GfQuath|quaternion nửa chính xác|
|double2|GfVec2d|vectơ 2 nhân đôi|
|float2|GfVec2f|vectơ của 2 số float|
|half2|GfVec2h|vectơ 2 nửa|
|int2|GfVec2i|vectơ của 2 số nguyên|
|double3|GfVec3d|vectơ 3 nhân đôi|
|float3|GfVec3f|vectơ 3 số float|
|half3|GfVec3h|vectơ 3 nửa|
|int3|GfVec3i|vectơ 3 số nguyên|
|double4|GfVec4d|vectơ 4 nhân đôi|
|float4|GfVec4f|vectơ 4 số float|
|half4|GfVec4h|vectơ 4 nửa|
|int4|GfVec4i|vectơ 4 số nguyên|

## Ví dụ USD

Một ví dụ về tệp USD ở định dạng tệp ASCII đơn giản như sau.

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
## Người giới thiệu ##

* [Giới thiệu về USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Tham chiếu API USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

