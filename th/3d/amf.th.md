{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "ไฟล์ amf", "รูปแบบไฟล์ amf", "รูปแบบไฟล์", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AMF และ API ที่สามารถเปิดและสร้างไฟล์ AMF",
  "title" :"AMF - ไฟล์การผลิตสารเติมแต่ง",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ AMF คืออะไร??
ไฟล์ AMF ประกอบด้วยแนวทางสำหรับคำอธิบายวัตถุเพื่อใช้ในกระบวนการผลิตแบบเพิ่มเนื้อ ประกอบด้วยช่องเปิด<amf> XML tag และลงท้ายด้วย a</amf> ธาตุ. นำหน้าด้วยบรรทัดประกาศ XML ที่ระบุเวอร์ชัน XML และการเข้ารหัสไฟล์ การประกาศสามารถรวมข้อมูลหน่วยการวัด และในกรณีที่ไม่มีข้อมูลดังกล่าว มิลลิเมตรจะถูกใช้เป็นหน่วยเริ่มต้น


## รูปแบบไฟล์ AMF

รูปแบบไฟล์ Additive Manufacturing (**AMF**) กำหนดมาตรฐานเปิดสำหรับคำอธิบายวัตถุเพื่อใช้ในกระบวนการผลิตเพิ่มเติม เช่น การพิมพ์ 3 มิติ โปรแกรม CAD ใช้รูปแบบไฟล์ AMF โดยใช้ข้อมูลต่างๆ เช่น รูปทรงเรขาคณิต สี และวัสดุของวัตถุ AMF แตกต่างจากรูปแบบ STL เนื่องจากรูปแบบด้านข้างไม่รองรับสี วัสดุ โครงตาข่าย และกลุ่มดาว

### องค์ประกอบของไฟล์ AMF

ห้าองค์ประกอบระดับสูงสุดที่กำหนดด้วย<AMF> แท็กมีรายละเอียดดังนี้ ต้องมีองค์ประกอบออบเจกต์เดียวสำหรับไฟล์ AMF ที่ทำงานได้อย่างสมบูรณ์

`<object> ` - องค์ประกอบวัตถุกำหนดปริมาณหรือปริมาตรของวัสดุ ซึ่งแต่ละองค์ประกอบเชื่อมโยงกับรหัสวัสดุสำหรับการพิมพ์ ต้องมีองค์ประกอบวัตถุอย่างน้อยหนึ่งรายการในไฟล์ วัตถุเพิ่มเติมเป็นตัวเลือก

`<material> ` - องค์ประกอบวัสดุที่เป็นตัวเลือกจะกำหนดวัสดุอย่างน้อยหนึ่งรายการสำหรับการพิมพ์ด้วยรหัสวัสดุที่เกี่ยวข้อง หากไม่มีองค์ประกอบวัสดุรวมอยู่ จะถือว่าวัสดุเริ่มต้นรายการเดียว

`<texture> ` - องค์ประกอบพื้นผิวที่เป็นตัวเลือกจะกำหนดรูปภาพหรือพื้นผิวตั้งแต่หนึ่งภาพขึ้นไปสำหรับการแมปสีหรือพื้นผิว โดยแต่ละรายการจะมีรหัสพื้นผิวที่เกี่ยวข้อง

`<constellation> ` - องค์ประกอบกลุ่มดาวที่เป็นทางเลือกจะรวมวัตถุและกลุ่มดาวอื่นๆ ตามลำดับชั้นเป็นรูปแบบสัมพัทธ์สำหรับการพิมพ์

`<metadata> ` - องค์ประกอบข้อมูลเมตาที่เป็นทางเลือกระบุข้อมูลเพิ่มเติมเกี่ยวกับวัตถุและองค์ประกอบที่มีอยู่ในไฟล์

## ตัวอย่าง AMF

ต่อไปนี้คือตัวอย่างไฟล์ AMF ที่สามารถคัดลอกไปยังไฟล์ [text](/th/word-processing/txt/) และบันทึกเป็นไฟล์บีบอัด [zip](/th/compression/zip/) เพื่อเปิด
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
## อ้างอิง

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [ข้อกำหนด AMF ใน ISO](https://www.iso.org/standard/67472.html)

