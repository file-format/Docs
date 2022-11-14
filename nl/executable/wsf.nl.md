{
  "date" : "2021-06-30",
  "keywords" :[ "wsf-bestand", "wsf-bestandsformaat", "wat is een wsf-bestand", "bestand", "wsf-voorbeeld", "wsf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over WSF-bestandsindeling en API's die WSF-bestanden kunnen maken en openen.",
  "title" :"WSF - Windows-scriptbestand",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Wat is een WSF-bestand?
Een WSF-bestand is een script dat onder de categorie uitvoerbaar valt en veel wordt gebruikt in Microsoft Windows. Het script ondersteunt het mengen van meerdere talen, dit betekent dat het WSF-bestand een mix van JScript, VBScript en optioneel enkele XML-elementen of andere scripttalen zoals Python, Object REXX, Perl, Kixtart kan bevatten, indien geïnstalleerd door de gebruiker. De WSF-bestanden voeren zichzelf uit in afwezigheid van WScript of CScript. De WSF-bestanden kunnen nuttig zijn bij het isoleren van fouten en het blootleggen van constanten.

## WSF-bestandsindeling
Het WSF-bestandsformaat kan de JScript en VBScript van uw eerdere Windows Script Host-projecten combineren, een .wsf-bestand stelt u in staat om ze te gebruiken met Windows Script Host. Een WSF-script omvat een bibliotheek met functies die door verschillende WSF-bestanden kunnen worden gebruikt. Het onderstaande voorbeeld toont een .wsf-bestand dat een JScript-bestand (fso.js) bevat, plus een VBScript-functie die een andere functie aanroept.
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
WSF-formaat ondersteunt de volgende extra functies:
- Uitspraken opnemen
- Meerdere motoren
- Typ bibliotheken
- Hulpmiddelen
- Meerdere taken in één bestand

## Voordelen van WSF-bestanden
De WSF-bestanden kunnen nuttig zijn op de volgende gebieden:

### Foutisolatie
Het modulaire karakter van het WSF-bestand kan voorkomen dat de ene scriptverwijzing de andere verstoort, wat de WSF nuttig maakt voor het isoleren van fouten. Hier is een voorbeeld van WSF met één module die een fout produceert en één die dat niet doet:
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
### Ondersteuning voor gemengde talen
Een WSF ondersteunt meerdere talen, u kunt een scripttaal code uit een andere scripttaal laten gebruiken. Hier is een voorbeeld van hoe dat werkt:
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
### Constanten blootleggen
De WSF ondersteunt de binding van een XML-wrapper aan een objectreferentie of -besturingselement, zodat u de constanten van dat object kunt gebruiken in plaats van ze te moeten declareren. Hieronder volgt een voorbeeld:
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


## Referenties

* [Windows Installer - door Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


