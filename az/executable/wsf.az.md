{
  "date": "2021-06-30",
  "keywords": [
"wsf faylı",
"wsf fayl formatı",
"wsf faylı nədir",
"fayl",
"wsf nümunəsi",
"wsf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "WSF fayl formatı və WSF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "WSF - Windows Skript Faylı",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-azf"
}
},
  "lastmod": "2021-06-30"
}

## WSF faylı nədir?
WSF faylı icra edilə bilən kateqoriyaya düşən və Microsoft Windows-da geniş istifadə olunan skriptdir. Skript bir çox dilin qarışdırılmasını dəstəkləyir, bu o deməkdir ki, WSF faylına JScript, VBScript və isteğe bağlı olaraq bəzi XML elementləri və ya istifadəçi tərəfindən quraşdırıldığı təqdirdə Python, Object REXX, Perl, Kixtart kimi digər skript dillərinin qarışığı daxil ola bilər. WSF faylları WScript və ya CScript olmadıqda özlərini icra edir. WSF faylları səhvlərin təcrid edilməsində və sabitlərin ifşasında faydalı ola bilər.

## WSF fayl formatı
WSF fayl formatı əvvəlki Windows Script Host layihələrinizdən JScript və VBScript-i qarışdıra bilər, .wsf faylı onları Windows Script Host ilə istifadə etməyə imkan verir. WSF skripti müxtəlif WSF faylları tərəfindən istifadə edilə bilən funksiyalar kitabxanasını əhatə edir. Aşağıdakı nümunədə JScript faylı (fso.js) və digər funksiyanı çağıran VBScript funksiyası olan .wsf faylı göstərilir.
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
WSF formatı aşağıdakı əlavə xüsusiyyətləri dəstəkləyir:
- Bəyanatları daxil edin
- Çoxlu mühərriklər
- Kitabxanaları yazın
- Alətlər
- Bir faylda birdən çox iş

## WSF fayllarının üstünlükləri
WSF faylları aşağıdakı sahələrdə faydalı ola bilər:

### Səhv izolyasiyası
WSF faylının modul təbiəti bir skript istinadının digərinə müdaxiləsinin qarşısını ala bilər ki, bu da WSF-ni səhvləri təcrid etmək üçün faydalı edir. Budur, bir modulu xəta yaradan və bir modulu olmayan WSF nümunəsi:
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
### Qarışıq dil dəstəyi
WSF birdən çox dili dəstəkləyir, başqa bir skript dilindən bir skript dili istifadə koduna sahib ola bilərsiniz. Bunun necə işlədiyinə dair bir nümunə:
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
### Sabitlərin ifşası
WSF XML sarğısının obyekt istinadına və ya nəzarətinə bağlanmasını dəstəkləyir ki, siz onları elan etmək əvəzinə həmin obyektin sabitlərindən istifadə edə biləsiniz. Aşağıda bir nümunə verilmişdir:
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


## İstinadlar 

* [Windows Quraşdırıcısı - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Windows_Installer)



