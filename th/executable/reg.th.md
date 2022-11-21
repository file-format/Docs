{
  "date" : "2021-08-02",
  "keywords" :[ "ไฟล์ reg", "รูปแบบไฟล์ reg", "ไฟล์ reg คืออะไร", "ไฟล์", "ตัวอย่าง reg", "นามสกุลไฟล์ reg", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ REG และ API ที่สามารถสร้างและเปิดไฟล์ REG",
  "title" :"REG - ไฟล์รีจิสทรีของ Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## ไฟล์ REG คืออะไร??
ไฟล์ REG เป็นเพียงไฟล์ข้อความที่มีนามสกุล .reg ไฟล์เหล่านี้มักจะสร้างขึ้นโดยการส่งออกคีย์ทั่วไปจาก Registry ไฟล์เหล่านี้สามารถใช้เป็นข้อมูลสำรองของรีจิสทรี (ขั้นตอนนี้สำคัญเป็นพิเศษก่อนทำการเปลี่ยนแปลง!) คุณจะเห็นว่าบางไฟล์มีให้ดาวน์โหลดเป็นไฟล์ในเว็บไซต์เดียวกับที่แสดงวิธีการแฮ็ก Registry ไฟล์ REG มีประโยชน์ในการเปลี่ยนแปลง Registry ด้วยตนเองและส่งออกการเปลี่ยนแปลงเหล่านั้น เพียงทำความสะอาดไฟล์เล็กน้อยแล้วแบ่งปันกับผู้อื่น

## รูปแบบไฟล์ REG
รูปแบบไฟล์ REG ได้รับการออกแบบมาสำหรับการส่งออกและนำเข้าบางส่วนของรีจิสทรีของ Windows โดยใช้ไวยากรณ์ที่ใช้ INI Windows Registry เป็นฐานข้อมูลเชิงสัมพันธ์หรือลำดับชั้นที่เก็บการตั้งค่าระดับต่ำสำหรับระบบปฏิบัติการ Microsoft Windows และแอปพลิเคชันอื่นๆ ที่ใช้รีจิสทรีของ Windows อีกทางเลือกหนึ่งคือ รีจิสทรีหรือ Windows Registry ประกอบด้วยข้อมูล ตัวเลือก การตั้งค่า และค่าอื่นๆ สำหรับโปรแกรมและฮาร์ดแวร์ที่ติดตั้งบนระบบปฏิบัติการ Microsoft Windows ทุกรุ่น
### ไวยากรณ์ของไฟล์ REG
ต่อไปนี้คือองค์ประกอบหลักบางส่วนที่เป็นส่วนหนึ่งของไวยากรณ์ไฟล์ REG:
- **RegistryEditorVersion**: เช่น "Windows Registry Editor เวอร์ชัน 5.00" สำหรับ Windows 2000, Windows XP และ Windows Server 2003
- **บรรทัดว่าง**: ระบุจุดเริ่มต้นของเส้นทางรีจิสทรีใหม่
- **RegistryPathx**: เส้นทางของคีย์ย่อยที่เก็บค่าแรกที่คุณกำลังนำเข้า
- **DataItemNamex**: ชื่อของรายการข้อมูลที่คุณต้องการนำเข้า
- **DataTypex**: ชนิดข้อมูลสำหรับค่ารีจิสทรี

คีย์ถูกจัดเก็บไว้ในไฟล์ .reg โดยใช้ไวยากรณ์ต่อไปนี้:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
คุณสามารถแก้ไขค่าเริ่มต้นของคีย์ได้โดยใช้ "@" แทน "ชื่อค่า":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### ตัวอย่าง
นี่คือตัวอย่างไฟล์ REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## อ้างอิง

* [Windows Registry- โดย Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [วิธีเพิ่ม แก้ไข หรือลบคีย์ย่อยและค่าของรีจิสทรีโดยใช้ไฟล์ .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- รีจิสทรีคีย์ย่อยและค่าโดยใช้ a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


