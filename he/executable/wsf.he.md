{
  "date" : "2021-06-30",
  "keywords" :[ "קובץ wsf", "פורמט קובץ wsf", "מהו קובץ wsf", "קובץ", "דוגמה ל-wsf", "סיומת קובץ wsf","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ WSF וממשקי API שיכולים ליצור ולפתוח קובצי WSF.",
  "title" :"WSF - קובץ סקריפט של Windows",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## מהו קובץ WSF?
קובץ WSF הוא סקריפט שנכלל תחת קטגוריית ההפעלה ונמצא בשימוש נפוץ ב-Microsoft Windows. הסקריפט תומך בערבוב של שפות מרובות, זה אומר שבקובץ WSF עשוי לכלול שילוב של JScript, VBScript ובאופן אופציונלי כמה אלמנטים של XML או שפות סקריפט אחרות כגון Python, Object REXX, Perl, Kixtart אם הותקנה על ידי המשתמש. קובצי WSF מבצעים את עצמם בהיעדר WScript או CScript. קבצי WSF יכולים להועיל בבידוד שגיאות וחשיפת קבועים.

## פורמט קובץ WSF
פורמט הקובץ WSF יכול לערבב את JScript ו-VBScript מפרויקטים קודמים של Windows Script Host Host, קובץ .wsf מאפשר לך להשתמש בהם עם Windows Script Host. סקריפט WSF מקפל ספריית פונקציות שניתן להשתמש בהן על ידי קבצי WSF שונים. הדוגמה שלהלן מציגה קובץ .wsf הכולל קובץ JScript (fso.js), בתוספת פונקציית VBScript הקוראת לפונקציה אחרת.
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
פורמט WSF תומך בתכונות הנוספות הבאות:
- כלול הצהרות
- מספר מנועים
- סוג ספריות
- כלים
- מספר עבודות בקובץ אחד

## היתרונות של קבצי WSF
קבצי WSF יכולים להיות מועילים בתחומים הבאים:

### בידוד שגיאה
האופי המודולרי של קובץ WSF יכול למנוע מהפניה לסקריפט אחד להפריע לאחר, מה שהופך את ה-WSF לשימושי לבידוד שגיאות. הנה דוגמה של WSF עם מודול אחד שמייצר שגיאה ואחד שלא:
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
### תמיכה בשפה מעורבת
WSF תומך במספר שפות, אתה יכול להשתמש בקוד של שפת סקריפט אחת משפת סקריפט אחרת. הנה דוגמה איך זה עובד:
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
### חשיפת קבועים
ה-WSF תומך בקשירה של מעטפת XML להפניה או פקד לאובייקט, כך שתוכל להשתמש בקבועים של אובייקט זה במקום להכריז עליהם. להלן דוגמה:
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


## הפניות

* [Windows Installer - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Windows_Installer)


