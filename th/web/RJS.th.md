{
  "date" : "2021-05-24",
  "keywords" :["rjs", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "นามสกุลไฟล์", "RJS", "ไฟล์ Ruby JavaScript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - ไฟล์ Ruby Javascript",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RJS และ API ที่สามารถสร้างและเปิดไฟล์ RJS ได้",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ไฟล์ RJS คืออะไร??

ไฟล์ที่มีนามสกุล .rjs คือการรวมกันของรหัส Ruby และ JavsScript ที่ช่วยให้นักพัฒนา Rails ใช้ Ruby เพื่อสร้างรหัส JavaScript แบบไดนามิก รหัส Ruby ถูกฝังอยู่ในฟังก์ชั่น Java และถูกคอมไพล์บนเว็บเซิร์ฟเวอร์ที่ต้องใช้เครื่องยนต์ Ruby เพื่อให้ทำงานบนเซิร์ฟเวอร์ RJS คล้ายกับ [RHTML](/th/web/rhtml/); ข้อแตกต่างเพียงอย่างเดียวคือด้านข้างมีโค้ด Ruby ใน [HTML](/th/web/html/) ในขณะที่มีโค้ด Ruby ในฟังก์ชัน Javascript

## รูปแบบไฟล์ RJS

ไฟล์ RJS จะถูกเข้ารหัสเป็นข้อความล้วนเหมือนกับภาษาสคริปต์หรือภาษาโปรแกรมอื่นๆ เมื่อไคลเอนต์ร้องขอเพจดังกล่าว โค้ด Ruby จะถูกดำเนินการบนเซิร์ฟเวอร์ และเฉพาะโค้ด HTML และ Javascript เท่านั้นที่จะถูกส่งกลับไปยังเบราว์เซอร์ของไคลเอนต์ ไวยากรณ์ของไฟล์ RJS คล้ายกับการรวมไวยากรณ์ของ Ruby และ JavaScript เช่น เฉพาะรหัส Ruby เท่านั้นที่ฝังอยู่ในฟังก์ชัน JavaScript

### ตัวอย่าง RJS

ตัวอย่างต่อไปนี้แสดงโค้ด Ruby อย่างง่ายโดยแยกจากกัน จากนั้นฝังในฟังก์ชัน JavaScript

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
และต่อไปนี้คือ RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## อ้างอิง

* [RJS](https://github.com/makevoid/rjs)

