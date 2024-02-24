{
  "date" : "2023-11-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ RBZ - ไฟล์ RBZ คืออะไร และวิธีการเปิดมัน",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RBZ และ API ที่สามารถสร้างและเปิดไฟล์ RBZ",
  "linktitle" : "RBZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-rb-thz"
}
},
  "lastmod" : "2023-11-23"
}

## ไฟล์ RBZ คืออะไร??

ไฟล์ RBZ เป็นไฟล์ปลั๊กอินที่ใช้โดยโปรแกรมสร้างแบบจำลอง **Trimble SketchUp** สำหรับการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) เป็นไฟล์ ZIP ที่ถูกบีบอัดซึ่งมีสคริปต์ Ruby (ไฟล์ .rb) หนึ่งไฟล์ขึ้นไปอยู่ข้างใน นั่นคือสาเหตุที่ไฟล์ประเภทนี้เป็น RBZ (RB + Z) ไฟล์ RBZ นั้นง่ายต่อการแจกจ่ายและไม่ได้อยู่บนเครือข่ายเนื่องจากขนาดไฟล์ที่เล็กอันเป็นผลมาจากการบีบอัด

## รูปแบบไฟล์ RBZ - ข้อมูลเพิ่มเติม

ไฟล์ RBZ เป็นไฟล์ ZIP ที่ถูกบีบอัดซึ่งมีไฟล์สคริปต์ Ruby มันถูกบีบอัดด้วยวิธีการบีบอัดที่ใช้บ่อยที่สุด **DEFLATE** ซึ่งอธิบายไว้ใน IETF **RFC 1951**

## เปิดไฟล์ .RBZ ได้อย่างไร

คุณสามารถเปิดไฟล์ RBZ ด้วย Trimble SketchUp บน Windows และ macOS

นอกจากนี้ เนื่องจากไฟล์ RBZ เป็นไฟล์ ZIP ที่ถูกบีบอัด คุณจึงสามารถแตกไฟล์เหล่านี้ด้วยโปรแกรมอรรถประโยชน์การแตกไฟล์ ZIP มาตรฐานโดยเปลี่ยนชื่อนามสกุลจาก .rbz เป็น .zip

## เกี่ยวกับ Sketch Up

SketchUp is a 3D modeling software widely used for architectural design, interior design, film and video game design, and other related fields. It was originally developed by @Last Software, which was later acquired by Google in 2006. Google พัฒนาและปรับปรุง SketchUp อย่างต่อเนื่องก่อนที่จะขายให้กับ Trimble Inc. ในปี 2012

## ผู้ตัดสิน

 * [แปลงไฟล์ ZIP เป็นรูปแบบไฟล์ RBZ](https://forums.sketchup.com/t/convert-zip-to-rbz/109528)
 * [Sketchup](https://www.sketchup.com/)
