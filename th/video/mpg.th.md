{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ MPG",
  "keywords" :[ "MPG", "ไฟล์", "นามสกุล", "รูปแบบ", "รูปแบบวิดีโอ", "รูปแบบไฟล์ mpg คืออะไร", "รูปแบบไฟล์ mpg", "เครื่องเล่นไฟล์ mpg", "การบีบอัด mpeg", "วิดีโอ ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MPG และ API ที่สามารถสร้างและแสดงวิธีเปิดไฟล์ MPG",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## รูปแบบไฟล์ MPG คืออะไร? ##

ไฟล์ที่มีนามสกุล .mpg อยู่ในกลุ่มของนามสกุลไฟล์สำหรับการบีบอัดเสียงและวิดีโอ MPEG-1 หรือ MPEG-2 วิดีโอ MPEG-1 ตอนที่ 2 หาดูได้ยาก และส่วนขยายนี้ (รูปแบบไฟล์ MPG) โดยทั่วไปจะชี้ไปที่สตรีมโปรแกรม MPEG ซึ่งกำหนดไว้ใน MPEG-1 และ MPEG-2 หรือสตรีมการขนส่ง MPEG ซึ่งกำหนดไว้ใน MPEG-2 . นอกจากนี้ยังมีส่วนขยายอื่นๆ เช่น .m2ts ที่ระบุคอนเทนเนอร์ที่ถูกต้อง ในกรณีนี้คือ MPEG-2 TS แต่สิ่งนี้มีความเกี่ยวข้องเพียงเล็กน้อยกับสื่อ MPEG-1 [.mp3](https://docs.fileformat.com/audio/mp3/) เป็นส่วนขยายทั่วไปสำหรับไฟล์ที่มีเสียง MP3 ไฟล์ MP3 เป็นสตรีมเสียงดิบทั่วไป วิธีดั้งเดิมในการแท็กไฟล์ MP3 คือการเขียนข้อมูลสตรีมไปยังส่วน "ขยะ" ของแต่ละเฟรม ซึ่งจะบันทึกข้อมูลมีเดีย แต่ **เครื่องเล่นไฟล์ mpg** จะละทิ้ง นี่เป็นเทคนิคที่คล้ายกันที่ใช้ในการติดแท็กไฟล์ AAC แต่ปัจจุบันรองรับน้อยลง

## การบีบอัด MPEG ##

ชื่อ MPEG ย่อมาจาก Moving Pictures Experts Group MPEG เป็นเครื่องมือสำหรับการบีบอัดวิดีโอ ซึ่งเกี่ยวข้องกับการบีบอัดภาพและเสียง รวมถึงการซิงโครไนซ์ของทั้งสอง
ปัจจุบันมีมาตรฐาน MPEG หลายมาตรฐาน

- เสนอ MPEG-1 สำหรับอัตราข้อมูลระดับกลาง ตามลำดับที่ 1.5 Mbit/วินาที
- เสนอ MPEG-2 สำหรับอัตราข้อมูลสูงอย่างน้อย 10 Mbit/วินาที
- มีการเสนอ MPEG-3 สำหรับการบีบอัด HDTV แต่พบว่าซ้ำซ้อนและถูกรวมเข้ากับ MPEG-2
- MPEG-4 ถูกเสนอสำหรับอัตราข้อมูลที่ต่ำมากน้อยกว่า 64 Kbit/วินาที


## สตรีมโปรแกรมรูปแบบไฟล์ MPG ##

สตรีมโปรแกรมเป็นคอนเทนเนอร์สำหรับการมัลติเพล็กซ์เสียงดิจิตอล วิดีโอ และอื่นๆ รูปแบบ Program Stream ระบุไว้ในส่วนที่ 1 ของ MPEG-1 (ISO/IEC 11172-1) และส่วนที่ 1 ของ MPEG-2, Systems (ISO/IEC standard 13818-1/ITU-T H.222.0) MPEG-2 Program Stream เป็นแบบแอนะล็อกและคล้ายกับ ISO/IEC 11172 Systems layer และรองรับฟอร์เวิร์ด

### รายละเอียดการเข้ารหัส ###

นี่คือรายละเอียดการเข้ารหัสของรูปแบบส่วนหัว MPEG-2 Program Stream บางส่วน:

| ชื่อ | จำนวนบิต | คำอธิบาย |
---|---|---|
| ซิงค์ไบต์ | 32 | 0x000001BA |
| บิตเครื่องหมาย | 2 | 01b สำหรับเวอร์ชัน MPEG-2 บิตเครื่องหมายสำหรับเวอร์ชัน MPEG-1 คือ 4 บิตที่มีค่า 0010b |
| นาฬิการะบบ [32..30] | 3 | การอ้างอิงนาฬิการะบบ (SCR) บิต 32 ถึง 30 |
| บิตเครื่องหมาย | 1 | ตั้งค่า 1 บิตเสมอ |
| นาฬิการะบบ [29..15] | 15 | บิตนาฬิการะบบ 29 ถึง 15 |
| บิตเครื่องหมาย | 1 | ตั้งค่า 1 บิตเสมอ |
| นาฬิการะบบ [14..0] | 15 | บิตนาฬิการะบบ 14 ถึง 0 |
| บิตเครื่องหมาย | 1 | ตั้งค่า 1 บิตเสมอ |
| ส่วนขยาย SCR | 9 | |
| บิตเครื่องหมาย | 1 | ตั้งค่า 1 บิตเสมอ |
| อัตราบิต | 22 | ในหน่วย 50 ไบต์ต่อวินาที |
| บิตเครื่องหมาย | 2 | ตั้งค่า 11 บิตเสมอ |
| สงวน | 5 | สงวนไว้สำหรับใช้ในอนาคต |
| ความยาวบรรจุ | 3 | |
| การบรรจุไบต์ | 8 * ความยาวบรรจุ | |
| ส่วนหัวของระบบ (ไม่บังคับ) | 0 หรือมากกว่า | ถ้ารหัสเริ่มต้นของส่วนหัวของระบบดังต่อไปนี้: 0x000001BB |

ตารางต่อไปนี้แสดงรูปแบบส่วนหัวของระบบบางส่วน:

| ชื่อ | จำนวนไบต์ | คำอธิบาย |
---|---|---|
| ซิงค์ไบต์ | 4 | 0x000001BB |
| ความยาวส่วนหัว | 2 | |
| อัตราขอบเขตและบิตเครื่องหมาย | 3 | |
| ขอบเขตเสียงและแฟล็ก | 1 | |
| ค่าสถานะ บิตเครื่องหมาย และขอบเขตวิดีโอ | 1 | |
| ข้อ จำกัด อัตราแพ็คเก็ตและไบต์ที่สงวนไว้ | 1 | |


## อ้างอิง ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)


