{
  "date" : "2021-06-30",
  "keywords" :[ "soubor wsf", "formát souboru wsf", "co je soubor wsf", "soubor", "příklad wsf", "přípona souboru wsf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů WSF a rozhraních API, která mohou vytvářet a otevírat soubory WSF.",
  "title" :"WSF - soubor skriptu Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Co je soubor WSF?
Soubor WSF je skript, který spadá do kategorie spustitelných souborů a běžně se používá v systému Microsoft Windows. Skript podporuje míchání více jazyků, to znamená, že v souboru WSF může obsahovat směs JScript, VBScript a volitelně některé prvky XML nebo jiné skriptovací jazyky, jako je Python, Object REXX, Perl, Kixtart, pokud si je uživatel nainstaloval. Soubory WSF se spouštějí samy v nepřítomnosti WScript nebo CScript. Soubory WSF mohou být užitečné při izolaci chyb a odhalení konstant.

## Formát souboru WSF
Formát souboru WSF může kombinovat JScript a VBScript z vašich předchozích projektů Windows Script Host, soubor .wsf vám umožňuje používat je s Windows Script Host. Skript WSF zapouzdřuje knihovnu funkcí, které mohou používat různé soubory WSF. Níže uvedený příklad ukazuje soubor .wsf, který obsahuje soubor JScript (fso.js), plus funkci VBScript, která volá jinou funkci.
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
Formát WSF podporuje následující dodatečné funkce:
- Zahrnout prohlášení
- Více motorů
- Knihovny typů
- Nástroje
- Více úloh v jednom souboru

## Výhody souborů WSF
Soubory WSF mohou být užitečné v následujících oblastech:

### Izolace chyb
Modulární povaha souboru WSF může zabránit tomu, aby jedna reference skriptu interferovala s jinou, což činí WSF užitečným pro izolování chyb. Zde je příklad WSF s jedním modulem, který generuje chybu, a jedním, který ne:
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
### Podpora smíšených jazyků
WSF podporuje více jazyků, můžete mít jeden skriptovací jazyk používat kód z jiného skriptovacího jazyka. Zde je příklad, jak to funguje:
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
### Odhalování konstant
WSF podporuje vazbu obálky XML na odkaz na objekt nebo ovládací prvek, takže můžete použít konstanty tohoto objektu místo toho, abyste je museli deklarovat. Následuje příklad:
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


## Reference

* [Windows Installer – od Wikipedie](https://en.wikipedia.org/wiki/Windows_Installer)


