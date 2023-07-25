{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - รูปแบบไฟล์สคริปต์ Haskell",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ HS และ API ที่สามารถสร้างและเปิดไฟล์ HS ได้",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - รูปแบบไฟล์ Java HelpSet

## ไฟล์ Java HS คืออะไร??

ไฟล์ที่มีนามสกุล .hs ในภาษาโปรแกรม Java เป็นไฟล์เอกสารวิธีใช้ที่ใช้โดยระบบ JavaHelp เมื่อเปิดใช้งานโดยแอปพลิเคชัน กำหนดชุดความช่วยเหลือสำหรับแอปพลิเคชันเฉพาะที่ติดตั้งและประกอบด้วยชุดย่อยหลายชุดซึ่งเป็นส่วนหนึ่งของวิธีใช้ระบบสำหรับแอปพลิเคชัน โปรแกรม Java ต้องสามารถค้นหาไฟล์ helpset ที่ชื่อลงท้ายด้วยนามสกุล .hs

## ข้อมูลชุดช่วยเหลือ Java

ไฟล์ .hs อาจมีข้อมูลต่อไปนี้

|ข้อมูล|คำอธิบาย|
---|---|
|ไฟล์แผนที่|ไฟล์แผนที่ถูกใช้เพื่อเชื่อมโยงรหัสหัวข้อกับตัวระบุตำแหน่งทรัพยากรแบบเดียวกันหรือชื่อพาธของไฟล์หัวข้อภาษามาร์กอัปไฮเปอร์เท็กซ์|
|ดูข้อมูล|ข้อมูลที่อธิบายตัวนำทางที่ใช้งานอยู่ในชุดความช่วยเหลือ เนวิเกเตอร์คุณภาพ ได้แก่ สารบัญ ดัชนี และการค้นหาข้อความแบบเต็ม ตัวนำทางเพิ่มเติมรวมถึงเงาและตัวนำทางรายการโปรด ข้อมูลเพิ่มเติมเกี่ยวกับเนวิเกเตอร์ที่กำหนดเองถูกแนบไว้ที่นี่|
<html>|ชื่อชุดความช่วยเหลือ|The \<title> มีระบุไว้ในไฟล์ helpset (.hs) ชื่อนี้จะดูเหมือนอยู่ด้านบนสุดของหน้าต่างส่วนใหญ่และหน้าต่างรองใดๆ ที่อยู่ในไฟล์ helpset ของคุณ| </html>,
|Home ID|ชื่อของ ID (ค่าเริ่มต้น) ที่แสดงเมื่อมีการเรียกผู้เฝ้าดูความช่วยเหลือโดยไม่ระบุ ID|
|การนำเสนอ|หน้าต่างสำหรับแสดงอาสาสมัคร นี่อาจเป็นการรวมที่ทันสมัยของโปรแกรมคอมพิวเตอร์ JavaHelp 2 ซึ่งมีรายละเอียดเพิ่มเติมอยู่ใต้ \<presentation> .|
|ชุดความช่วยเหลือย่อย|พื้นที่ตามดุลยพินิจนี้จะรวมชุดความช่วยเหลืออื่นๆ แบบคงที่โดยใช้แท็ก ชุดความช่วยเหลือที่แสดงโดยแท็กนี้จะรวมกันเป็นชุดความช่วยเหลือที่มีแท็ก จุดสนใจเพิ่มเติมเกี่ยวกับการผสมสามารถพบได้ใน Blending Helpets|
|การนำไปปฏิบัติ|เซกเมนต์ตามดุลยพินิจนี้สร้างรีจีสทรีที่ให้การแมปข้อมูลสำคัญเพื่อกำหนดลักษณะของคลาส HelpBroker เพื่อใช้ภายในเมธอด HelpSet.createHelpBroker นอกจากนี้ รีจิสทรียังตัดสินใจเลือกโปรแกรมดูเนื้อหาไปยังไคลเอ็นต์สำหรับการจัดเรียง Emulate ที่กำหนด|

## รูปแบบไฟล์ Java HS

ไฟล์ Java HS อยู่ในรูปแบบไฟล์ XML และอิงตามคำแนะนำที่เสนอของ World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). ซึ่งหมายความว่าไฟล์ Java HS อยู่ในรูปแบบไฟล์ XML ที่มนุษย์อ่านได้ ซึ่งสามารถเปิดได้ในแอปพลิเคชันตัวอ่าน XML ใดๆ

### ตัวอย่างรูปแบบไฟล์ Java HS

ต่อไปนี้เป็นตัวอย่างของไฟล์ helpset จาก [เอกสาร Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## อ้างอิง
* [ไฟล์ Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - รูปแบบไฟล์สคริปต์ Haskell

## ไฟล์ HS คืออะไร??

ไฟล์ที่มีนามสกุล .hs คือไฟล์สคริปต์ Haskell ที่เขียนด้วย [Haskell](https://wiki.haskell.org/Haskell) ซึ่งเป็นภาษาโปรแกรมโอเพนซอร์ซขั้นสูงที่ใช้งานได้อย่างแท้จริง โค้ดที่เขียนในไฟล์ HS จะขึ้นอยู่กับฟังก์ชันเท่านั้น ซึ่งแตกต่างจาก [C](/th/programming/c/), [C++](/th/programming/cpp/) และอื่นๆ ที่เป็นไปตามหลักการพัฒนาอย่างรวดเร็วของซอฟต์แวร์ที่มีประสิทธิภาพและรัดกุม Haskell มอบการทำงานพร้อมกันในตัวและความขนานพร้อมกับ APIs ที่หลากหลาย ตัวสร้างโปรไฟล์และตัวดีบั๊กเพื่อสร้างแอปพลิเคชันที่ยืดหยุ่นและมีคุณภาพสูง

## รูปแบบไฟล์ H.S

เช่นเดียวกับภาษาการเขียนโปรแกรม ไฟล์ HS ถูกเขียนในรูปแบบข้อความล้วนที่มนุษย์สามารถอ่านได้ สิ่งเหล่านี้สามารถสร้าง แก้ไข และดูได้ด้วยเครื่องมือข้อความที่มีอยู่ ไฟล์ซอร์สโค้ด .hs ถูกคอมไพล์ด้วยคอมไพเลอร์ Haskell ซึ่งสร้างไฟล์ไบนารีที่เรียกใช้งานได้

### ตัวอย่างรูปแบบไฟล์ HS

สามารถเขียนโค้ดในไฟล์ .hs และคอมไพล์โดยใช้คอมไพเลอร์ Haskell เช่น [GHC](https://haskell.org/ghc) โค้ดบรรทัดต่อไปนี้บันทึกเป็น `HelloWorld.hs` ตามที่แสดงในตัวอย่างต่อไปนี้

```
main = putStrLn "Hello, World!"
```

สิ่งนี้รวบรวมโดยใช้คำสั่ง:

```
$ ghc -o hello hello.hs
```
และไฟล์ปฏิบัติการที่เป็นผลลัพธ์สามารถเรียกใช้เป็น:

```
$ ./hello
```
นี่พิมพ์คำว่า "Hello, World!" คำสั่งไปยังผลลัพธ์

## อ้างอิง

* [แฮสเคลล์](https://wiki.haskell.org/Haskell)
* [Haskell ใน 5 ขั้นตอนง่ายๆ](https://wiki.haskell.org/Haskell_in_5_steps)

