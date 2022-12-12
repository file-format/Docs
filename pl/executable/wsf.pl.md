{
  "date" : "2021-06-30",
  "keywords" :["plik wsf", "format pliku wsf", "co to jest plik wsf", "plik", "przykład wsf", "rozszerzenie pliku wsf","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików WSF i interfejsy API, które mogą tworzyć i otwierać pliki WSF.",
  "title" :"WSF - plik skryptu systemu Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Czym jest plik WFS?
Plik WSF to skrypt należący do kategorii plików wykonywalnych i powszechnie używany w systemie Microsoft Windows. Skrypt obsługuje mieszanie wielu języków, co oznacza, że plik WSF może zawierać mieszankę JScript, VBScript i opcjonalnie niektóre elementy XML lub inne języki skryptowe, takie jak Python, Object REXX, Perl, Kixtart, jeśli zostały zainstalowane przez użytkownika. Pliki WSF wykonują się same przy braku WScript lub CScript. Pliki WSF mogą być przydatne w izolacji błędów i ujawnianiu stałych.

## Format pliku WSF
Format pliku WSF może łączyć skrypty JScript i VBScript z poprzednich projektów hosta skryptów systemu Windows, a plik .wsf umożliwia ich używanie z hostem skryptów systemu Windows. Skrypt WSF zawiera bibliotekę funkcji, które mogą być używane przez różne pliki WSF. Poniższy przykład pokazuje plik .wsf, który zawiera plik JScript (fso.js) oraz funkcję VBScript, która wywołuje inną funkcję.
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
Format WSF obsługuje następujące dodatkowe funkcje:
- Dołącz oświadczenia
- Wiele silników
- Biblioteki typów
- Narzędzia
- Wiele zadań w jednym pliku

## Korzyści z plików WSF
Pliki WSF mogą być korzystne w następujących obszarach:

### Izolacja błędów
Modułowy charakter pliku WSF może zapobiegać zakłóceniom jednego skryptu z innym, co sprawia, że WSF jest przydatny do izolowania błędów. Oto przykład WSF z jednym modułem, który generuje błąd, i jednym, który nie:
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
### Obsługa różnych języków
WSF obsługuje wiele języków, możesz mieć jeden język skryptowy używający kodu z innego języka skryptowego. Oto przykład, jak to działa:
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
### Ujawnianie stałych
WSF obsługuje powiązanie opakowania XML z odwołaniem do obiektu lub kontrolką, dzięki czemu można używać stałych tego obiektu zamiast konieczności ich deklarowania. Oto przykład:
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


## Bibliografia

* [Instalator Windows — z Wikipedii](https://en.wikipedia.org/wiki/Windows_Installer)


