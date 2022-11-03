{
  "date" : "2021-06-30",
  "keywords" :[ "файл wsf", "формат файла wsf", "что такое файл wsf", "файл", "пример wsf", "расширение файла wsf", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файлов WSF и API-интерфейсах, которые могут создавать и открывать файлы WSF.",
  "title" :"WSF — файл сценария Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .WSF вариант №
Файл WSF — это сценарий, который относится к категории исполняемых файлов и обычно используется в Microsoft Windows. Сценарий поддерживает смешивание нескольких языков, это означает, что в файле WSF может быть смесь JScript, VBScript и, при необходимости, некоторые элементы XML или другие языки сценариев, такие как Python, Object REXX, Perl, Kixtart, если они установлены пользователем. Файлы WSF выполняются сами по себе в отсутствие WScript или CScript. Файлы WSF могут быть полезны для изоляции ошибок и раскрытия констант.

## WSF формат файла
Формат файла WSF может смешивать JScript и VBScript из ваших предыдущих проектов Windows Script Host, файл .wsf позволяет использовать их с Windows Script Host. Сценарий WSF инкапсулирует библиотеку функций, которые могут использоваться различными файлами WSF. В приведенном ниже примере показан файл .wsf, который включает файл JScript (fso.js) и функцию VBScript, которая вызывает другую функцию.
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
Формат WSF поддерживает следующие дополнительные функции:
- Включить заявления
- Несколько двигателей
- Библиотеки типов
- Инструменты
- Несколько заданий в одном файле

## Преимущества файлов WSF
Файлы WSF могут быть полезны в следующих областях:

### Изоляция ошибок
Модульная природа файла WSF может предотвратить взаимодействие одной ссылки сценария с другой, что делает WSF полезным для изоляции ошибок. Вот пример WSF с одним модулем, который выдает ошибку, и другим, который этого не делает:
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
### Поддержка смешанных языков
WSF поддерживает несколько языков, вы можете использовать код одного языка сценариев из другого языка сценариев. Вот пример того, как это работает:
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
### Предоставление констант
WSF поддерживает привязку XML-оболочки к объектной ссылке или элементу управления, поэтому вы можете использовать константы этого объекта вместо их объявления. Ниже приведен пример:
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


## использованная литература

* [Установщик Windows — из Википедии] (https://en.wikipedia.org/wiki/Windows_Installer)


