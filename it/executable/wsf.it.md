{
  "date" : "2021-06-30",
  "keywords" :[ "file wsf", "formato file wsf", "cos'è un file wsf", "file", "esempio wsf", "estensione file wsf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file WSF e le API che possono creare e aprire file WSF.",
  "title" :"WSF - File script di Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Che cos'è un file WSF?
Un file WSF è uno script che rientra nella categoria eseguibile e comunemente utilizzato in Microsoft Windows. Lo script supporta la combinazione di più linguaggi, significa che nel file WSF può includere una miscela di JScript, VBScript e opzionalmente alcuni elementi XML o altri linguaggi di scripting come Python, Object REXX, Perl, Kixtart se installati dall'utente. I file WSF vengono eseguiti da soli in assenza di WScript o CScript. I file WSF possono essere utili per l'isolamento degli errori e l'esposizione di costanti.

## Formato file WSF
Il formato di file WSF può combinare JScript e VBScript dai precedenti progetti di Windows Script Host, un file .wsf consente di utilizzarli con Windows Script Host. Uno script WSF incapsula una libreria di funzioni che possono essere utilizzate da vari file WSF. L'esempio seguente mostra un file .wsf che include un file JScript (fso.js), più una funzione VBScript che chiama un'altra funzione.
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
Il formato WSF supporta le seguenti funzionalità aggiuntive:
- Includere dichiarazioni
- Motori multipli
- Librerie di tipi
- Strumenti
- Più lavori in un file

## Vantaggi dei file WSF
I file WSF possono essere utili nelle seguenti aree:

### Isolamento degli errori
La natura modulare del file WSF può impedire a un riferimento di script di interferire con un altro, il che rende il file WSF utile per isolare gli errori. Ecco un esempio di WSF con un modulo che produce un errore e uno che non lo fa:
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
### Supporto per lingue miste
Un WSF supporta più linguaggi, puoi fare in modo che un linguaggio di scripting utilizzi il codice di un altro linguaggio di scripting. Ecco un esempio di come funziona:
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
### Esporre le costanti
Il WSF supporta l'associazione di un wrapper XML a un riferimento o controllo di un oggetto in modo da poter utilizzare le costanti di quell'oggetto invece di doverle dichiarare. Di seguito è riportato un esempio:
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


## Riferimenti

* [Windows Installer - di Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


