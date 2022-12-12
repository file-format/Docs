{
  "date" : "2021-06-30",
  "keywords" :[ "wsf fájl", "wsf fájl formátum", "mi a wsf fájl", "fájl", "wsf példa", "wsf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a WSF fájlformátumról és az API-król, amelyek WSF-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WSF - Windows Script File",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Mi az a WSF fájl?
A WSF-fájl egy olyan szkript, amely a végrehajtható kategóriába tartozik, és általában a Microsoft Windows rendszerben használatos. A szkript támogatja több nyelv keverését, ami azt jelenti, hogy a WSF fájl tartalmazhat JScript, VBScript és opcionálisan néhány XML elem keverékét vagy más szkriptnyelveket, például Python, Object REXX, Perl, Kixtart, ha a felhasználó telepíti. A WSF fájlok WScript vagy CScript hiányában önmagukat hajtják végre. A WSF fájlok hasznosak lehetnek a hiba elkülönítésében és az állandók feltárásában.

## WSF fájlformátum
A WSF fájlformátum keverheti a korábbi Windows Script Host projektjeiből származó JScriptet és VBScriptet, a .wsf fájl lehetővé teszi a Windows Script Host-szal való használatát. A WSF-szkript olyan függvénykönyvtárat foglal magában, amelyet különféle WSF-fájlok használhatnak. Az alábbi példa egy .wsf fájlt mutat be, amely tartalmaz egy JScript fájlt (fso.js), valamint egy VBScript függvényt, amely egy másik függvényt hív meg.
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
A WSF formátum a következő további szolgáltatásokat támogatja:
- Tartalmazzon nyilatkozatokat
- Több motor
- Típuskönyvtárak
- Eszközök
- Több munka egy fájlban

## A WSF fájlok előnyei
A WSF fájlok a következő területeken lehetnek hasznosak:

### Hibaszigetelés
A WSF-fájl moduláris jellege megakadályozhatja, hogy az egyik szkriptreferencia megzavarja a másikat, ami hasznossá teszi a WSF-t a hibák elkülönítésére. Íme egy példa a WSF-re, amelyben az egyik modul hibát okoz, a másik pedig nem:
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
### Vegyes nyelvi támogatás
Egy WSF több nyelvet támogat, egy szkriptnyelvet használhat egy másik szkriptnyelvből. Íme egy példa a működésére:
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
### Állandók feltárása
A WSF támogatja az XML-burkolók objektumhivatkozáshoz vagy vezérlőhöz való kötését, így az objektum állandóit használhatja deklarálásuk helyett. A következő egy példa:
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


## Hivatkozások

* [Windows Installer – Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


