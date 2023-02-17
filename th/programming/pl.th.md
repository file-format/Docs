{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "file", "extension", "format", "Perl", "Perl language", "PL files", "programming"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PL และ API ที่สามารถสร้างและเปิดไฟล์ PL",
  "title" :"ไฟล์ PL - รูปแบบไฟล์สคริปต์ Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## ไฟล์ PL คืออะไร??

ไฟล์ที่มีนามสกุล .pl คือไฟล์ Perl Script ที่เป็นภาษาสคริปต์ สิ่งเหล่านี้รวบรวมและเรียกใช้โดยใช้ซอฟต์แวร์ Perl Interpreter ไฟล์สคริปต์ PL ประกอบด้วยบรรทัดของโค้ด ตัวแปร และความคิดเห็น ภาษาสคริปต์ค่อนข้างยาก
ทำความเข้าใจกับรูปแบบไฟล์โปรแกรมอื่นๆ เช่น [PHP](/th/programming/php/) สามารถสร้างไฟล์ PL และเข้ากันได้กับ Windows, macOS และ Linux

## ประวัติย่อของภาษาสคริปต์ Perl

ภาษานี้ถูกใช้งานครั้งแรกในปี 1987 ดังนั้นไฟล์เหล่านี้จึงมีต้นกำเนิดในปีนั้น ในปี 1989 Perl 2 ได้รับการปล่อยตัว ต่อมาได้มีการปรับปรุงและแก้ไขเป็นเวอร์ชัน 5.35 และเวอร์ชันถัดไปมีเป้าหมายที่จะออกในปีหน้า

ในการอัปเดตทุกครั้ง มีการเพิ่มเครื่องมือเกี่ยวกับการทำงาน ประสิทธิภาพ และรูปลักษณ์ของภาษาและไฟล์ มีการเปลี่ยนแปลงมากมายเกี่ยวกับเวอร์ชันในปีนี้ เดิมเป็นภาษาสคริปต์พื้นฐาน แต่ตอนนี้ประกอบด้วยโมดูลอื่น ๆ อีกมากมายด้วย เดิมทีเป็นภาษาที่เรียบง่ายมาก แต่สคริปต์ของภาษานี้ค่อนข้างเข้าใจยากเนื่องจากมีขนาดเล็ก

## ข้อมูลจำเพาะส่วนขยายรูปแบบไฟล์ Perl

มีคุณสมบัติหรือข้อกำหนดของไฟล์โปรแกรมเหล่านี้บางส่วนมีดังนี้:

* รหัสที่รวมอยู่ในไฟล์เหล่านี้อยู่ในรูปแบบข้อความธรรมดาและใช้สำหรับการพัฒนาสคริปต์
* สคริปต์ของเซิร์ฟเวอร์ การแยกวิเคราะห์ข้อความ และการดูแลระบบเซิร์ฟเวอร์เป็นประเด็นหลักที่สคริปต์ของภาษานี้ครอบคลุม
* โปรแกรมยอดนิยมหลายโปรแกรมที่เกี่ยวข้องกับภาษานี้คือ Active state Active Perl และ Bare Bones BBEdit (เข้ากันได้กับ Mac OS)
* ภาษานี้ถือเป็นภาษาระดับสูง
* สำหรับ Win32 ผู้ใช้อาจต้องติดตั้งการแจกแจงไบนารีดั้งเดิมของภาษา
* ต้องใช้เครื่องมือสคริปต์บางอย่างเพื่อให้สามารถเรียกใช้งานได้ใน Windows Resource Kits ต่างๆ
* Visual Studio .NET เป็นเฟรมเวิร์กที่มีชื่อเสียงสำหรับการพัฒนาภาษาโปรแกรม เครื่องมือ Active State ที่เรียกว่า Visual Perl ใช้เพื่อเพิ่ม Perl ลงใน Visual Studio
* ในไฟล์ บรรทัดแรกของซอร์สโค้ดจะอธิบายข้อมูลของล่ามที่ใช้ ไฟล์ PL มักจะขึ้นต้นด้วย **#!/usr/bin/perl** บรรทัดที่บอกให้คอมพิวเตอร์ของคุณเรียกใช้สคริปต์นี้โดยใช้ตัวแปล Perl ที่ติดตั้งในคอมพิวเตอร์


## ตัวอย่างสคริปต์ PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

สิ่งนี้จะพิมพ์

```
Hello, World
```

### ความคิดเห็นบรรทัดเดียว ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### ความคิดเห็นหลายบรรทัด ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### การกำหนดตัวแปร ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### การกำหนดตัวแปรสเกลาร์ ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### การดำเนินการสเกลาร์อย่างง่าย ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## อ้างอิง ##

- [Python (ภาษาโปรแกรม) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))
