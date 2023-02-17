{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ IFO - ไฟล์ IFO คืออะไร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ IFO และ API ที่สามารถสร้างและเปิดไฟล์ IFO",
  "linktitle" : "IFO",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## ไฟล์ IFO คืออะไร??

ไฟล์ .ifo คือไฟล์ข้อมูลที่เป็นส่วนหนึ่งของข้อมูลจำเพาะของดีวีดี IFO ย่อมาจากคำว่า Information ไฟล์ IFO ให้ข้อมูลเกี่ยวกับเนื้อหาของแผ่นดิสก์ไปยังเครื่องเล่นดีวีดี เช่น เกี่ยวกับไฟล์วิดีโอ เมนู คำบรรยาย และคุณสมบัติพิเศษใดๆ ที่ดีวีดีอาจมี นี่คือไฟล์ที่บอกเครื่องเล่นดีวีดีว่าจะแสดงอะไรเมื่อเมนูปรากฏขึ้น จุดเริ่มต้นของตอนต่างๆ ในดีวีดี และตำแหน่งและเวลาของไฟล์วิดีโอและไฟล์เสียงในดีวีดี VLAN VLC Player สามารถเปิดไฟล์ IFO

ไฟล์ IFO ถูกบันทึกด้วยนามสกุล **.ifo**

## รูปแบบไฟล์ IFO - ข้อมูลเพิ่มเติม

ไฟล์ IFO จะถูกบันทึกเป็นไฟล์ข้อความและสามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad++, Notepad และ Apple TextEdit ส่วนหัวในไฟล์ IFO จะบอกเครื่องเล่นดีวีดีเกี่ยวกับหน้าจอเริ่มต้น ตำแหน่งของแต่ละแทร็กวิดีโอบนดิสก์ ตำแหน่งแทร็กเสียง และข้อมูลอื่น ๆ ที่เกี่ยวข้อง

ไฟล์ IFO อาจสร้างความเสียหายได้หากแผ่นดีวีดีมีรอยขีดข่วน นั่นคือเหตุผลที่ไฟล์ BUP ได้รับการสร้างเป็นข้อมูลสำรองของไฟล์ IFO ในกรณีที่ไม่สามารถอ่านไฟล์ IFO ได้ ไฟล์ BUP จะถูกอ่านแทน ไฟล์เหล่านี้อยู่ร่วมกับไฟล์ [VOB](https://docs.fileformat.com/video/vob/) ที่มีดัชนีของเนื้อหาในแผ่นดิสก์

## อ้างอิง

* [VobSub](https://www.videohelp.com/software/VobSub)
* [ไฟล์วิดีโอดีวีดี-วิดีโอภายใน](https://en.wikibooks.org/wiki/Inside_DVD-Video/IFO_Files)
