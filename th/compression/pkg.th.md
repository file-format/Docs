{
  "date" : "2021-04-08",
  "keywords" :[ "ไฟล์ pkg", "รูปแบบไฟล์ pkg", "ไฟล์ pkg คืออะไร", "ไฟล์", "ตัวอย่าง pkg", "นามสกุลไฟล์ pkg", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - รูปแบบไฟล์เก็บถาวรที่ขยายได้",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PKG และ API ที่สามารถสร้างและเปิดไฟล์ PKG",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## ไฟล์ PKG คืออะไร??

ไฟล์ที่มีนามสกุล .pkg เป็นไฟล์แพ็คเกจตัวติดตั้งที่ใช้ในการติดตั้งซอฟต์แวร์บน macOS นอกจากคอมพิวเตอร์ Macintosh แล้ว ยังใช้บน iPhone อีกด้วย สามารถใช้แอปพลิเคชันตัวติดตั้งในตัวของ Apple เพื่อติดตั้งเนื้อหาของไฟล์ PKG ไฟล์ PKG คล้ายกับไฟล์ MSI ที่ใช้ในระบบปฏิบัติการ Windows สำหรับการติดตั้งซอฟต์แวร์ ระหว่างการติดตั้ง ไฟล์แพ็คเกจเหล่านี้สามารถบันทึกข้อความที่ทำให้คุณทราบว่ามีการติดตั้งสิ่งพิเศษใดบ้างในแพ็คเกจนี้

## รูปแบบไฟล์ PKG

PKR เป็นไฟล์ไบนารีที่ถูกบีบอัดเพื่อลดขนาดไฟล์โดยรวม ตั้งแต่ OSX 10.5 เป็นต้นมา Apple ได้แนะนำแพ็คเกจแฟลตพร้อมไฟล์ตัวติดตั้งเดียว รูปแบบเหล่านี้แตกต่างจากรูปแบบบรรจุภัณฑ์ก่อนหน้านี้ที่มาเป็นกลุ่มแทนที่จะเป็นไฟล์เดียว แพ็กเกจแบบบันเดิลเหล่านี้มีลำดับชั้นไดเร็กทอรีที่มีโครงสร้างซึ่งจัดเก็บไฟล์ในลักษณะที่อำนวยความสะดวกในการเรียกค้นผ่านไฟล์ดัชนีบางไฟล์ รูปแบบไฟล์ PKG แบบแบนคือไฟล์เก็บถาวร [XAR](/th/compression/xar/) ที่มี:

* Header - กำหนดขนาด เช็คซัม และข้อมูลเวอร์ชัน
* สารบัญ - เอกสาร XML ที่ (และต้อง) เข้ารหัสเป็น UTF-8 และจัดเก็บไว้ในส่วนต้นของไฟล์ ทำให้ง่ายต่อการสแกนผ่านไฟล์เก็บถาวรเพื่อแยกไฟล์แต่ละไฟล์
* กอง - กองข้อมูลที่ไม่มีโครงสร้างอ้างอิงโดย TOC

## อ้างอิง

* [รูปแบบไฟล์แพ็คเกจแบบแบน](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - วิกิพีเดีย](https://en.wikipedia.org/wiki/.pkg)

