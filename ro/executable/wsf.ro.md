{
  "date" : "2021-06-30",
  "keywords" :[ "fișier wsf", "format fișier wsf", "ce este un fișier wsf", "fișier", "exemplu wsf", "extensie fișier wsf", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier WSF și despre API-urile care pot crea și deschide fișiere WSF.",
  "title" :"WSF - Fișier Script Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Ce este un fișier WSF?
Un fișier WSF este un script care se încadrează în categoria executabile și este utilizat în mod obișnuit în Microsoft Windows. Scriptul acceptă amestecarea mai multor limbi, înseamnă că în fișierul WSF poate include un amestec de JScript, VBScript și opțional unele elemente XML sau alte limbaje de scripting, cum ar fi Python, Object REXX, Perl, Kixtart dacă sunt instalate de utilizator. Fișierele WSF se execută singure în absența WScript sau CScript. Fișierele WSF pot fi benefice în izolarea erorilor și expunerea constantelor.

## Format de fișier WSF
Formatul de fișier WSF poate combina JScript și VBScript din proiectele dvs. anterioare Windows Script Host, un fișier .wsf vă permite să le utilizați cu Windows Script Host. Un script WSF încapsulează o bibliotecă de funcții care pot fi utilizate de diferite fișiere WSF. Exemplul de mai jos arată un fișier .wsf care include un fișier JScript (fso.js), plus o funcție VBScript care apelează o altă funcție.
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
Formatul WSF acceptă următoarele caracteristici suplimentare:
- Includeți declarații
- Mai multe motoare
- Biblioteci de tipări
- Unelte
- Mai multe locuri de muncă într-un singur fișier

## Beneficiile fișierelor WSF
Fișierele FSM pot fi benefice în următoarele domenii:

### Izolarea erorii
Natura modulară a fișierului WSF poate împiedica o referință de script să interfereze cu alta, ceea ce face ca WSF să fie util pentru izolarea erorilor. Iată un exemplu de WSF cu un modul care produce o eroare și unul care nu:
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
### Suport pentru limbi mixte
Un WSF acceptă mai multe limbi, puteți avea un cod de utilizare a unui limbaj de scripting dintr-un alt limbaj de scripting. Iată un exemplu despre cum funcționează:
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
### Expunerea constantelor
WSF acceptă legarea unui wrapper XML la o referință de obiect sau un control, astfel încât să puteți utiliza constantele acelui obiect în loc să trebuiască să le declarați. Mai jos este un exemplu:
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


## Referințe

* [Windows Installer - de la Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


