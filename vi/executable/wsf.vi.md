{
  "date" : "2021-06-30",
  "keywords" :[ "tệp wsf", "định dạng tệp wsf", "tệp wsf là gì", "tệp", "ví dụ wsf", "phần mở rộng tệp wsf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp WSF và API có thể tạo và mở tệp WSF.",
  "title" :"WSF - Tệp tập lệnh Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Tệp WSF là gì?
Tệp WSF là một tập lệnh thuộc danh mục có thể thực thi và thường được sử dụng trong Microsoft Windows. Tập lệnh hỗ trợ trộn nhiều ngôn ngữ, điều đó có nghĩa là trong tệp WSF có thể bao gồm sự pha trộn của JScript, VBScript và tùy chọn một số phần tử XML hoặc các ngôn ngữ tập lệnh khác như Python, Object REXX, Perl, Kixtart nếu người dùng cài đặt. Các tệp WSF tự thực thi khi không có WScript hoặc CScript. Các tệp WSF có thể hữu ích trong việc cách ly lỗi và hiển thị các hằng số.

## Định dạng tệp WSF
Định dạng tệp WSF có thể kết hợp JScript và VBScript từ các dự án Windows Script Host trước đây của bạn, tệp .wsf cho phép bạn sử dụng chúng với Windows Script Host. Tập lệnh WSF đóng gói một thư viện các chức năng có thể được sử dụng bởi các tệp WSF khác nhau. Ví dụ bên dưới hiển thị tệp .wsf bao gồm tệp JScript (fso.js), cùng với hàm VBScript gọi hàm khác.
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
Định dạng WSF hỗ trợ các tính năng bổ sung sau:
- Bao gồm các tuyên bố
- Nhiều động cơ
- Loại thư viện
- Công cụ
- Nhiều công việc trong một tập tin

## Lợi ích của tệp WSF
Các tệp WSF có thể hữu ích trong các lĩnh vực sau:

### Cách ly lỗi
Bản chất mô-đun của tệp WSF có thể ngăn một tham chiếu tập lệnh can thiệp vào tập lệnh khác, điều này làm cho WSF hữu ích để cô lập các lỗi. Dưới đây là một ví dụ về WSF với một mô-đun tạo ra lỗi và một mô-đun không:
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
### Hỗ trợ ngôn ngữ hỗn hợp
Một WSF hỗ trợ nhiều ngôn ngữ, bạn có thể có một ngôn ngữ kịch bản sử dụng mã từ một ngôn ngữ kịch bản khác. Đây là một ví dụ về cách thức hoạt động:
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
### Hiển thị hằng số
WSF hỗ trợ liên kết một trình bao bọc XML với một tham chiếu hoặc điều khiển đối tượng để bạn có thể sử dụng các hằng số của đối tượng đó thay vì phải khai báo chúng. Sau đây là một ví dụ:
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


## Người giới thiệu

* [Trình cài đặt Windows - theo Wikipedia](https://vi.wikipedia.org/wiki/Windows_Installer)


