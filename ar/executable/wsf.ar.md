{
  "date" : "2021-06-30",
  "keywords" :["wsf file", "wsf file format", "what is a wsf file", "file", "wsf example", "wsf file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف WSF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات WSF وفتحها." ,
  "title" :"WSF - ملف Windows Script" ,
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-06-30"
}

## ما هو ملف WSF؟
ملف WSF هو برنامج نصي يندرج تحت فئة قابلة للتنفيذ ويستخدم بشكل شائع في Microsoft Windows. يدعم البرنامج النصي خلط لغات متعددة ، وهذا يعني أنه في ملف WSF قد يتضمن مزيجًا من JScript و VBScript واختيارياً بعض عناصر XML أو لغات البرمجة النصية الأخرى مثل Python و Object REXX و Perl و Kixtart إذا تم تثبيتها من قبل المستخدم. تنفذ ملفات WSF نفسها في حالة عدم وجود WScript أو CScript. يمكن أن تكون ملفات WSF مفيدة في عزل الخطأ وكشف الثوابت.

## تنسيق ملف WSF
يمكن أن يخلط تنسيق ملف WSF بين JScript و VBScript من مشاريع Windows Script Host السابقة ، ويسمح لك ملف .wsf باستخدامها مع Windows Script Host. يقوم البرنامج النصي WSF بتغليف مكتبة من الوظائف التي يمكن استخدامها بواسطة ملفات WSF المختلفة. يوضح المثال أدناه ملف .wsf يتضمن ملف JScript (fso.js) ، بالإضافة إلى وظيفة VBScript التي تستدعي وظيفة أخرى.
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
يدعم تنسيق WSF الميزات الإضافية التالية:
- تضمين البيانات
- محركات متعددة
- اكتب المكتبات
- أدوات
- وظائف متعددة في ملف واحد

## فوائد ملفات WSF
يمكن أن تكون ملفات WSF مفيدة في المجالات التالية:

### عزل الخطأ
يمكن أن تمنع الطبيعة المعيارية لملف WSF أحد مرجع البرنامج النصي من التداخل مع آخر مما يجعل WSF مفيدًا لعزل الأخطاء. فيما يلي مثال على WSF مع وحدة نمطية واحدة تنتج خطأ وأخرى لا:
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
### دعم اللغات المختلطة
يدعم WSF لغات متعددة ، يمكنك جعل لغة برمجة واحدة تستخدم رمزًا من لغة برمجة نصية أخرى. فيما يلي مثال على كيفية عمل ذلك:
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
### فضح الثوابت
يدعم WSF ربط برنامج تضمين XML بمرجع كائن أو عنصر تحكم بحيث يمكنك استخدام ثوابت هذا الكائن بدلاً من الاضطرار إلى التصريح عنها. فيما يلي مثال:
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
    dim title, str, i
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


## مراجع

* [Windows Installer - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


