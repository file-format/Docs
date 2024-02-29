{
  "date": "2021-06-30",
  "keywords": [
"فایل wsf",
"فرمت فایل wsf",
"فایل wsf چیست",
"فایل",
"مثال wsf",
"پسوند فایل wsf",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Muhammad Umar"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل WSF و APIهایی که می توانند فایل های WSF را ایجاد و باز کنند، بیاموزید.",
  "title": "WSF - فایل اسکریپت ویندوز",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-faf"
}
}،
  "lastmod": "2021-06-30"
}

## فایل WSF چیست؟
فایل WSF اسکریپتی است که در دسته اجرایی قرار می گیرد و معمولاً در ویندوز مایکروسافت استفاده می شود. این اسکریپت از اختلاط چندین زبان پشتیبانی می کند، به این معنی که در فایل WSF ممکن است ترکیبی از JScript، VBScript و به صورت اختیاری برخی از عناصر XML یا زبان های برنامه نویسی دیگر مانند Python، Object REXX، Perl، Kixtart در صورت نصب توسط کاربر باشد. فایل های WSF خود را در غیاب WScript یا CScript اجرا می کنند. فایل های WSF می توانند در جداسازی خطا و افشای ثابت ها مفید باشند.

## فرمت فایل WSF
فرمت فایل WSF می تواند JScript و VBScript را از پروژه های قبلی میزبان اسکریپت ویندوز شما ترکیب کند، یک فایل wsf به شما امکان می دهد از آنها با میزبان اسکریپت ویندوز استفاده کنید. یک اسکریپت WSF مجموعه ای از توابع را در بر می گیرد که می تواند توسط فایل های مختلف WSF استفاده شود. مثال زیر یک فایل .wsf را نشان می دهد که شامل یک فایل JScript (fso.js) به اضافه یک تابع VBScript است که تابع دیگری را فراخوانی می کند.
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
فرمت WSF از ویژگی های اضافی زیر پشتیبانی می کند:
- شامل اظهارات
- موتورهای متعدد
- تایپ کتابخانه ها
- ابزار
- چندین کار در یک فایل

## مزایای فایل های WSF
فایل های WSF می توانند در زمینه های زیر مفید باشند:

### جداسازی خطا
ماهیت ماژولار فایل WSF می تواند از تداخل یک مرجع اسکریپت با مرجع دیگر جلوگیری کند که باعث می شود WSF برای جداسازی خطاها مفید باشد. در اینجا یک مثال از WSF با یک ماژول است که خطا ایجاد می کند و یکی که خطا ایجاد نمی کند:
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
### پشتیبانی از زبان ترکیبی
یک WSF از چندین زبان پشتیبانی می‌کند، شما می‌توانید از یک زبان برنامه‌نویسی کد استفاده از یک زبان برنامه‌نویسی دیگر داشته باشید. در اینجا مثالی از نحوه کار آن آورده شده است:
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
### نشان دادن ثابت ها
WSF از اتصال یک بسته بندی XML به یک مرجع یا کنترل شی پشتیبانی می کند، بنابراین شما می توانید از ثابت های آن شی به جای اینکه مجبور باشید آنها را اعلام کنید، استفاده کنید. در زیر یک مثال آمده است:
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


## منابع 

* [Windows Installer - توسط Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



