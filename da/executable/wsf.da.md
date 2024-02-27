{
  "date": "2021-06-30",
  "keywords": [
"wsf fil",
"wsf filformat",
"hvad er en wsf-fil",
"fil",
"wsf eksempel",
"wsf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WSF filformat og API'er, der kan oprette og åbne WSF filer.",
  "title": "WSF - Windows Script-fil",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-daf"
}
},
  "lastmod": "2021-06-30"
}

## Hvad er WSF fil?
En WSF-fil er et script, der falder ind under den eksekverbare kategori og almindeligvis brugt i Microsoft Windows. Scriptet understøtter blanding af flere sprog, det betyder, at WSF-filen kan indeholde en blanding af JScript, VBScript og eventuelt nogle XML-elementer eller andre scriptsprog såsom Python, Object REXX, Perl, Kixtart, hvis det er installeret af brugeren. WSF-filerne kører sig selv i fravær af WScript eller CScript. WSF-filerne kan være gavnlige til fejlisolering og eksponering af konstanter.

## WSF filformat
WSF-filformatet kan blande JScript og VBScript fra dine tidligere Windows Script Host-projekter, en .wsf-fil giver dig mulighed for at bruge dem med Windows Script Host. Et WSF-script indkapsler et bibliotek af funktioner, der kan bruges af forskellige WSF-filer. Eksemplet nedenfor viser en .wsf-fil, der indeholder en JScript-fil (fso.js), plus en VBScript-funktion, der kalder en anden funktion.
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
WSF-format understøtter følgende yderligere funktioner:
- Medtag udsagn
- Flere motorer
- Type biblioteker
- Værktøjer
- Flere job i én fil

## Fordele ved WSF-filer
WSF-filerne kan være gavnlige på følgende områder:

### Fejlisolering
Den modulære karakter af WSF-fil kan forhindre en scriptreference i at forstyrre en anden, hvilket gør WSF nyttig til at isolere fejl. Her er et eksempel på WSF med et modul, der producerer en fejl og et, der ikke gør:
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
### Understøttelse af blandet sprog
En WSF understøtter flere sprog, du kan få et scriptsprog til at bruge kode fra et andet scriptsprog. Her er et eksempel på, hvordan det fungerer:
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
### Eksponering af konstanter
WSF understøtter bindingen af en XML-indpakning til en objektreference eller kontrol, så du kan bruge objektets konstanter i stedet for at skulle erklære dem. Følgende er et eksempel:
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


## Referencer 

* [Windows Installer - af Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



