{
  "date" : "2021-02-26",
  "keywords" :[ "OPUS", "file", "extension", "format", "Audio Coding"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OPUS และ API ที่สามารถสร้างและเปิดไฟล์ OPUS",
  "title" :"บทประพันธ์",
  "linktitle" : "OPUS",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-26"
}

## ไฟล์ OPUS คืออะไร??

Opus เป็นรูปแบบไฟล์เสียงที่สร้างขึ้นโดยมูลนิธิ Xiph.Org และต่อมาได้รับการกำหนดมาตรฐานโดย IETF (Internet Engineering Task Force) ได้รับการพัฒนาขึ้นสำหรับการสตรีมทางอินเทอร์เน็ต, Voice over IP (VOIP), การประชุมผ่านวิดีโอ และการสนทนาในเกมเป็นหลัก ซึ่งเป็นเหตุผลว่าทำไมจึงได้รับการออกแบบมาเพื่อรักษาความหน่วงต่ำไว้ในขณะที่ยังคงรักษาการสื่อสารแบบโต้ตอบตามเวลาจริง การรักษาคุณภาพเสียงของไฟล์ Opus การทดสอบการฟังแบบตาบอดหลายครั้งได้กำหนดให้ Opus เป็นรูปแบบเสียงคุณภาพสูงกว่ารูปแบบเสียงอื่น ๆ ที่บิตเรตใด ๆ

## ข้อมูลจำเพาะรูปแบบไฟล์ OPUS

รูปแบบ Opus ใช้ทั้งตัวแปลงสัญญาณ SILK (ใช้โดย Skype) และ Xiph.Org และรองรับอัตราบิตผันแปรตั้งแต่ 6 kb/s ถึง 510 kb/s ส่วนขยายบทประพันธ์ใช้อัลกอริทึม SILK ที่ใช้ LPC ที่เน้นเสียงพูดและอัลกอริทึม CELT ที่ใช้ MDCT ที่มีความหน่วงแฝงต่ำ บางครั้งสลับระหว่างทั้งสองอย่างหรือบางครั้งโดยการรวมอัลกอริทึมทั้งสองเข้าด้วยกันเพื่อให้มีประสิทธิภาพสูงสุด ไฟล์ในรูปแบบ Opus มีนามสกุล .opus ซึ่งแตกต่างจากรูปแบบไฟล์ Vorbis, Codebooks ขนาดใหญ่ไม่จำเป็นต้องใช้โดย Opus สำหรับแต่ละไฟล์ นั่นคือเหตุผลว่าทำไมรูปแบบนี้จึงค่อนข้างมีประสิทธิภาพ

## อ้างอิง ##

* [OPUS - โดย Wikipedia](https://en.wikipedia.org/wiki/Opus_(audio_format))
