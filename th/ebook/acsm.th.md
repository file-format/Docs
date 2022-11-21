{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extension", "format", "eBook", "file", "Adobe Digital Editions" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ACSM โดย Adobe และ API ที่สามารถสร้างและเปิดไฟล์ ACSM",
  "title" :"ACSM - รูปแบบไฟล์ข้อความ Adobe Content Server",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## ไฟล์ ACSM คืออะไร??

ไฟล์ที่มีนามสกุล .acsm เรียกว่าไฟล์ Adobe Content Server Message ไฟล์เหล่านี้ถูกใช้โดย **Adobe Digital Editions** เพื่อเปิดใช้งานและดาวน์โหลดเนื้อหาที่มีการป้องกันด้วย Adobe DRM อันที่จริง ไฟล์ ACSM ไม่ใช่ไฟล์ eBook; ไม่สามารถเปิดอ่านได้เหมือน eBook อื่นๆ (เช่น PDF); ประกอบด้วยข้อมูลเพื่อเปิดใช้งานและดาวน์โหลด ebook เท่านั้น หมายความว่าไฟล์ ACSM ประกอบด้วยข้อมูลที่สื่อสารกับเซิร์ฟเวอร์ของ Adobe เท่านั้น ผู้ใช้ Digital Editions สามารถดูไฟล์ ACSM ได้หากจะดาวน์โหลด eBook แต่การดาวน์โหลดจะหยุดลงไม่ว่าด้วยเหตุผลใดก็ตาม ผู้ใช้สามารถดำเนินการดาวน์โหลดต่อได้โดยดับเบิลคลิกที่ไฟล์ .acsm

## ไฟล์ ACSM ทำงานอย่างไร

เนื่องจาก Adobe Content Server มีหน้าที่รับผิดชอบในการปกป้อง eBooks และเนื้อหาดิจิทัลอื่นๆ หลังจากซื้อแล้ว เนื้อหาจะเชื่อมโยงกับ Adobe ID ของผู้ซื้อโดยอัตโนมัติ ID เป็นส่วนตัวและไม่สามารถโอนให้ผู้อื่นได้ ผู้ใช้ต้องตั้งค่าก่อนที่จะซื้อเอกสารใดๆ ที่มีการป้องกันการคัดลอกของ Adobe ลูกค้าไม่สามารถเข้าถึงเอกสารที่มีการป้องกันการคัดลอกโดยไม่ส่ง Adobe ID ไปยังแอปพลิเคชันเซิร์ฟเวอร์ Adobe ที่ทำงานอยู่เบื้องหลัง

เมื่อลูกค้าทำการซื้อ ACSM จะเป็นไฟล์เดียวที่พวกเขาสามารถดาวน์โหลดได้ในตอนแรก ลูกค้าต้องติดตั้งซอฟต์แวร์ Adobe Digital Editions ในระบบของตนและเชื่อมโยงกับ Adobe ID ของตนเพื่อเปิดไฟล์ ACSM Adobe Digital Editions จะตรวจสอบ ID สำหรับการอนุญาตให้แปลงไฟล์ ACSM หากตรวจสอบสิทธิ์แล้ว ผู้ใช้จะดาวน์โหลด eBook ได้ในรูปแบบ [EPUB](/th/ebook/epub/) หรือ [PDF](/th/pdf/) Adobe Digital Editions ยังใช้ไฟล์ ACSM เพื่อจดจำไดเร็กทอรีการดาวน์โหลด

## อ้างอิง

* [Adobe Content Server - โดย Wikipedia](https://en.wikipedia.org/wiki/Adobe_Content_Server)


