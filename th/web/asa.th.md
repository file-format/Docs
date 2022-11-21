{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "รูปแบบไฟล์", "ประเภทไฟล์", "ไฟล์ .asa คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ไฟล์การกำหนดค่า ASP",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ ASA และ API ที่สามารถสร้างและเปิดไฟล์ ASA ได้",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## ไฟล์ ASA คืออะไร??

ไฟล์ ASA เป็นไฟล์กำหนดค่าที่สร้างขึ้นสำหรับโปรเจ็กต์ [ASP](/th/web/asp/)/ASP.NET ประกอบด้วยการประกาศตัวแปร ประกอบด้วย และฟังก์ชันที่เข้าถึงได้ในระดับ Global ในแอปพลิเคชัน หน้าทั้งหมดในโครงการสามารถเข้าถึงตัวแปรและฟังก์ชันเหล่านี้ได้ จึงไม่ต้องเขียนใหม่ ตัวอย่างหนึ่งคือหน้า Global.asa ที่จัดเก็บไว้ในไดเร็กทอรีรากเพื่อให้เข้าถึงได้โดยหน้าเว็บไซต์ ASP อื่น ไฟล์ Global.asa เป็นตัวเลือก แต่ถ้าใช้ แต่ละแอปพลิเคชันจะมีไฟล์ Global.asa ได้เพียงไฟล์เดียวเท่านั้น

## รูปแบบไฟล์ ASA - ข้อมูลเพิ่มเติม

ไฟล์ ASA เป็นไฟล์ข้อความธรรมดาที่มีข้อมูลต่อไปนี้

* กิจกรรมการสมัคร
* เหตุการณ์เซสชัน
* \<object> ประกาศ
* ประกาศ TypeLibrary
* คำสั่ง #include

## ตัวอย่างไฟล์ ASA

ไฟล์ Global.asa อาจมีลักษณะดังนี้

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## อ้างอิง

* [ไฟล์ ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

