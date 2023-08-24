{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - รูปแบบไฟล์ Apple Mail",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EMLX และ API ที่สามารถสร้างและเปิดไฟล์ EMLX",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ EMLX คืออะไร??

รูปแบบไฟล์ EMLX ถูกนำมาใช้และพัฒนาโดย Apple แอปพลิเคชัน Apple Mail ใช้รูปแบบไฟล์ EMLX เพื่อส่งออกอีเมล มีแอปพลิเคชั่นอื่นที่สามารถเปิดไฟล์ EMLX และแปลงไฟล์เหล่านี้เป็นรูปแบบไฟล์อื่นได้

## ประวัติโดยย่อของรูปแบบไฟล์ EMLX

ระบบปฏิบัติการ Mac OS X นำโปรแกรมอีเมลที่มีอยู่ NeXTMail ซึ่งสร้างโดย NeXT เป็นส่วนหนึ่งของระบบปฏิบัติการ NeXTSTEP Apple หลังจากได้รับ NeXT ได้ยกระดับคุณสมบัติต่างๆ และกลายเป็นแอปพลิเคชันอีเมล Apple Mail ที่จะใช้เป็นโปรแกรมรับส่งอีเมลเริ่มต้น อีเมลที่ส่งออกผ่าน Apple Mail จะถูกบันทึกโดยตรงเป็นไฟล์ EMLX นอกจากนี้ยังเป็นไคลเอ็นต์อีเมลเริ่มต้นสำหรับไฟล์ EMLX เมื่อมีคนเปิดไฟล์เหล่านี้โดยดับเบิลคลิกบน Mac OS

## รูปแบบไฟล์ EMLX

ไฟล์ EMLx เป็นไฟล์ข้อความธรรมดาที่สามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ เช่น Notepad โครงสร้างไฟล์ EMLX ประกอบด้วยสามส่วน:

* จำนวนไบต์สำหรับข้อความ - ความยาวของข้อความเอง เขียนเป็น ASCII เป็นทศนิยม สิ้นสุดด้วย 0x0a
* ข้อความนั้นเอง
* ข้อมูลเมตาของข้อความในรูปแบบของ XML plist

สิ่งเหล่านี้สามารถอธิบายได้ดีขึ้นโดยใช้ตัวอย่างอีเมลที่แยกจาก Apple Mail เป็น EMLX และเปิดในโปรแกรมแก้ไขข้อความ

### ตัวอย่าง EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

ในตัวอย่างนี้ 875 จะแสดงความยาวทั้งหมดของข้อความ ข้อมูลเมตาของข้อความอยู่ใน<plist> แท็กและแฟล็กมีคำอธิบายดังต่อไปนี้:

|ฟิลด์|คำอธิบาย|ค่า
---|---|---|
|0|อ่าน|1 << 0
|1|ถูกลบ|1 << 1
|2|ตอบแล้ว|1 << 2
|3|เข้ารหัส|1 << 3
|4|ตั้งค่าสถานะ|1 << 4
|5|ล่าสุด|1 << 5
|6|ฉบับร่าง|1 << 6
|7|เริ่มต้น (เลิกใช้แล้ว)|1 << 7
|8|ส่งต่อ|1 << 8
|9|เปลี่ยนเส้นทาง|1 << 9
|10-15|จำนวนสิ่งที่แนบมา|3F << 10 (6 บิต)
|16-22|ระดับความสำคัญ|7F << 16 (7 บิต)
|23|ลงชื่อ|1 << 23
|24|เป็นขยะ|1 << 24
|25|ไม่ใช่ขยะ|1 << 25
|26-28|เดลต้าขนาดตัวอักษร|7 << 26 (3 บิต)
|29|บันทึกระดับเมลขยะแล้ว|1 << 29
|30|เน้นข้อความใน toc|1 << 30
|31|(ไม่ได้ใช้)|

## ดูสิ่งนี้ด้วย ##

* [EML](/th/email/eml/)
* [MSG](/th/email/msg/)
