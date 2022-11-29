{
  "date" : "2021-06-30",
  "keywords" :[ "wsf fil", "wsf filformat", "vad är en wsf fil", "fil", "wsf exempel", "wsf filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om WSF-filformat och API:er som kan skapa och öppna WSF-filer.",
  "title" :"WSF - Windows Script File",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Vad är WSF fil?
En WSF-fil är ett skript som faller under den körbara kategorin och som vanligtvis används i Microsoft Windows. Skriptet stöder blandning av flera språk, det betyder att WSF-filen kan innehålla en blandning av JScript, VBScript och eventuellt några XML-element eller andra skriptspråk som Python, Object REXX, Perl, Kixtart om de installeras av användaren. WSF-filerna körs själva i frånvaro av WScript eller CScript. WSF-filerna kan vara fördelaktiga för felisolering och exponering av konstanter.

## WSF filformat
WSF-filformatet kan blanda JScript och VBScript från dina tidigare Windows Script Host-projekt, en .wsf-fil låter dig använda dem med Windows Script Host. Ett WSF-skript kapslar in ett bibliotek med funktioner som kan användas av olika WSF-filer. Exemplet nedan visar en .wsf-fil som innehåller en JScript-fil (fso.js), plus en VBScript-funktion som anropar en annan funktion.
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
WSF-formatet stöder följande ytterligare funktioner:
- Inkludera påståenden
- Flera motorer
- Typ bibliotek
- Verktyg
- Flera jobb i en fil

## Fördelar med WSF-filer
WSF-filerna kan vara till nytta inom följande områden:

### Felisolering
Den modulära karaktären hos WSF-filen kan förhindra en skriptreferens från att störa en annan, vilket gör WSF användbart för att isolera fel. Här är ett exempel på WSF med en modul som ger ett fel och en som inte gör det:
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
### Stöd för blandade språk
En WSF stöder flera språk, du kan använda kod för ett skriptspråk från ett annat skriptspråk. Här är ett exempel på hur det fungerar:
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
### Exponera konstanter
WSF stöder bindningen av ett XML-omslag till en objektreferens eller kontroll så att du kan använda objektets konstanter istället för att behöva deklarera dem. Följande är ett exempel:
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


## Referenser

* [Windows Installer - av Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


