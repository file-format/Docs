{
  "date": "2021-06-30",
  "keywords": [
"wsf failą",
"wsf failo formatas",
"kas yra wsf failas",
"failą",
"wsf pavyzdys",
"wsf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WSF failo formatą ir API, kurios gali kurti ir atidaryti WSF failus.",
  "title": "WSF – „Windows“ scenarijaus failas",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-ltf"
}
},
  "lastmod": "2021-06-30"
}

## Kas yra WSF failas?
WSF failas yra scenarijus, kuris patenka į vykdomųjų kategoriją ir dažniausiai naudojamas Microsoft Windows. Scenarijus palaiko kelių kalbų maišymą, tai reiškia, kad WSF faile gali būti JScript, VBScript ir pasirinktinai kai kurių XML elementų arba kitų scenarijų kalbų, tokių kaip Python, Object REXX, Perl, Kixtart, derinys, jei jas įdiegė vartotojas. WSF failai paleidžiami patys, jei nėra WScript arba CScript. WSF failai gali būti naudingi išskiriant klaidas ir atskleidžiant konstantas.

## WSF failo formatas
WSF failo formatas gali maišyti JScript ir VBScript iš ankstesnių Windows Script Host projektų, .wsf failas leidžia juos naudoti su Windows Script Host. WSF scenarijus apima funkcijų, kurias gali naudoti įvairūs WSF failai, biblioteką. Toliau pateiktame pavyzdyje parodytas .wsf failas, kuriame yra JScript failas (fso.js) ir VBScript funkcija, kuri iškviečia kitą funkciją.
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
WSF formatas palaiko šias papildomas funkcijas:
- Įtraukite pareiškimus
- Keli varikliai
- Tipų bibliotekos
- Įrankiai
- Keli darbai viename faile

## WSF failų pranašumai
WSF failai gali būti naudingi šiose srityse:

### Klaidų izoliavimas
Modulinis WSF failo pobūdis gali neleisti vienai scenarijaus nuorodai trukdyti kitai, todėl WSF naudinga atskiriant klaidas. Štai WSF pavyzdys su vienu moduliu, kuris sukuria klaidą, o kitą - ne:
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
### Mišrių kalbų palaikymas
WSF palaiko kelias kalbas, galite turėti vieną scenarijų kalbos kodą iš kitos scenarijų kalbos. Štai pavyzdys, kaip tai veikia:
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
### Konstantų atskleidimas
WSF palaiko XML paketo susiejimą su objekto nuoroda arba valdikliu, kad galėtumėte naudoti to objekto konstantas, o ne jas deklaruoti. Toliau pateikiamas pavyzdys:
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


## Nuorodos 

* [Windows Installer – Vikipedija](https://en.wikipedia.org/wiki/Windows_Installer)



