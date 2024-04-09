{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ svgz", "รูปแบบไฟล์ svgz", "ไฟล์ svgz คืออะไร", "ไฟล์", "ตัวอย่าง svgz", "นามสกุลไฟล์ svgz","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ SVGZ - Metafile ที่บีบอัดของ Windows",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EMZ และ API ที่สามารถสร้างและเปิดไฟล์ SVGZ",
  "linktitle" : "SVGZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## ไฟล์ SVGZ คืออะไร??

ไฟล์ที่มีนามสกุล .svgz คือไฟล์ Scalable Vector Graphics (.SVG) เวอร์ชันบีบอัด มันถูกบีบอัดด้วยการบีบอัด gzip และมีข้อมูลในรูปแบบ [XML](/th/web/xml/) ไฟล์ SVGZ รองรับความโปร่งใส การไล่ระดับสี ภาพเคลื่อนไหว และตัวกรอง ไฟล์ SVGZ มีขนาดเล็กกว่าเมื่อเทียบกับไฟล์ SVG เริ่มต้น และขนาดไฟล์ที่ลดลงนี้จะช่วยถ่ายโอนไฟล์กราฟิกออนไลน์ นักออกแบบกราฟิกสร้างไฟล์ SVGZ โดยใช้เครื่องมือต่างๆ เช่น Adobe Illustrator, Corel PaintShop Pro และอื่นๆ อย่างไรก็ตาม สามารถสร้างไฟล์ SVGZ ได้โดยการเปิดใช้งาน [การบีบอัด GZip](/th/compression/gz/) ในเซิร์ฟเวอร์ Apache ขณะที่ส่งข้อมูลภาพออกไป

## รูปแบบไฟล์ SVGZ

SVGZ ซึ่งถูกบีบอัด [SVG](/th/page-description-language/svg/) อิงตามรูปแบบ gzip บีบอัดแบบเปิดที่ลดขนาดของเอกสาร SVG ไฟล์เก็บถาวรแบบบีบอัดนี้ประกอบด้วยเอกสาร SVG แบบข้อความล้วนซึ่งอยู่บนพื้นฐานของรูปแบบไฟล์ XML (/th/web/xml/) เท่านั้น ไฟล์ SVGZ สามารถเปิดได้โดยโปรแกรมดู/แอปพลิเคชันที่เป็นไปตามข้อกำหนด SVG 1.1 ไฟล์ SVGZ มีขนาดเล็กกว่าไฟล์ SVG ดั้งเดิม 20-50%

## อ้างอิง

* [SVGZ โดย Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics#Compression)

