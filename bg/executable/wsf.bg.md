{
  "date" : "2021-06-30",
  "keywords" :[ "wsf файл", "wsf файлов формат", "какво е wsf файл", "файл", "wsf пример", "wsf файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за WSF файловия формат и API, които могат да създават и отварят WSF файлове.",
  "title" :"WSF - Windows скрипт файл",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Какво е WSF файл?
WSF файлът е скрипт, който попада в категорията на изпълними файлове и често се използва в Microsoft Windows. Скриптът поддържа смесване на множество езици, което означава, че WSF файлът може да включва комбинация от JScript, VBScript и по избор някои XML елементи или други скриптови езици като Python, Object REXX, Perl, Kixtart, ако са инсталирани от потребителя. WSF файловете се изпълняват сами при липса на WScript или CScript. WSF файловете могат да бъдат полезни при изолиране на грешки и излагане на константи.

## WSF файлов формат
Файловият формат WSF може да смесва JScript и VBScript от вашите предишни проекти за Windows Script Host, .wsf файл ви позволява да ги използвате с Windows Script Host. WSF скрипт капсулира библиотека от функции, които могат да се използват от различни WSF файлове. Примерът по-долу показва .wsf файл, който включва JScript файл (fso.js), плюс VBScript функция, която извиква друга функция.
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
WSF форматът поддържа следните допълнителни функции:
- Включете изявления
- Множество двигатели
- Типови библиотеки
- Инструменти
- Няколко работни места в един файл

## Предимства на WSF файловете
WSF файловете могат да бъдат полезни в следните области:

### Изолиране на грешки
Модулният характер на WSF файла може да попречи на една препратка към скрипт да пречи на друга, което прави WSF полезен за изолиране на грешки. Ето пример за WSF с един модул, който генерира грешка и един, който не:
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
### Поддръжка на смесени езици
WSF поддържа множество езици, можете да накарате един скриптов език да използва код от друг скриптов език. Ето пример как работи това:
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
### Излагане на константи
WSF поддържа обвързването на XML обвивка към препратка към обект или контрола, така че можете да използвате константите на този обект, вместо да се налага да ги декларирате. Следва пример:
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


## Препратки

* [Windows Installer - от Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


