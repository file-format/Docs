{
  "date" : "2021-06-30",
  "keywords" :[ "wsf 文件", "wsf 文件格式", "什么是 wsf 文件", "文件", "wsf 示例", "wsf 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 WSF 文件格式和可创建和打开 WSF 文件的 API。",
  "title" :"WSF - Windows 脚本文件",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## 什么是一 .wsf 文件？
WSF 文件是属于可执行类别的脚本，通常在 Microsoft Windows 中使用。该脚本支持多种语言的混合，这意味着在 WSF 文件中可能包含 JScript、VBScript 和可选的一些 XML 元素或其他脚本语言，如 Python、Object REXX、Perl、Kixtart（如果用户安装）的混合。 WSF 文件在没有 WScript 或 CScript 的情况下自行执行。 WSF 文件有助于错误隔离和公开常量。

## WSF 文件格式
WSF 文件格式可以混合您以前的 Windows 脚本宿主项目中的 JScript 和 VBScript，.wsf 文件允许您将它们与 Windows 脚本宿主一起使用。 WSF 脚本封装了可供各种 WSF 文件使用的函数库。下面的示例显示了一个 .wsf 文件，其中包括一个 JScript 文件 (fso.js)，以及一个调用另一个函数的 VBScript 函数。
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
WSF 格式支持以下附加功能：
- 包括语句
- 多个引擎
- 类型库
- 工具
- 一个文件中的多个作业

## WSF 文件的优点
WSF 文件可在以下领域中发挥作用：

### 错误隔离
WSF 文件的模块化特性可以防止一个脚本引用干扰另一个脚本引用，这使得 WSF 可用于隔离错误。下面是一个 WSF 示例，其中一个模块产生错误，一个模块不产生错误：
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
### 混合语言支持
WSF 支持多种语言，您可以让一种脚本语言使用另一种脚本语言的代码。这是一个如何工作的示例：
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
### 暴露常量
WSF 支持将 XML 包装器绑定到对象引用或控件，因此您可以使用该对象的常量而不必声明它们。下面是一个例子：
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


## 参考

* [Windows 安装程序 - 维基百科提供](https://en.wikipedia.org/wiki/Windows_Installer)


