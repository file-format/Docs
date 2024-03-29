{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "ไฟล์", "ส่วนขยาย", "รูปแบบไฟล์", "รูปแบบวิดีโอ", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - ไฟล์วิดีโอ TrueMotion",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VP9 และ API ที่สามารถสร้างและเปิดไฟล์ VP9",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## ไฟล์ VP9 คืออะไร??

Google ได้พัฒนาตัวแปลงสัญญาณ VP9 เป็นมาตรฐานการเข้ารหัสวิดีโอแบบโอเพ่นซอร์สที่ไม่มีค่าลิขสิทธิ์ โดยเป็นรุ่นต่อจาก VP8 เดิมทีออกแบบมาเพื่อบีบอัดเนื้อหาความละเอียดสูงพิเศษบน YouTube เนื่องจากขยายและปรับปรุงประสิทธิภาพการเข้ารหัสของรุ่นก่อน หากเราพูดถึงตัวแปลงสัญญาณ VPX ดั้งเดิม พวกมันมาจากเทคโนโลยี On2 ซึ่ง Google หลอมรวมเข้าด้วยกันในปี 2010 ต่อมา Google ได้เปิดแหล่งที่มาของตัวแปลงสัญญาณดังกล่าว VP8 และ VP9 ทั้งสองรูปแบบมีให้ใช้ภายใต้ใบอนุญาต BSD ฟรี ซึ่งอนุญาตให้ผู้ปฏิบัติงานจัดระเบียบการเข้ารหัสหรือถอดรหัสความเชี่ยวชาญทั้งในซอฟต์แวร์เอกสิทธิ์และซอฟต์แวร์โอเพ่นซอร์สโดยไม่ต้องเปิดเผยซอร์สโค้ด

## คุณสมบัติทางเทคนิคของ VP9

* VP9 ให้ความละเอียดสูงสุด 8192x4352 ที่สูงสุด 120 fps และช่วงสีที่หลากหลายด้วย Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 และ sRGB
* รูปแบบนี้รองรับการใช้งานเว็บไซต์และมือถืออย่างเต็มรูปแบบตั้งแต่การบีบอัดบิตเรตต่ำไปจนถึง ultra-HD คุณภาพสูง พร้อมการสนับสนุนเพิ่มเติมสำหรับการเข้ารหัส 10/12 บิตและ HDR
* สามารถลดอัตราบิตวิดีโอได้มากถึง 50% เมื่อเปรียบเทียบกับอัตราบิตอื่น ๆ
* รองรับการสตรีมแบบปรับได้และใช้งานโดย YouTube และผู้ให้บริการเว็บวิดีโอที่มีชื่อเสียงอื่นๆ
* อุปกรณ์ Chrome, Opera, Edge, Firefox และ Android ตลอดจนสมาร์ททีวีหลายล้านเครื่อง รองรับการถอดรหัสของตัวแปลงสัญญาณนี้
* ความละเอียดวิดีโอที่มากกว่า 1080p ได้รับการแก้ไขผ่าน VP9 และอนุญาตให้มีการบีบอัดแบบไม่สูญเสียข้อมูล
* พื้นที่สีต่างๆ เช่น Rec. 601, Rec. 709, ประวัติ 2020, SMPTE-170, SMPTE-240 และ sRGB รองรับโดย VP9
* วิดีโอ HDR ที่ใช้ Hybrid Log-Gamma และ Perceptual Quantizer ยังรองรับโดย VP9


## ประวัติย่อ

* การพัฒนาตัวแปลงสัญญาณวิดีโอ VP9 ได้เริ่มขึ้นในปี 2554 และเพิ่มตัวถอดรหัสลงในเว็บเบราว์เซอร์ Chromium ในเดือนธันวาคม 2555
* เว็บเบราว์เซอร์ Google Chrome เวอร์ชันแรกเปิดตัวในเดือนกุมภาพันธ์ 2013 และเผยแพร่การถอดรหัสในเวลานั้น
* Google เปิดตัว Chrome 29.0.1547 พร้อมการสนับสนุนขั้นสุดท้าย VP9 ในเดือนสิงหาคม 2013
* ในเดือนตุลาคม 2013 มีการเพิ่มตัวถอดรหัส VP9 ตามสัญชาตญาณใน FFmpeg
* Mozilla ได้เพิ่ม VP9 sustenance ให้กับ Firefox ในเดือนธันวาคม 2013 ในเวอร์ชัน 2 ซึ่งเปิดตัวเมื่อวันที่ 18 มีนาคม 2014
 

## การทำงานของ VP9

โดยปกติแล้ว วิดีโอ 4K จะเพิ่มคุณภาพของภาพโดยทำให้พิกเซลบางพิกเซลเล็กลง ตัวแปลงสัญญาณ VP9 และ HEVC ทำให้พิกเซลใหญ่ขึ้นเพื่อลดขนาดบิตเรตและขนาดไฟล์ แม้ว่าสิ่งนี้อาจดูขัดแย้งกัน แต่เอ็นจิ้นการเข้ารหัสจะใช้พิกเซลที่ใหญ่ขึ้นและเปลี่ยนให้เป็นผลผลิตที่มีความละเอียดดีขึ้น วิดีโอต้นทาง ซึ่งเกี่ยวข้องกับเฟรมวิดีโอ ถูกเข้ารหัสหรือบีบอัดเพื่อสร้างบิตสตรีมวิดีโอที่ถูกบีบอัด แต่ละเฟรมที่แยกจากกันจะถูกแบ่งออกเป็นบล็อกพิกเซลก่อน จากนั้นบล็อกจะถูกตรวจสอบสำหรับการเลิกจ้างแบบสามมิติและการเชื่อมต่อตามลำดับระหว่างเฟรมจะได้รับการประเมินเพื่อใช้ประโยชน์จากพื้นที่ที่ไม่สามารถเปลี่ยนแปลงได้ สิ่งเหล่านี้ถูกเข้ารหัสผ่านเวกเตอร์การเคลื่อนไหวที่รับประกันคุณภาพของบล็อกที่กำหนดในเฟรมถัดไป ข้อมูลที่เหลือจะถูกเข้ารหัสโดยใช้การบีบอัดแบบไบนารีที่มีประสิทธิผล

## อ้างอิง

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [เอกสารเว็บ MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [มะพร้าว](https://www.coconut.co/)

