{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ HAML - ไฟล์ซอร์สโค้ด Haml",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ HAML และ API ที่สามารถสร้างและเปิดไฟล์ HAML",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## ไฟล์ HAML คืออะไร??

ไฟล์ HAML เป็นไฟล์ภาษามาร์กอัป HTML ที่เป็นนามธรรมซึ่งมีซอร์สโค้ดที่เขียนด้วยภาษา [Haml](https://haml.info/) สามารถใช้แทน ERB (สคริปต์เทมเพลต Ruby) ไฟล์ HAML มีซอร์สโค้ดเทมเพลตสำหรับสร้าง HTML ของเอกสารเว็บ ไฟล์ ERB สามารถแทนที่ได้โดยเพียงแค่แทนที่ไฟล์เหล่านี้ในโฟลเดอร์ app/views เป็น Haml โดยเปลี่ยนนามสกุลของไฟล์ ไฟล์ HAML สามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad, Notepad++, Apple TextEdit,

## รูปแบบไฟล์ HAML

ไฟล์ HAML เป็นไฟล์ต้นฉบับที่บันทึกลงดิสก์เป็นไฟล์ข้อความธรรมดา มันมีรหัสที่เขียนด้วยไวยากรณ์ HAML HAML แทนที่แท็ก **<>** ด้วยเครื่องหมาย **%** เพื่อให้โค้ดเรียบง่ายและง่ายขึ้น ไฟล์ ERB สามารถแทนที่ได้ด้วย HAML ดังที่แสดงในตัวอย่างง่ายๆ ต่อไปนี้

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### ตัวอย่าง HAML

ต่อไปนี้คือตัวอย่าง Hello World ตัวอย่างของ HAML

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
ซึ่งแสดงผลเป็นเอาต์พุต HTML ต่อไปนี้

```
<p class="sample" id="welcome">Hello, World!</p>
```

## อ้างอิง

* [HAML - Github](https://github.com/haml/haml)

