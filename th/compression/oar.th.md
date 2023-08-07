{
  "date" : "2021-04-08",
  "keywords" :[ "ไฟล์ oar", "รูปแบบไฟล์ oar", "ไฟล์ oar คืออะไร", "ไฟล์", "ตัวอย่าง oar", "นามสกุลไฟล์ oar","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - รูปแบบไฟล์เก็บถาวร OpenSimulator",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OAR และ API ที่สามารถสร้างและเปิดไฟล์ OAR",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## ไฟล์ OAR คืออะไร??

ไฟล์ที่มีนามสกุล .oar คือไฟล์เก็บถาวรที่ใช้โดยแอปพลิเคชัน OpenSimulator ซึ่งเป็นเซิร์ฟเวอร์แอปพลิเคชัน 3 มิติแบบโอเพ่นซอร์สสำหรับสร้างสภาพแวดล้อมเสมือนจริงที่เข้าถึงได้สำหรับผู้ใช้หลายคนผ่านเครือข่าย รูปแบบไฟล์ OAR ให้ข้อมูลสินทรัพย์ที่จำเป็นสำหรับการโหลดภูมิประเทศ พื้นผิววัตถุ และสินค้าคงคลังในระบบอื่นอย่างสมบูรณ์ OpenSimulator ยังมีไฮเปอร์กริดเสริมที่ช่วยให้ผู้ใช้สามารถเยี่ยมชมการติดตั้ง OpenSimulator อื่น ๆ ทั่วทั้งเว็บ ไฟล์ OAR มีแอปพลิเคชันประเภท MIME อินเทอร์เน็ต/oar และมีไฟล์เก็บถาวรตั้งแต่หนึ่งไฟล์ขึ้นไป


## รูปแบบไฟล์ OAR

OAR เป็นไฟล์ไบนารีที่เก็บในรูปแบบไฟล์เก็บถาวรที่บีบอัด รูปแบบไฟล์ OAR เวอร์ชันล่าสุดคือ [เวอร์ชัน 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) ซึ่งมีการเปลี่ยนแปลงครั้งใหญ่จาก [เวอร์ชัน 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). เวอร์ชันล่าสุดรองรับการจัดเก็บหลายภูมิภาคใน OAR เดียว และไม่รองรับเวอร์ชันเก่าของ OpenSimulator ก่อน 0.7.5 ไฟล์ OAR เป็นไฟล์ gzip tar (tar.gz) ในรูปแบบ unix tar ดั้งเดิม (ไม่ใช่ USTAR)

## ตัวอย่างภูมิภาค OAR
ไฟล์ AOR สามารถมีหลายภูมิภาค โครงสร้างของไฟล์เก็บถาวรมีดังนี้ (ตัวอย่างนี้มี 4 ภูมิภาค):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## เอกสาร OAR.xml

ไฟล์ควบคุมการเก็บถาวรมีหมายเลขเวอร์ชันหลักสำหรับกำหนดความเข้ากันได้กับการเปลี่ยนแปลงรูปแบบในอนาคต การมีอยู่ของสินทรัพย์ในรูปแบบ OAR จะระบุโดยองค์ประกอบบูลีน<assets_included> . ข้อมูลเกี่ยวกับภูมิภาคที่รวมอยู่ในรายการที่มีอยู่ในไฟล์ควบคุม ตัวอย่างของ Archive.xml มีดังต่อไปนี้

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## อ้างอิง

* [รูปแบบ OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

