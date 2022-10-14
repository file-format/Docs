{
  "date" : "2021-06-30",
  "keywords" :[ "wsf-Datei", "wsf-Dateiformat", "was ist eine wsf-Datei", "Datei", "wsf-Beispiel", "wsf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das WSF-Dateiformat und APIs, die WSF-Dateien erstellen und öffnen können.",
  "title" :"WSF - Windows-Skriptdatei",
  "linktitle" :"WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Was ist eine WSF-Datei?
Eine WSF-Datei ist ein Skript, das in die Kategorie der ausführbaren Dateien fällt und häufig in Microsoft Windows verwendet wird. Das Skript unterstützt das Mischen mehrerer Sprachen, was bedeutet, dass die WSF-Datei eine Mischung aus JScript, VBScript und optional einigen XML-Elementen oder anderen Skriptsprachen wie Python, Object REXX, Perl, Kixtart enthalten kann, wenn sie vom Benutzer installiert wurden. Die WSF-Dateien werden in Abwesenheit von WScript oder CScript selbst ausgeführt. Die WSF-Dateien können bei der Fehlerisolierung und der Offenlegung von Konstanten hilfreich sein.

## WSF-Dateiformat
Das WSF-Dateiformat kann JScript und VBScript aus Ihren früheren Windows Script Host-Projekten mischen, eine .wsf-Datei ermöglicht Ihnen die Verwendung mit Windows Script Host. Ein WSF-Skript kapselt eine Bibliothek von Funktionen, die von verschiedenen WSF-Dateien verwendet werden können. Das folgende Beispiel zeigt eine .wsf-Datei, die eine JScript-Datei (fso.js) sowie eine VBScript-Funktion enthält, die eine andere Funktion aufruft.
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
Das WSF-Format unterstützt die folgenden zusätzlichen Funktionen:
- Anweisungen einschließen
- Mehrere Motoren
- Geben Sie Bibliotheken ein
- Werkzeug
- Mehrere Jobs in einer Datei

## Vorteile von WSF-Dateien
Die WSF-Dateien können in den folgenden Bereichen hilfreich sein:

### Fehlerisolierung
Die modulare Natur der WSF-Datei kann verhindern, dass eine Skriptreferenz eine andere stört, was die WSF zum Isolieren von Fehlern nützlich macht. Hier ist ein Beispiel für WSF mit einem Modul, das einen Fehler erzeugt, und einem, das dies nicht tut:
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
### Unterstützung für gemischte Sprachen
Ein WSF unterstützt mehrere Sprachen, eine Skriptsprache kann Code aus einer anderen Skriptsprache verwenden. Hier ist ein Beispiel, wie das funktioniert:
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
### Konstanten aussetzen
Das WSF unterstützt die Bindung eines XML-Wrappers an eine Objektreferenz oder ein Steuerelement, sodass Sie die Konstanten dieses Objekts verwenden können, anstatt sie deklarieren zu müssen. Nachfolgend ein Beispiel:
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


## Verweise

* [Windows Installer – von Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


