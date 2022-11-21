{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "partial", "extension", "file", "format", "web", "downloaded" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - ไฟล์ที่ดาวน์โหลดบางส่วน",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PART และ API ที่สามารถสร้างและเปิดไฟล์ PART",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## ไฟล์ PART คืออะไร?? ##

ไฟล์ส่วนหนึ่งหรือนามสกุล .part คือไฟล์ที่ดาวน์โหลดมาบางส่วน จะใช้เมื่อการดาวน์โหลดกำลังดำเนินการหรือถูกขัดจังหวะเนื่องจากปัญหาใด ๆ ทำให้ตัวจัดการการดาวน์โหลดมีโอกาสที่จะดำเนินการดาวน์โหลดต่อได้ทุกเมื่อที่ทำได้
ซึ่งหมายความว่าเบราว์เซอร์ เช่น Firefox หรือโปรแกรมถ่ายโอนไฟล์ เช่น eMule, eMule plus, FlashGet ฯลฯ จะเก็บไฟล์ส่วนหนึ่งไว้ เรียกว่า Part file ขณะที่กำลังดาวน์โหลดบนอุปกรณ์ของคุณ ไฟล์ส่วนนี้จะแสดงให้คุณเห็นว่าการดาวน์โหลดกำลังดำเนินการหรือถูกขัดจังหวะก่อนที่จะเสร็จสิ้น ไม่เพียงแค่นี้ แต่ไฟล์ PART จะเก็บข้อมูลทั้งหมดไว้จนกว่าการดาวน์โหลดจะเสร็จสิ้น ซึ่งเป็นสาเหตุที่บางไฟล์สามารถกลับมาทำงานต่อได้ในภายหลัง หากคุณต้องการเริ่มการดาวน์โหลดอีกครั้ง

## รูปแบบไฟล์ PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
