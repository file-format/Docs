{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "ไฟล์ usd", "รูปแบบไฟล์ usd", "รูปแบบไฟล์", "ไฟล์", "นามสกุล", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - รูปแบบคำอธิบายฉากสากล",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ USD และ API ที่สามารถเปิดและสร้างไฟล์ USD",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## ไฟล์ USD คืออะไร??

ไฟล์ที่มีนามสกุล .usd เป็นรูปแบบไฟล์ Universal Scene Description ที่เข้ารหัสข้อมูลเพื่อวัตถุประสงค์ในการแลกเปลี่ยนข้อมูลและเสริมระหว่างแอปพลิเคชันสร้างเนื้อหาดิจิทัล [USD](https://openusd.org/release/intro.html) พัฒนาโดย Pixar ให้ความสามารถในการแลกเปลี่ยนองค์ประกอบองค์ประกอบ (เช่น โมเดล) หรือภาพเคลื่อนไหว

## รูปแบบไฟล์ USD

ไฟล์ USD สามารถมีรูปแบบไบนารี (หรือที่เรียกว่าไฟล์ลัง) หรือไฟล์ที่สนับสนุน ASCII รูปแบบไฟล์ทั้งสองนี้สามารถใช้แทนกันได้ โดยการอ้างอิงสามารถเชื่อมโยงกับสินทรัพย์ .usd โดยไม่ต้องเปลี่ยนแหล่งที่มา รูปแบบไฟล์ USD ประกอบด้วยชุดของไลบรารี C++ ที่มีการเชื่อมโยง Python สำหรับการเขียนสคริปต์ ช่วยให้สามารถประกอบและจัดระเบียบองค์ประกอบฉาก 3 มิติจำนวนเท่าใดก็ได้ เช่น ฉากเสมือนจริง ฉาก และช็อต เพื่อส่งผ่านจากแอปพลิเคชันหนึ่งไปยังอีกแอปพลิเคชันหนึ่ง

### ประเภทข้อมูล USD

ประเภทข้อมูลพื้นฐานที่สนับสนุนโดยรูปแบบไฟล์ USD แสดงอยู่ในตารางต่อไปนี้

|โทเค็นประเภทค่า |ประเภท C++ |คำอธิบาย|
---|---|---|
|บูล|บูล||
|uchar|uint8_t|จำนวนเต็ม 8 บิตที่ไม่ได้ลงชื่อ|
|int|int32_t|จำนวนเต็ม 32 บิต|
|uint|uint32_t|จำนวนเต็ม 32 บิตที่ไม่ได้ลงชื่อ|
|int64|int64_t|จำนวนเต็ม 64 บิต|
|uint64|uint64_t|จำนวนเต็ม 64 บิตที่ไม่ได้ลงชื่อ|
|half|GfHalf|จุดลอยตัว 16 บิต|
|ลอย|ลอย|จุดลอยตัว 32 บิต|
|double|double|จุดลอยตัว 64 บิต|
|รหัสเวลา|SdfTimeCode|สองเท่าแทนเวลาที่สามารถแก้ไขได้|
|string|std::string|stl สตริง|
|token|TfToken|interned string พร้อมการเปรียบเทียบอย่างรวดเร็วและการแฮช|
|asset|SdfAssetPath|แสดงถึงเส้นทางที่แก้ไขได้ไปยังเนื้อหาอื่น|
|matrix2d|GfMatrix2d|2x2 เมทริกซ์คู่|
|matrix3d|GfMatrix3d|3x3 เมทริกซ์คู่|
|matrix4d|GfMatrix4d|4x4 เมทริกซ์คู่|
|quatd|GfQuatd|ควอเทอร์เนียนที่มีความแม่นยำสองเท่า|
|quatf|GfQuatf|ควอเทอร์เนียนความแม่นยำเดียว|
|quath|GfQuath|ควอเทอร์เนียนครึ่งความแม่นยำ|
|double2|GfVec2d|เวกเตอร์ของ 2 สองเท่า|
|float2|GfVec2f|เวกเตอร์ของ 2 float|
|half2|GfVec2h|เวกเตอร์ของ 2 ครึ่ง|
|int2|GfVec2i|เวกเตอร์ของ 2 ints|
|double3|GfVec3d|เวกเตอร์ของ 3 คู่|
|float3|GfVec3f|เวกเตอร์ของ 3 float|
|half3|GfVec3h|เวกเตอร์ของ 3 ครึ่ง|
|int3|GfVec3i|เวกเตอร์ของ 3 ints|
|double4|GfVec4d|เวกเตอร์ของ 4 คู่|
|float4|GfVec4f|เวกเตอร์ของ 4 float|
|half4|GfVec4h|เวกเตอร์ของ 4 ครึ่ง|
|int4|GfVec4i|เวกเตอร์ของ 4 ints|

## ตัวอย่าง USD

ตัวอย่างของไฟล์ USD ในรูปแบบไฟล์ ASCII ธรรมดามีดังต่อไปนี้

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
## อ้างอิง ##

* [ความรู้เบื้องต้นเกี่ยวกับ USD](https://openusd.org/release/intro.html)
* [ข้อมูลอ้างอิง USD API](https://openusd.org/release/apiDocs.html)

