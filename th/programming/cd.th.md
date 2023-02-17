{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "ไฟล์ cd คืออะไร", "วิธีเปิดไฟล์ cd", "นามสกุล", "ไฟล์", "ไฟล์ cd","รูปแบบไฟล์ cd", "นามสกุลไฟล์ cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ซีดี - ไฟล์ไดอะแกรมคลาส Visual Studio",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ซีดีและ API ที่สามารถสร้างและเปิดไฟล์ซีดี",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## ไฟล์ซีดีคืออะไร?

ไฟล์ที่มีนามสกุล .cd คือไฟล์ไดอะแกรมคลาส Visual Studio ที่ให้ข้อมูลเกี่ยวกับโครงสร้างและความสัมพันธ์ระหว่างคลาสทั้งหมดในโซลูชันปัจจุบัน โซลูชัน Visual Studio (แสดงโดย [.sln](/th/programming/sln/)) อาจมีหนึ่งโปรเจ็กต์หรือมากกว่า แต่ละโปรเจ็กต์มีหลายคลาสที่แตกต่างกัน สามารถสร้างไฟล์ไดอะแกรมคลาสได้โดยการคลิกขวาที่โปรเจ็กต์และเลือกตัวเลือกคลาสไดอะแกรม

## รูปแบบไฟล์คลาสไดอะแกรม (.cd) - ข้อมูลเพิ่มเติม

ไฟล์ไดอะแกรมคลาสถูกบันทึกในรูปแบบไฟล์ XML มาตรฐานที่แสดงถึงคลาสในโครงการเป็นโหนด XML หากไม่มี Visual Studio ไฟล์ไดอะแกรมคลาสเหล่านี้สามารถเปิดได้ในโปรแกรมแอปพลิเคชันใดๆ ที่รองรับการเปิดไฟล์ XML

### วิธีเพิ่มคลาสไดอะแกรมในโครงการ Visual Studio

ใน Visual Studio ให้เปิดโซลูชัน/โครงการที่คุณต้องการเพิ่มคลาสไดอะแกรม จากนั้น คลิกขวาที่โหนดโครงการ จากนั้นเลือก เพิ่ม > รายการใหม่ หรือกด Ctrl+Shift+A

* กล่องโต้ตอบเพิ่มรายการใหม่จะเปิดขึ้น

* ขยาย รายการทั่วไป > ทั่วไป แล้วเลือก ไดอะแกรมคลาส จากรายการเทมเพลต สำหรับโปรเจ็กต์ Visual C++ ให้ดูที่หมวดหมู่ยูทิลิตี้เพื่อค้นหาเทมเพลตไดอะแกรมคลาส

### ส่งออกคลาสไดอะแกรม (ซีดี) เป็นรูปภาพ

Visual Studio อนุญาตให้แปลง/ส่งออกคลาสไดอะแกรมเป็นรูปภาพ เช่น [PNG](/th/image/png/), [JPEG](/th/image/jpeg/) และ [BMP](/th/image/bmp/) ไฟล์ไดอะแกรมคลาสที่ส่งออกเหล่านี้สามารถใช้สำหรับวัตถุประสงค์ในการเก็บบันทึกชุดข้อมูลทางเทคนิค (TDP) และเอกสารประกอบ ในการแปลงคลาสไดอะแกรมเป็นรูปภาพ สามารถใช้ขั้นตอนต่อไปนี้จากภายใน Microsoft Visual Studio

1. เปิดไฟล์ไดอะแกรมคลาส (.cd) ของคุณ
1. จากเมนูคลาสไดอะแกรมหรือเมนูทางลัดพื้นผิวไดอะแกรม ให้เลือก ส่งออกไดอะแกรมเป็นรูปภาพ
1. เลือกไดอะแกรม
1. เลือกรูปแบบที่คุณต้องการ
1. เลือก ส่งออก เพื่อเสร็จสิ้นการส่งออก

## อ้างอิง

* [คลาสการออกแบบใน Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)
