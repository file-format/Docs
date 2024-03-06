{
  "date": "2021-06-30",
  "keywords": [
"wsf failu",
"wsf faila formātā",
"kas ir wsf fails",
"failu",
"wsf piemērs",
"wsf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WSF faila formātu un API, kas var izveidot un atvērt WSF failus.",
  "title": "WSF — Windows skripta fails",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-lvf"
}
},
  "lastmod": "2021-06-30"
}

## Kas ir WSF fails?
WSF fails ir skripts, kas ietilpst izpildāmo failu kategorijā un parasti tiek izmantots operētājsistēmā Microsoft Windows. Skripts atbalsta vairāku valodu sajaukšanu, tas nozīmē, ka WSF failā var būt JScript, VBScript un pēc izvēles daži XML elementi vai citas skriptu valodas, piemēram, Python, Object REXX, Perl, Kixtart, ja lietotājs to ir instalējis. WSF faili tiek izpildīti paši, ja nav WScript vai CScript. WSF faili var būt noderīgi kļūdu izolācijā un konstantu atklāšanā.

## WSF faila formāts
WSF faila formāts var sajaukt JScript un VBScript no jūsu iepriekšējiem Windows Script Host projektiem, .wsf fails ļauj tos izmantot kopā ar Windows Script Host. WSF skripts iekapsulē funkciju bibliotēku, ko var izmantot dažādi WSF faili. Tālāk esošajā piemērā ir parādīts .wsf fails, kas ietver JScript failu (fso.js), kā arī VBScript funkciju, kas izsauc citu funkciju.
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
WSF formāts atbalsta šādas papildu funkcijas:
- Iekļaujiet paziņojumus
- Vairāki dzinēji
- Tipu bibliotēkas
- Instrumenti
- Vairāki darbi vienā failā

## WSF failu priekšrocības
WSF faili var būt noderīgi šādās jomās:

### Kļūdu izolācija
WSF faila modulārais raksturs neļauj vienai skripta atsaucei traucēt citai, kas padara WSF noderīgu kļūdu izolēšanai. Šeit ir WSF piemērs ar vienu moduli, kas rada kļūdu, un vienu, kas nerada kļūdu:
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
### Jauktu valodu atbalsts
WSF atbalsta vairākas valodas, varat izmantot vienu skriptu valodas kodu no citas skriptu valodas. Šeit ir piemērs, kā tas darbojas:
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
### Konstantes eksponēšana
WSF atbalsta XML iesaiņojuma saistīšanu ar objekta atsauci vai vadīklu, lai jūs varētu izmantot šī objekta konstantes, nevis tās deklarēt. Tālāk ir sniegts piemērs:
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


## Atsauces 

* [Windows Installer — Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



