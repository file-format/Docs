{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - ไฟล์กำหนดค่า",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CONFIG พร้อมตัวอย่าง CONFIG และ API ที่สามารถสร้างและเปิดไฟล์ CONFIG",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## ไฟล์ CONFIG คืออะไร??
ไฟล์ CONFIG เรียกว่าไฟล์กำหนดค่า ใช้เพื่อกำหนดค่าพารามิเตอร์และการตั้งค่าหลักสำหรับซอฟต์แวร์คอมพิวเตอร์หลายตัว ซอฟต์แวร์บางตัวอ่าน **ไฟล์คอนฟิกูเรชัน** เมื่อเริ่มต้นเท่านั้น อื่น ๆ ตรวจสอบไฟล์การกำหนดค่าสำหรับการเปลี่ยนแปลงเป็นระยะ ๆ

## รูปแบบไฟล์ CONFIG
**รูปแบบไฟล์ CONFIG** ใช้สำหรับการประมวลผลของเซิร์ฟเวอร์ แอปพลิเคชันซอฟต์แวร์ และการตั้งค่าระบบปฏิบัติการ โปรแกรมเมอร์สามารถเขียนโค้ดเพื่อสั่งให้ซอฟต์แวร์อ่านไฟล์คอนฟิกูเรชันครั้งแล้วครั้งเล่าหลังจากช่วงเวลาหนึ่งและใช้การเปลี่ยนแปลงกับกระบวนการปัจจุบัน ไม่มีมาตรฐานที่แน่นอนหรือแบบแผนที่ชัดเจนสำหรับ SYSNtax ของไฟล์ CONFIG ตัวอย่างเช่น ไฟล์ Web.config ของ Microsoft เป็นของรูปแบบไฟล์ CONFIG ซึ่งประกอบด้วยชุดแท็กตาม [XML](/web/xml/) สามารถแก้ไขได้ด้วย Microsoft Visual Studio หรือโปรแกรมแก้ไขข้อความอื่นๆ

## ตัวอย่างของไฟล์คอนฟิกูเรชัน:
เนื่องจากไฟล์คอนฟิกูเรชันไม่ได้ถูกสร้างขึ้นตามกฎ สแตนด์ราด หรือแบบแผนใดๆ ไฟล์เหล่านี้จึงอาจเขียนขึ้นโดยใช้รูปแบบที่แตกต่างกัน ไฟล์ .config อาจใช้ XML, [JSON](/web/json/) หรือรูปแบบอื่นๆ ต่อไปนี้เป็นตัวอย่างของไฟล์คอนฟิกูเรชันสำหรับระบบปฏิบัติการและซอฟต์แวร์ที่รู้จักกันดี:

### ไฟล์การกำหนดค่าใน Linux
โปรแกรม Linux ทุกโปรแกรมเป็นไฟล์เรียกทำงานซึ่งเก็บรายการ **opcodes** ที่ CPU เรียกใช้งานเพื่อดำเนินการทั่วไปให้สำเร็จ การทำงานของเกือบทุกโปรแกรมสามารถปรับแต่งตามความต้องการของคุณได้โดยการเปลี่ยนไฟล์คอนฟิกูเรชัน ไฟล์คอนฟิกูเรชันหลายไฟล์ในระบบ Linux อยู่ในไดเร็กทอรี /etc ไฟล์คอนฟิกูเรชันสามารถแบ่งออกเป็นประเภทต่อไปนี้:
|ประเภท|ตัวอย่าง| ความคิดเห็น|
---|---|---|
|เข้าถึงไฟล์|/etc/host.conf|บอกเซิร์ฟเวอร์โดเมนเครือข่ายถึงวิธีค้นหาชื่อโฮสต์|
|การบูตและการเข้าสู่ระบบ/ออกจากระบบ|/etc/rc.d/rc.local|ไม่เป็นทางการ อาจถูกเรียกจาก rc, rc.sysinit หรือ /etc/inittab.|
|ระบบไฟล์|/etc/mtools.conf|การกำหนดค่าสำหรับการดำเนินการทั้งหมด (mkdir, คัดลอก, รูปแบบ ฯลฯ) บนระบบไฟล์ประเภท DOS|
|การดูแลระบบ|/etc/shells|เก็บรายการของ "shell" ที่เป็นไปได้ที่ระบบมีอยู่|
|เครือข่าย|/etc/gated.conf|การกำหนดค่าสำหรับ gated ใช้โดย gated daemon เท่านั้น|
|คำสั่งระบบ|/etc/logrotate.conf|การกำหนดค่าสำหรับ Dynamic Linker|
|Daemons|/etc/httpd.conf|ไฟล์การกำหนดค่าสำหรับ Apache ซึ่งเป็นเว็บเซิร์ฟเวอร์ โดยทั่วไปแล้วไฟล์นี้จะไม่อยู่ใน /etc.|
|โปรแกรมผู้ใช้| /etc/lynx.cfg| การตั้งค่าพร็อกซี|
### ตัวอย่างไฟล์ AWS CONFIG
การตั้งค่าการกำหนดค่าและข้อมูลรับรองที่ใช้บ่อยสามารถบันทึกไว้ในไฟล์ CONFIG ที่ดูแลโดย AWS CLI ไฟล์ CONFIG ต้องเป็นไฟล์ข้อความล้วนที่ใช้รูปแบบต่อไปนี้:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### ตัวอย่างไฟล์ SSH CONFIG
ไฟล์การกำหนดค่าฝั่งไคลเอนต์ OpenSSH มีชื่อว่า CONFIG และจัดเก็บอยู่ในไดเร็กทอรี .ssh ไฟล์ SSH CONFIG ประกอบด้วยโครงสร้างต่อไปนี้:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### ตัวอย่างไฟล์ Python CONFIG
ไฟล์ Python CONFIG อาจมีลักษณะดังนี้:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## อ้างอิง

* [ทำความเข้าใจไฟล์คอนฟิกูเรชัน Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [การกำหนดค่าและการตั้งค่าไฟล์ข้อมูลรับรอง](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [ไฟล์การกำหนดค่าใน Python](https://martin-thoma.com/configuration-files-in-python/)

