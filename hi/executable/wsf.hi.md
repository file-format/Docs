{
  "date" : "2021-06-30",
  "keywords" :[ "डब्ल्यूएसएफ फाइल", "डब्ल्यूएसएफ फाइल फॉर्मेट", "डब्ल्यूएसएफ फाइल क्या है", "फाइल", "डब्ल्यूएसएफ उदाहरण", "डब्ल्यूएसएफ फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSF फ़ाइल स्वरूप और API के बारे में जानें जो WSF फ़ाइलें बना और खोल सकते हैं।",
  "title" :"डब्ल्यूएसएफ - विंडोज स्क्रिप्ट फाइल",
  "linktitle" : "WSF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## डब्ल्यूएसएफ फाइल क्या है?
WSF फ़ाइल एक स्क्रिप्ट है जो निष्पादन योग्य श्रेणी के अंतर्गत आती है और आमतौर पर Microsoft Windows में उपयोग की जाती है। स्क्रिप्ट कई भाषाओं के मिश्रण का समर्थन करती है, इसका मतलब है कि WSF फ़ाइल में JScript, VBScript और वैकल्पिक रूप से कुछ XML तत्वों या अन्य स्क्रिप्टिंग भाषाओं जैसे कि Python, Object REXX, Perl, Kixtart का मिश्रण शामिल हो सकता है यदि उपयोगकर्ता द्वारा स्थापित किया गया हो। WSF फाइलें WScript या CScript की अनुपस्थिति में खुद को निष्पादित करती हैं। WSF फाइलें त्रुटि अलगाव और स्थिरांक को उजागर करने में फायदेमंद हो सकती हैं।

## डब्ल्यूएसएफ फ़ाइल प्रारूप
WSF फ़ाइल स्वरूप आपके पिछले Windows स्क्रिप्ट होस्ट प्रोजेक्ट से JScript और VBScript को मिला सकता है, एक .wsf फ़ाइल आपको उन्हें Windows स्क्रिप्ट होस्ट के साथ उपयोग करने की अनुमति देती है। WSF स्क्रिप्ट फ़ंक्शंस की एक लाइब्रेरी को इनकैप्सुलेट करती है जिसका उपयोग विभिन्न WSF फ़ाइलों द्वारा किया जा सकता है। नीचे दिया गया उदाहरण एक .wsf फ़ाइल दिखाता है जिसमें एक JScript फ़ाइल (fso.js) शामिल है, साथ ही एक VBScript फ़ंक्शन जो किसी अन्य फ़ंक्शन को कॉल करता है।
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
WSF प्रारूप निम्नलिखित अतिरिक्त सुविधाओं का समर्थन करता है:
- बयान शामिल करें
- एकाधिक इंजन
- पुस्तकालय टाइप करें
- औजार
- एक फ़ाइल में एकाधिक कार्य

## डब्ल्यूएसएफ फाइलों के लाभ
WSF फाइलें निम्नलिखित क्षेत्रों में फायदेमंद हो सकती हैं:

### त्रुटि अलगाव
WSF फ़ाइल की मॉड्यूलर प्रकृति एक स्क्रिप्ट संदर्भ को दूसरे के साथ हस्तक्षेप करने से रोक सकती है जो WSF को त्रुटियों को अलग करने के लिए उपयोगी बनाता है। यहां एक मॉड्यूल के साथ WSF का एक उदाहरण दिया गया है जो एक त्रुटि उत्पन्न करता है और एक जो नहीं करता है:
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
### मिश्रित भाषा समर्थन
एक WSF कई भाषाओं का समर्थन करता है, आपके पास एक स्क्रिप्टिंग भाषा का उपयोग किसी अन्य स्क्रिप्टिंग भाषा से कोड हो सकता है। यहां एक उदाहरण दिया गया है कि यह कैसे काम करता है:
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
### स्थिरांक को उजागर करना
डब्लूएसएफ किसी ऑब्जेक्ट संदर्भ या नियंत्रण में एक्सएमएल रैपर के बाध्यकारी का समर्थन करता है ताकि आप उस ऑब्जेक्ट के स्थिरांक का उपयोग घोषित करने के बजाय कर सकें। निम्नलिखित एक उदाहरण है:
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


## संदर्भ

* [विंडोज इंस्टालर - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Windows_Installer)


