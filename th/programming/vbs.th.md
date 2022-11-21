{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "สคริปต์ Visual Basic", "คู่มือการเขียนโปรแกรม", "ตัวอย่าง vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - ไฟล์สคริปต์ Visual Basic",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VBS และ API ที่สามารถสร้างและเปิดไฟล์ VBS",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## ไฟล์ VBS คืออะไร??

VBS หรือ VBScript เชื่อมต่อกับ Microsoft Visual Basic รุ่นสคริปต์ ในสภาพแวดล้อมของคอมพิวเตอร์ ผู้ใช้จะได้รับอนุญาตให้เข้าถึงและควบคุมหลายด้านของมัน VBScript ได้รับอนุญาตให้ใช้โมเดลชื่อ **Component Object Model** เพื่อใช้ประโยชน์จากองค์ประกอบและเครื่องมือของสภาพแวดล้อม สภาพแวดล้อมนี้ถูกระบุสำหรับการทำงานและเรียกใช้ VBScript

มันทำหน้าที่คล้ายกับ Javascript เมื่อลูกค้าเข้าถึงได้ในด้านการพัฒนาเว็บ นอกจากนี้ยังใช้โดยเซิร์ฟเวอร์สำหรับการประมวลผลหน้าเว็บ สามารถพิจารณาได้ในไฟล์สคริปต์ประเภทอื่นๆ เช่น แอปพลิเคชันของ [HTML](/th/web/html/)


## ประวัติย่อ ##

เปิดตัวครั้งแรกในปี 1996 โดยเป็นส่วนหนึ่งของเทคโนโลยีที่ Microsoft ใช้กับ Windows Scripts ได้รับการพัฒนาโดยเฉพาะเพื่อช่วยเหลือนักพัฒนาเว็บในขั้นต้น ในปีเดียวกัน Explorer ของ Microsoft Windows ชื่อ Internet Explorer ได้เปิดตัวพร้อมกับคุณสมบัติของ Visual Basic Script

ด้วยความก้าวหน้าทางเทคโนโลยีและการพัฒนาเว็บ VBScript หลายเวอร์ชันพร้อมกับคุณสมบัติขั้นสูงมากมายได้เปิดตัว ยิ่งไปกว่านั้น ในปีหน้า ภาษาสคริปต์นี้จะเป็นส่วนหนึ่งของ Microsoft Windows พร้อมฟีเจอร์ใหม่ๆ

## ข้อมูลจำเพาะทางเทคนิค ##

สำหรับหน้าเว็บที่ฝั่งเซิร์ฟเวอร์ เครื่องมือต่างๆ เช่น **Active Server Pages** จะใช้ร่วมกับ VBScript ภาษาสคริปต์นี้สามารถใช้ในคอมโพเนนต์สคริปต์ของ Windows ไฟล์ของภาษานี้ถูกจัดเก็บด้วยนามสกุล .vbs ใน Windows

มีโครงสร้างควบคุมมากมาย เช่น ลูปที่ใช้ในโค้ดของภาษานี้ นอกจากนี้ยังมีอาร์กิวเมนต์ที่เป็นบรรทัดคำสั่งและอาจตั้งชื่อหรือไม่ตั้งชื่อก็ได้ ไฟล์ของภาษานี้สามารถเก็บไว้ในโฟลเดอร์หรือบนเดสก์ท็อปของระบบปฏิบัติการ Windows แม้ว่าจะไม่มีสภาพแวดล้อมการพัฒนาแบบรวมเฉพาะสำหรับโปรแกรม VBScript เช่น Microsoft Script Editor แต่สิ่งอำนวยความสะดวกในการพัฒนาภาษานี้

เมื่อ VBScript โฮสต์โดยโฮสต์ Script ของ Windows จะมีคุณลักษณะต่างๆ ที่ค่อนข้างพบได้ทั่วไปในภาษาของสคริปต์ แต่ไม่มีใน Visual Basic 6.0 คุณลักษณะที่เกี่ยวข้องกับการเข้าถึงได้ง่ายหรือโดยตรง ได้แก่ เครื่องพิมพ์เครือข่าย อาร์กิวเมนต์บรรทัดคำสั่งที่ไม่มีชื่อและระบุชื่อ stdout และ stdin เครือข่ายที่ใช้ร่วมกัน เครื่องมือการจัดการ Windows ข้อมูลผู้ใช้ของเครือข่าย เช่น การเป็นสมาชิกกลุ่ม และอื่นๆ อีกมากมาย

## ตัวอย่างรูปแบบไฟล์ VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>,
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## อ้างอิง ##

* [VBS - โดย Wikipedia](https://en.wikipedia.org/wiki/VBScript)



