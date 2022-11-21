{
  "date" : "2021-06-30",
  "keywords" :[ "ไฟล์ wsf", "รูปแบบไฟล์ wsf", "ไฟล์ wsf คืออะไร", "ไฟล์", "ตัวอย่าง wsf", "นามสกุลไฟล์ wsf","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WSF และ API ที่สามารถสร้างและเปิดไฟล์ WSF",
  "title" :"WSF - ไฟล์สคริปต์ Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## ไฟล์ WSF คืออะไร??
ไฟล์ WSF เป็นสคริปต์ที่อยู่ในหมวดหมู่ปฏิบัติการและใช้กันทั่วไปใน Microsoft Windows สคริปต์รองรับการผสมหลายภาษา หมายความว่าในไฟล์ WSF อาจรวม JScript, VBScript และองค์ประกอบ XML หรือภาษาสคริปต์อื่นๆ เช่น Python, Object REXX, Perl, Kixtart หากติดตั้งโดยผู้ใช้ ไฟล์ WSF ดำเนินการเองโดยไม่มี WScript หรือ CScript ไฟล์ WSF สามารถเป็นประโยชน์ในการแยกข้อผิดพลาดและเปิดเผยค่าคงที่

## รูปแบบไฟล์ WSF
รูปแบบไฟล์ WSF สามารถผสม JScript และ VBScript จากโครงการ Windows Script Host ก่อนหน้าของคุณ ไฟล์ .wsf ช่วยให้คุณใช้กับ Windows Script Host ได้ สคริปต์ WSF สรุปไลบรารีของฟังก์ชันที่ไฟล์ WSF ต่างๆ สามารถใช้ได้ ตัวอย่างด้านล่างแสดงไฟล์ .wsf ที่มีไฟล์ JScript (fso.js) บวกกับฟังก์ชัน VBScript ที่เรียกใช้ฟังก์ชันอื่น
```
<job id="IncludeExample">
   <script language="JScript" src="FSO.JS"/>
   <script language="VBScript">
      ' Get the free space for drive C.
      s = GetFreeSpace("c:")
      WScript.Echo s
   <script>
</job>
```
รูปแบบ WSF รองรับคุณสมบัติเพิ่มเติมต่อไปนี้:
- รวมงบ
- เครื่องยนต์หลายตัว
- ห้องสมุดประเภท
- เครื่องมือ
- หลายงานในไฟล์เดียว

## ประโยชน์ของไฟล์ WSF
ไฟล์ WSF มีประโยชน์ในด้านต่อไปนี้:

### การแยกข้อผิดพลาด
ลักษณะโมดูลาร์ของไฟล์ WSF สามารถป้องกันการอ้างอิงสคริปต์หนึ่งไม่ให้รบกวนการอ้างอิงอื่น ซึ่งทำให้ WSF มีประโยชน์ในการแยกข้อผิดพลาด นี่คือตัวอย่างของ WSF ที่มีหนึ่งโมดูลที่สร้างข้อผิดพลาดและอีกโมดูลที่ไม่มี:
```
<?xml version="1.0" ?>
 <job id="Partially works">
   <!-- This will not work -->
   <script language="VBScript">
'    <![CDATA[
         WScript.echo 4/0 ' Oh, boy! You cannot divide by zero...
     ]]>
   </script>
   <!-- This will work... definitely... -->
   <script language="VBScript">
     <![CDATA[
         WScript.echo "Hello, Scripters!" & vbNewline & _
                      "Fantastic! It worked!"
'    ]]>
   </script>
 </job>
```
### รองรับภาษาผสม
WSF รองรับหลายภาษา คุณสามารถใช้รหัสภาษาสคริปต์หนึ่งภาษาจากภาษาสคริปต์อื่นได้ นี่คือตัวอย่างวิธีการทำงาน:
```
<?xml version="1.0" ?>
<!-- Mixing JScript and VBScript -->
 <job id="SORT-VBScriptWithJScript">
   <script language="JScript">
     function SortVBArray(arrVBArray) {return arrVBArray.toArray().sort();}
   </script>
   <script language="VBScript">
'    <![CDATA[
     '** Fastest sort: call the Jscript sort from VBScript
     myData = "a,b,c,1,2,3,X,Y,Z,p,d,q"
     wscript.echo "Original List of values: " & vbTab & myData
     starttime = timer()
     sortedArray = SortVBArray(split(myData,","))
     endtime=timer()
     jscriptTime = round(endtime-starttime,2)
     wscript.echo "JScript sorted in " & jscriptTime & " seconds: "  & vbTab & sortedArray
'    ]]>
   </script>
 </job>
```
### การเปิดเผยค่าคงที่
WSF รองรับการผูก XML wrapper กับการอ้างอิงวัตถุหรือการควบคุม ดังนั้นคุณจึงสามารถใช้ค่าคงที่ของวัตถุนั้นแทนการประกาศ ต่อไปนี้เป็นตัวอย่าง:
```
<?xml version="1.0" ?>
<!-- WSF Example with Object Reference
Notes for this very formal example:
 CDATA is used to help the XML parser ignore 
 special characters in the content of the script.  
 The CDATA open and close must be masked 
 from VBScript by making them comments.
-->
<package>
 <job id="EnumerateConstantsADO">
  <reference object="ADODB.Recordset" />
  <script language="VBScript">
'  <![CDATA[
    dim title, str, i,
    ctecArray = Array("adOpenUnspecified","adOpenForwardOnly", _
                      "adOpenKeyset","adOpenDynamic","adOpenStatic")
    title = "ADO Recordset Values for Constants"
    str = title & vbNewLine & vbNewLine
    str = str & "*CursorTypeEnum Constants*" & vbNewLine
    For i = 0 to ubound(ctecArray)
      str = str & Eval(ctecArray(i)) & vbTab & ctecArray(i) & vbNewLine
    Next
    str = str & vbNewLine
    str = str & "*LockTypeEnum Constants*" & vbNewLine
    ltecArray = Array("adLockUnspecified","adLockReadOnly", _
                      "adLockPessimistic","adLockOptimistic", _
                      "adLockBatchOptimistic")
    For i = 0 to ubound(ltecArray)
      str = str & Eval(ltecArray(i)) & vbTab & ltecArray(i) & vbNewLine
    Next
    MsgBox str, vbInformation, Title
'  ]]>
  </script>
 </job>
</package>
```


## อ้างอิง

* [ตัวติดตั้ง Windows - โดย Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


