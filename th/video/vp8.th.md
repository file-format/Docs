{
  "date" : "2021-03-10",
  "keywords" :[ "VP8", "ไฟล์", "ส่วนขยาย", "รูปแบบไฟล์", "รูปแบบวิดีโอ", "TrueMotion Video", "WebRTC", "WebM"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP8 - ไฟล์วิดีโอ TrueMotion",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VP8 และ API ที่สามารถสร้างและเปิดไฟล์ VP8",
  "linktitle" : "VP8",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## ไฟล์ VP8 คืออะไร??

VP8 ได้รับการประกาศโดย Google ว่าเป็นหนึ่งในรูปแบบวิดีโอที่ดีที่สุดโดยมีอัตราข้อมูลคุณภาพภาพและความเร็วในการเข้ารหัสที่ดีที่สุด ข้อได้เปรียบที่ดีที่สุดของ VP8 ก็คือการทดแทน H.264 ที่ไม่มีค่าลิขสิทธิ์ เป็นรูปแบบเฉพาะสำหรับการเข้ารหัสและถอดรหัสวิดีโอคุณภาพสูงในรูปแบบไฟล์หรือบิตสตรีม ไม่มีค่าใช้จ่ายใดๆ เนื่องจาก Google ได้เผยแพร่สิทธิบัตร VP8 ทั้งหมดภายใต้ใบอนุญาตสาธารณะแบบปลอดค่าลิขสิทธิ์ เกือบ 90% หรือมากกว่าของเซสชันวิดีโอ WebRTC ทั้งหมดใช้ VP8

## รูปแบบไฟล์ VP8

VP8 ได้รับการพัฒนาโดย On2 Technologies ในปี 2008 และต่อมาเป็นของ Google ในปี 2010 ข้อได้เปรียบหลักของตัวแปลงสัญญาณวิดีโอ VP8 คือไม่มีค่าลิขสิทธิ์ภายใต้ใบอนุญาตฟรี ออกแบบมาเพื่อให้บริการวิดีโอคุณภาพสูงสำหรับเว็บและอุปกรณ์เคลื่อนที่ คอนเทนเนอร์วิดีโอและเสียงตัวแรกสำหรับ VP8 คือ WebM และตัวแปลงสัญญาณนี้ได้รับเลือกให้เป็นตัวแปลงรหัสวิดีโอ WebRTC ในปี 2011 รูปแบบนี้ได้รับการยอมรับในแอปพลิเคชันอุตสาหกรรมมากมาย เช่น HTML5, การสื่อสารแบบเรียลไทม์บนเว็บ และการเล่นวิดีโอในเบราว์เซอร์ต่างๆ มีความต้องการของตลาดอย่างเต็มที่เพื่อรองรับรูปแบบนี้ที่ความละเอียดระดับ Full-HD ใช้เพื่อวัตถุประสงค์ต่างๆ เช่น การประชุมผ่านวิดีโอ การแพร่ภาพวิดีโอ และการบันทึกจากอุปกรณ์พกพา

## ข้อมูลจำเพาะ ##

### คุณสมบัติของ VP8
 



* ตัวแปลงสัญญาณวิดีโอฟรี
* รูปแบบไฟล์วิดีโอที่ก้าวหน้าที่สุด
* ปรับปรุงความต้านทานต่อการสูญเสียเฟรม
* ถอดรหัสวิดีโอความเร็วสูง
* ง่ายต่อการคิดค้นบนแพลตฟอร์มฮาร์ดแวร์
* มีคุณลักษณะเฉพาะของโหมดแนะนำตัว กล่าวคือ ใช้เฉพาะเฟรมที่มีรหัสเฉพาะบุคคลโดยไม่มีการคาดคะเนตามลำดับ เพื่อเปิดใช้งานการเข้าถึงแบบสุ่มในแอปพลิเคชัน เช่น การตัดต่อวิดีโอ
* libvpx เป็นไลบรารีซอฟต์แวร์เดียวที่เชี่ยวชาญในการเข้ารหัสสตรีมวิดีโอ VP8
* VP8 ได้รับการออกแบบอย่างชัดเจนให้ทำงานในช่วงคุณภาพเป็นหลัก

* มีฮาร์ดแวร์ไคลเอ็นต์หลากหลายประเภทที่เชื่อมต่อกับเว็บ ขยายจากอุปกรณ์เคลื่อนที่และฝังพลังงานต่ำไปจนถึงคอมพิวเตอร์เดสก์ท็อปขั้นสูงสุดที่มีแกนประมวลผลจำนวนมาก
* การสุ่มตัวอย่างสี 420 สี, ความลึกของสี 8 บิตต่อแชนเนล, การสแกนแบบโปรเกรสซีฟ และขนาดภาพสูงสุด 16383x16383 พิกเซล รูปแบบภาพสามารถดำเนินการได้ง่ายๆ ผ่าน VP8
* แรงกระตุ้นสำหรับความสามารถในการบีบอัดและความเรียบง่ายของตัวถอดรหัสภายใต้การออกแบบเหล่านี้ทำให้เกิดคุณสมบัติทางเทคนิคที่เป็นเอกลักษณ์หลายอย่างใน VP8 โดยเปรียบเทียบกับรูปแบบการบีบอัดวิดีโออื่นๆ ที่ได้รับการยอมรับ
* VP8 ใช้กรอบอ้างอิงสามกรอบ จากโครงร่างการชดเชยการเคลื่อนไหวอ้างอิงจำนวนมากที่เห็นในรูปแบบอื่นๆ
* VP8 ไม่จำกัดอัตราเฟรมหรืออัตราข้อมูล ใช้ 14 บิตสำหรับทั้งความกว้างและความสูง ซึ่งทำให้ความละเอียดสูงสุด 16384x16384 พิกเซล

### ข้อ จำกัด ของ VP8

ขีดจำกัดของ VP8 ในแง่ของความละเอียด อัตราข้อมูล และอัตราเฟรมมีดังนี้:

* VP8 ใช้ 14 บิตสำหรับความกว้างและความสูง สำหรับความละเอียดสูงสุด 16384x16384 พิกเซล
* VP9 ใช้ 16 บิตสำหรับความกว้างและความสูง สำหรับความละเอียดสูงสุด 65536x65536 พิกเซล
* ไม่มีข้อ จำกัด เกี่ยวกับอัตราเฟรมหรืออัตราข้อมูล
 



 



## อ้างอิง

* [วิกิพีเดีย VP8](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20was%20first%20released%20by,%2C%20replacing%20its%20predecessor%2C%20VP7.&text= บน%20พฤษภาคม%2019%2C%20at%20its,an%20irrevocable%20free%20patent%20license)
* [ลิงก์ Springer](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)
