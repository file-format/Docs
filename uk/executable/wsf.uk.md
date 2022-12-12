{
  "date" : "2021-06-30",
  "keywords" :[ "файл wsf", "формат файлу wsf", "що таке файл wsf", "файл", "приклад wsf", "розширення файлу wsf", "розширення", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу WSF та API, які можуть створювати та відкривати файли WSF.",
  "title" :"WSF - файл сценарію Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Що таке файл WSF?
Файл WSF — це сценарій, який відноситься до категорії виконуваних файлів і зазвичай використовується в Microsoft Windows. Сценарій підтримує змішування кількох мов, це означає, що файл WSF може включати суміш JScript, VBScript і, за бажанням, деякі елементи XML або інші мови сценаріїв, такі як Python, Object REXX, Perl, Kixtart, якщо встановлено користувачем. Файли WSF виконуються самостійно за відсутності WScript або CScript. Файли WSF можуть бути корисними для ізоляції помилок і виявлення констант.

## Формат файлу WSF
Формат файлу WSF може змішувати JScript і VBScript з ваших попередніх проектів Windows Script Host, файл .wsf дозволяє використовувати їх із Windows Script Host. Сценарій WSF інкапсулює бібліотеку функцій, які можуть використовуватися різними файлами WSF. У прикладі нижче показано файл .wsf, який містить файл JScript (fso.js), а також функцію VBScript, яка викликає іншу функцію.
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
Формат WSF підтримує такі додаткові функції:
- Додайте заяви
- Кілька двигунів
- Бібліотеки типів
- Інструменти
- Кілька завдань в одному файлі

## Переваги файлів WSF
Файли WSF можуть бути корисними в таких сферах:

### Ізоляція помилок
Модульна природа файлу WSF може запобігти перешкоджанню одного посилання на сценарій іншому, що робить WSF корисним для ізоляції помилок. Ось приклад WSF з одним модулем, який створює помилку, і одним, який не викликає:
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
### Підтримка змішаних мов
WSF підтримує кілька мов, ви можете мати в одній мові сценаріїв код з іншої мови сценаріїв. Ось приклад того, як це працює:
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
### Викриття констант
WSF підтримує прив’язку обгортки XML до посилання на об’єкт або елемент керування, щоб ви могли використовувати константи цього об’єкта замість того, щоб їх оголошувати. Ось приклад:
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


## Список літератури

* [Інсталятор Windows - від Вікіпедії](https://en.wikipedia.org/wiki/Windows_Installer)


